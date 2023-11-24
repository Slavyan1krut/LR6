# LR6
## __Лабораторная работа №6__
### __Система контроля версий__
_Цель лабораторной работы_: изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.

# Ход выполнения лабораторной работы
> Скриншоты лабораторной работы находятся в папке screenshots, каждый из них имеет название, соответствующее номеру пункта, выполнение которого необходимо подкрепить этим самым скриншотом. Например, скриншот для пункта 1 соответственно имеет название _1.PNG_
## Пункт 1
Необходимо создать аккаунт на сайте GitHub (_см. screenshots/1.PNG_). 
## Пункт 2
Далее при помощи Fork создается копия [репозитория лабораторной работы](https://github.com/Kurtyanik/LR6/) в личное хранилище (_см. screenshots/2.PNG_).
## Пункт 3
Соглано лабораторной работе, необходимо установить Git (_см. screenshots/3.png_).
## Пункт 4
Далее с помощью _git config --global user_name_ и _git config --global user_email_ был настроен клиент git (_см. screenshots/4.PNG_).
## Пункт 5
Затем на диске С в папке infa была создана копия своего личного удалённого репозитория на компьютер (_см. screenshots/5.PNG_).
## Пункт 6
Теперь нужно добавить файл через интерфейс GitHub и подтянуть изменения в локальный репозиторий. На скриншоте 6 (_см. screenshots/6.PNG_) представлены файлы, находящиеся в локальном репозитории, до обновленния данных и после. Их поиск осуществляется командой _ls -1_, а обновление информации - _git pull_.
## Пункты 7, 8
Далее необходимо получить историю операций для веток и просмотреть последние изменения. Первое осуществлялось с помощью команды _git reflog branch_name_, а второе - с помощью _log_ (_см. screenshots/7_8.PNG_).
## Пункт 9
Затем нужно выполнить слияние в ветку master. С помощью команды _git merge branch_name_ ветки _master_ и _new_file_ были объединены (содержимое new_file появилось в ветке master, _см. screenshots/9.PNG_).
## Пункт 10
Теперь необходимо удалить побочную ветку. Для этого была использована команда _git branch -d branch_name_ (_см. screenshots/10.PNG_).
## Пункт 11
Для наглядной работы с репозиторием необходимо сделать изменения и зафиксировать их, оставляя комментарии. Поочередно в репозиторий были добавлены три текстовых файла: minecraft.txt, fnaf.txt, fnaf2.txt, созданные командой _echo "text" >> name.txt_. Извенения фиксировались командой _git add_, для создания коммита - _git commit -m "text"_, для обновления информации в репозитории - _git push_ (_см. screenshots/11_1.PNG; screenshots/11_2.PNG; screenshots/11_3.PNG_).
## Пункт 12
С помощью _git revert HEAD --no-edit_ был осуществлен откат коммита (_см. screenshots/12.PNG_).

# Лог команд
git config --global user.name "4217 Купцова П. Д."

git config --global user.email "polina528740@gmail.com"

cd /c/infa

git clone https://github.com/dmit-p0/LR6

ls -1

git pull

ls -1

git reflog

git log

git checkout new_file

ls -1

git checkout master

ls -1

git merge new_file

ls -1

git branch -d new_file

echo "майнкрафт это моя жизнь" >> minecraft.txt

git status

git add minecraft.txt

git status

git commit -m "Добавлен первый файл"

git push

echo "i always come back" >> fnaf.txt

git status

git add fnaf.txt

git status

git commit -m "Добавлен второй файл"

git push

echo "o holero cho to freddy fazbear" >> fnaf2.txt

git status

git add fnaf2.txt

git status

git commit -m "Добавлен третий файл"

git push

git revert HEAD --no-edit

# История операций

commit 3ee67ada4988db94bb60527a2d9d9c8da5db2803 (HEAD -> master)
Author: 4217 Купцова П. Д <polina528740@gmail.com>
Date:   Fri Nov 24 15:14:46 2023 +0300

    Revert "Добавлен третий файл"

    This reverts commit 99085342123d1fb382076763f6318e7a9497f916.

commit 99085342123d1fb382076763f6318e7a9497f916 (origin/master, origin/HEAD)
Author: 4217 Купцова П. Д <polina528740@gmail.com>
Date:   Fri Nov 24 15:12:00 2023 +0300

    Добавлен третий файл

commit 8b6398cd907c7d570001d2543f72f6a086a98c04
Author: 4217 Купцова П. Д <polina528740@gmail.com>
Date:   Fri Nov 24 15:07:00 2023 +0300

    Добавлен второй файл

commit 550a502bb90b609f22cb7fd6d80543c5417ca2b6
Author: 4217 Купцова П. Д <polina528740@gmail.com>
Date:   Fri Nov 24 15:04:28 2023 +0300

    Добавлен первый файл

commit 06dca9d4210ac23234636c2c64b6046d0a450296
Author: 4217 Купцова П. Д <polina528740@gmail.com>
Date:   Fri Nov 24 14:31:52 2023 +0300

    Проба пера

commit 8834cc825ccb762e6ed7abb69a4023f24088f6a2 (origin/new_file)
Author: dmit-p0 <113605601+dmit-p0@users.noreply.github.com>
Date:   Fri Nov 24 01:01:03 2023 +0300

    Update new_file

commit 9e67ee0d2b4c01beaa5756724969bf42991fc4b2
:...skipping...
commit 3ee67ada4988db94bb60527a2d9d9c8da5db2803 (HEAD -> master)
Author: 4217 Купцова П. Д <polina528740@gmail.com>
Date:   Fri Nov 24 15:14:46 2023 +0300

    Revert "Добавлен третий файл"

    This reverts commit 99085342123d1fb382076763f6318e7a9497f916.

commit 99085342123d1fb382076763f6318e7a9497f916 (origin/master, origin/HEAD)
Author: 4217 Купцова П. Д <polina528740@gmail.com>
Date:   Fri Nov 24 15:12:00 2023 +0300

    Добавлен третий файл

commit 8b6398cd907c7d570001d2543f72f6a086a98c04
Author: 4217 Купцова П. Д <polina528740@gmail.com>
Date:   Fri Nov 24 15:07:00 2023 +0300

    Добавлен второй файл

commit 550a502bb90b609f22cb7fd6d80543c5417ca2b6
Author: 4217 Купцова П. Д <polina528740@gmail.com>
Date:   Fri Nov 24 15:04:28 2023 +0300

    Добавлен первый файл

commit 06dca9d4210ac23234636c2c64b6046d0a450296
Author: 4217 Купцова П. Д <polina528740@gmail.com>
Date:   Fri Nov 24 14:31:52 2023 +0300

    Проба пера

commit 8834cc825ccb762e6ed7abb69a4023f24088f6a2 (origin/new_file)
Author: dmit-p0 <113605601+dmit-p0@users.noreply.github.com>
Date:   Fri Nov 24 01:01:03 2023 +0300

    Update new_file

commit 9e67ee0d2b4c01beaa5756724969bf42991fc4b2
Author: dmit-p0 <113605601+dmit-p0@users.noreply.github.com>
Date:   Fri Nov 24 00:27:20 2023 +0300

    Create new_file

commit 921f53b8d0cebf542c791cf31f04e9b792f385a4
Author: Kurtyanik <45309985+Kurtyanik@users.noreply.github.com>
Date:   Sat Nov 21 20:09:49 2020 +0300

    Обновление информации

commit c08a654a63cfc3a7146b2b7015884d9020f5cbf5
Author: Kurtyanik <45309985+Kurtyanik@users.noreply.github.com>
Date:   Sat Nov 21 20:02:16 2020 +0300

    Файл создан пустым
