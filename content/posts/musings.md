+++
title = 'Prolblems with the online solution'
date = 2024-06-01T08:49:50-04:00
draft = false
+++

So the frame rate is very bad. In the container we don't have a gpu so the rendering is done by software which can be slow.
I have also tried to mount bind dev in the container but that does not work.
Also qt has vnc built in and the melonds snap works with it but no gpu.
I have not figured out how to get melonds to not crash with [vnc-eglfs](https://github.com/uwerat/vnc-eglfs).
