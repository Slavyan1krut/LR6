# LR6
## __Лабораторная работа №6__
### __Система контроля версий__
_Цель лабораторной работы_: изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.

# Ход выполнения лабораторной работы
> Скриншоты лабораторной работы находятся в папке screenshots, каждый из них имеет название, соответствующее номеру пункта, выполнение которого необходимо подкрепить этим самым скриншотом. Например, скриншот для пункта 1 соответственно имеет название _1.PNG_
## Пункт 1
Необходимо создать аккаунт на сайте GitHub (_см. [рис. 1](https://github.com/dmit-p0/LR6/blob/Report/screenshots/1.PNG)_). 
## Пункт 2
Далее при помощи Fork создается копия [репозитория лабораторной работы](https://github.com/Kurtyanik/LR6/) в личное хранилище (_см. [рис. 2](https://github.com/dmit-p0/LR6/blob/Report/screenshots/2.PNG)_).
## Пункт 3
Соглано лабораторной работе, необходимо установить Git (_см. [рис. 3](https://github.com/dmit-p0/LR6/blob/Report/screenshots/3.png)_).
## Пункт 4
Далее с помощью _git config --global user_name_ и _git config --global user_email_ был настроен клиент git (_см. [рис. 4](https://github.com/dmit-p0/LR6/blob/Report/screenshots/4.PNG)_).
## Пункт 5
Затем на диске С в папке infa была создана копия своего личного удалённого репозитория на компьютер (_см. [рис. 5](https://github.com/dmit-p0/LR6/blob/Report/screenshots/5.PNG)_).
## Пункт 6
Теперь нужно добавить файл через интерфейс GitHub и подтянуть изменения в локальный репозиторий. На скриншоте 6 (_см. [рис. 6](https://github.com/dmit-p0/LR6/blob/Report/screenshots/6.PNG)_) представлены файлы, находящиеся в локальном репозитории, до обновленния данных и после. Их поиск осуществляется командой _ls -1_, а обновление информации - _git pull_.
## Пункты 7, 8
Далее необходимо получить историю операций для веток и просмотреть последние изменения. Первое осуществлялось с помощью команды _git reflog branch_name_, а второе - с помощью _log_ (_см. [рис. 7, 8](https://github.com/dmit-p0/LR6/blob/Report/screenshots/7_8.PNG)_).
## Пункт 9
Затем нужно выполнить слияние в ветку master. С помощью команды _git merge branch_name_ ветки _master_ и _new_file_ были объединены (содержимое new_file появилось в ветке master, _см. [рис. 9](https://github.com/dmit-p0/LR6/blob/Report/screenshots/9.PNG)_).
## Пункт 10
Теперь необходимо удалить побочную ветку. Для этого была использована команда _git branch -d branch_name_ (_см. [рис. 10](https://github.com/dmit-p0/LR6/blob/Report/screenshots/10.PNG)_).
## Пункт 11
Для наглядной работы с репозиторием необходимо сделать изменения и зафиксировать их, оставляя комментарии. Поочередно в репозиторий были добавлены три текстовых файла: minecraft.txt, fnaf.txt, fnaf2.txt, созданные командой _echo "text" >> name.txt_. Извенения фиксировались командой _git add_, для создания коммита - _git commit -m "text"_, для обновления информации в репозитории - _git push_ (_см. [рис. 11.1](https://github.com/dmit-p0/LR6/blob/Report/screenshots/11_1.PNG); [рис. 11.2](https://github.com/dmit-p0/LR6/blob/Report/screenshots/11_2.PNG); [рис. 11.3](https://github.com/dmit-p0/LR6/blob/Report/screenshots/11_3.PNG)_).
## Пункт 12
С помощью _git revert HEAD --no-edit_ был осуществлен откат коммита (_см. [рис. 12](https://github.com/dmit-p0/LR6/blob/Report/screenshots/12.PNG)_).

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
С помощью команды _git log --pretty=format:"%h - %ad - %an: %s" --date=short_ была получена история операций в укороченном виде.

3ee67ad - 2023-11-24 - 4217 Купцова П. Д: Revert "Добавлен третий файл"

9908534 - 2023-11-24 - 4217 Купцова П. Д: Добавлен третий файл

8b6398c - 2023-11-24 - 4217 Купцова П. Д: Добавлен второй файл

550a502 - 2023-11-24 - 4217 Купцова П. Д: Добавлен первый файл

06dca9d - 2023-11-24 - 4217 Купцова П. Д: Проба пера

8834cc8 - 2023-11-24 - dmit-p0: Update new_file

9e67ee0 - 2023-11-24 - dmit-p0: Create new_file

921f53b - 2020-11-21 - Kurtyanik: Обновление информации

c08a654 - 2020-11-21 - Kurtyanik: Файл создан пустым
3c6e913 - 2020-11-21 - Kurtyanik: Initial commit
