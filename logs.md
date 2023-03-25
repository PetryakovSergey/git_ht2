1. Просмотрите историю коммитов в своём проекте и выберите три случайных коммита. Просмотрите изменения, которые были в них сделаны.

>git log -p -3


2. Верните эти изменения командой git revert последовательно, чтобы в итоге получилось тоже три коммита.
>git revert bbf1b69d6
>git add .
>git commit -m "First training commit"

>git revert daaa3d32
>git add .
>git commit -m "Second training commit"

>git revert fe4e2639
>git add .
>git commit -m "Third training commit"


3. Попробуйте отменить эти три коммита:
* последний — командами git reset --soft и git restore;

>git reset --soft 70678daec8d

* предпоследний — командой git reset --mixed и git restore;

>git reset --mixed 9da14523c6
>git add .
>git commit -m "Commit after git reset --mixed"

* первый — командой git reset --hard. 

>git reset --hard 8897d25c
