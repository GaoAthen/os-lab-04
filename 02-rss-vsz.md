# Таблица RSS/VSZ
~~~
gao@fedora:~$ ps -eo pid,user,vsz,rss,comm --sort=-rss | head -10

    PID USER        VSZ   RSS COMMAND
   2431 gao      1273984 229288 gnome-software
   3288 gao      1376684 218780 ptyxis
   2130 gao      3581916 217780 gnome-shell
   3038 root     707064 200668 dnf5daemon-serv
   3140 gao      616320 107836 ibus-engine-tb
   2827 gao      978748 83352 mutter-x11-fram
   2426 gao      1289916 74528 evolution-alarm
   2567 gao      263440 70200 Xwayland
   2345 gao      1051460 53628 evolution-sourc
~~~
# python-процессы
~~~
[Первый]
ps -o pid,vsz,rss,comm -C python3
    PID    VSZ   RSS COMMAND
   3442 754200  9872 python3
[Второй]
gao@fedora:~$ ps -o pid,vsz,rss,comm -C python3
    PID    VSZ   RSS COMMAND
   3486 754200 521756 python3
~~~
# Разница RSS с VSZ 
У первого RSS маленький а VSZ большой потому что RSS показывает то сколько процесс на самом деле занимает памяти, а VSZ показывает то сколько всего у него имеется памяти(запрошено или зарезервированно)
# Выделено ≠ занято
Память выдаётся, но физически выделяется только тогда когда в неё что либо записывается
