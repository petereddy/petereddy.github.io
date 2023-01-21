---
layout: single
title:  "Opening files in the OS's default application from Emacs"
date:   2023-01-11 16:36:37 -0500
categories: emacs macOS
---

Recently, while viewing an image in Emacs, I decided the image could
do with a bit of cropping. In order to do that I needed to get the
image into my image editor. This isn't exactly a difficult proposition
but it could be accomplished in multiple ways, each of which require
multiple steps and none of which seemed entirely satisfactory to me.

My fist thought was that I wasn't exactly sure what directory the
image was in. I could open an Emacs shell and type:

```shell
$ open my-image.jpeg
``` 

to have the OS open the image editor associated with that type of
file. But I already had a Emacs shell open, so I'd need to close or
rename that shell in order to open a new one in the image file's
directory.

Wouldn't it be an *enormous* improvement if I could open the file in
the image editor with a single keystroke instead? Of course it would!
A perfect excuse to distract myself with a little elisp project!

Here it is:

```lisp
(defun os-open (arg)
  "Open the current file or directory with the OS's perferred
application. With a prefix argument (C-n), always open the
containing directory."
  (interactive "P")
  (message (concat "default-directory " default-directory))
  (when-let (path (or
                   (and arg (or
                             default-directory
                             (dired-current-directory)))
                   (dired-get-filename nil t)
                   (buffer-file-name
                    (window-buffer
                     (minibuffer-selected-window)))
                   default-directory))
    (shell-command (concat "open" " " path))))

(global-set-key (kbd "C-s-o") 'os-open)
```

Plop this in your Emacs `~/.emacs.d/init.el` file or wherever you
prefer to keep elisp code, evaluate it, and suddenly it'll be trivial
to get your OS to open files in their associated application from
Emacs.

The meat of this simple function are the parameters to the `(or)`
form. `(or)` returns the first non nil value that it encounters. 

In addition to being able to use the OS open functionality for the
file I was editing, I also wanted the option to open the directory
that contained that file. So the first input to `(or)` is:

```lisp
(and arg (or
           default-directory
           (dired-current-directory)))
```

The `(and)` form returns the last value it evaluates, so in this case
it returns the file or dired's (depending upon the buffer type)
containing directory if a prefix argument is specified (i.e. is
non-nil) when the function is invoked, e.g:

```
C-n C-s-o
```

It doesn't matter what the prefix argument is, it's just a way to
indicate that you want the containing directory and not the file
itself.

The next function in the `(or)` parameter list returns the file you're
pointing at in `dired` mode. This means you can open the file via the
OS without actually opening it in Emacs, just put the point (cursor) in
`dired` on that file and invoke the function. If the current buffer
isn't `dired` then this function simply returns nil.

The next function in the `(or)` parameter list will return the file
name for the current buffer if there is one or nil if the buffer
doesn't have an associated file.

Finally, if you're in a buffer that's a shell, the last parameter to
`(or)` is the path to the current directory of that shell, so it'll
open a Finder window on that directory.

Oh yes, Finder. This implementation uses macOS's `open` command
meaning that it's specific to that OS. There's just the one `open`
command for this purpose on macOS but, unfortunately, many different
commands that do the same thing on Linux depending upon your desktop
environment. I believe Windows uses `start` for this purpose. With a
little work this function could be enhanced to work in any
environment. If you're using a different system and lazy like me you
could simply change `"open"` to whatever command your OS uses.

![bow](/assets/images/200.webp)

Et voilà, I have successfully automated the problem away!

Never mind the fact I never got around to cropping the original image
that was the impetus for the function, and then this blog post. And
never mind that I can't remember what that image even *was* anymore or
where I wanted to use it. I'm now supremely satisfied in the knowledge
that the *next* time the need arises I'll be prepared (assuming I
remember that the function exists and the key mapping I've assigned to
it.)
