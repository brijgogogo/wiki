= Vim Windows =
$ :sp or :split (splits windows horizontally)
$ :sp file.ext
$ :vsplit or :vs (vertial split)
$ :on (or :only) (close all except current one)
$ Ctrl + w, w (move betwen windows)
$ Ctrl + w, (j,k,l,h) (move)
$ Ctrl-w + (increase height) (use 10 as prefix to increase 10 times, eg.
10<C-w>+)
$ Ctrl-w - (decrease height)
$ Ctrl-w > (increase width)
$ Ctrl-w < (decrease width)
$ Crtrl-w _ (to maximize height)
$ Ctrl-w | (maximize width)
$ Ctrl-w = (make all windws same size)
$ Ctrl-w r (rotates window)
$ Ctrl-w R (rotates in opposite direction)
$ Ctrl-w (H, J, K, L) (moves current window)
$ball (or :ba) open all buffers in windows (whatever can be shown)
$ :q (to close window)
$ C-w c (to close window)
$ :windo %s/#/@/g (execute in all windows)
$ :h ^ww
$ :h windows

== Resizing ==
* :resize 60 or :res 60 : change height to 60 rows
* :res +5
* :res -5
* :vertical resize 80 : change width to 80 columns
* :vertical resize +5
* :vertical resize -5
* <C-w, +>, <C-w, -> : in split, resize height of current window by a single row
* <C-w, >>, <C-w, <> : in vsplit, resize height of current window by a single column
* <C-w, 10+> : increase size by 10 lines
* <C-w, => : resize all to equal dimensions
* <C-w, _> : max height
* <C-w, |> : max width
