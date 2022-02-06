---
title: MPD-controlling GUI in Emacs
categories: emacs,mpd
...

One day I wanted to play with [/Emacs]() widgets and make a simple application. I decided to make a remote control for the [/mpd]() by wrapping a couple of [mpc](https://musicpd.org/clients/mpc/) calls.

Here is a interface part of the code (subprocess-calling part was to trivial to save it):

```commonlisp
(let ((b (get-buffer-create "*mpc*")))
  (save-current-buffer
    (set-buffer b)
    (read-only-mode -1)
    (delete-region (buffer-end -1)
                   (buffer-end 1))
    (let ((action (lambda (btn)
                    (call-mpc (button-get btn 'cmd))
                    (kill-buffer))))
      (dolist (item '(("|<" . "prev")
                      ("[]" . "stop")
                      ("||" . "toggle")
                      ("|>" . "play")
                      (">|" . "next")))
        (let* ((label (car item))
               (cmd (cdr item)))
          (insert-button label
                         'action action
                         'follow-link t
                         'cmd cmd)
          (insert " "))))
    (read-only-mode 1)
    (switch-to-buffer b)))
```