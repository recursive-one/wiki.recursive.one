---
categories: emacs,emacs-lisp
toc: no
...

# "ielm it!"

I tried to implement a function supposed to run **ielm** ([/Emacs]() [/Lisp]() REPL) in a context of current buffer to be able to apply some `(insert)`-like stuff to that particular buffer.

The success wasn't complete, but maybe I'll try to improve it someday. The problem is that ielm works only in a context of itself. So I provide a macro `(*> ..)` that works like `(with-current-buffer <target> ..)` but frees you from providing a target buffer each time.

```commonlisp
(defun my/ielm-it ()
  (interactive)
  (let* (old-point
         (target-buf (current-buffer))
         (tgt-name (buffer-name target-buf))
         (buf-name (format "*ielm (%s)*" tgt-name))
         (buf (get-buffer-create buf-name)))
    (unless (comint-check-proc buf)
      (with-current-buffer buf
        (unless (zerop (buffer-size))
          (setq old-point (point)))
        (inferior-emacs-lisp-mode)
        (setq-local my/ielm/target target-buf)))
    (pop-to-buffer buf)
    (when old-point
      (push-mark old-point))))

(defmacro *> (&rest body)
  `(when (ielm-process)
     (when-let ((tgt (when (local-variable-p 'my/ielm/target)
                       my/ielm/target)))
       (with-current-buffer tgt
         ,@body))))
```