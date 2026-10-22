# на каком объёме процесс упал с MemoryError 
~~~
gao@fedora:~$ ( ulimit -v 307200; python3 ~/eat.py )
MemoryError на 60 МБ
~~~
# Что делает ulimit -v
