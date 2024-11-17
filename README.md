# LR6
## Лабораторная работа №6
### Система контроля версий
_Цель лабораторной работы_: изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.

# Ход выполнения лабораторной работы
> Скриншоты лабораторной работы находятся в папке screenshots, каждый из них имеет название. Например, скриншот для пункта 1 соответственно имеет название _1.PNG_
## Пункт 1
Необходимо создать аккаунт на сайте GitHub (_см. [рис. 1](https://github.com/Slavyan1krut/LR6/blob/report/screenshots/1.png)_). 
## Пункт 2
Далее при помощи Fork создается копия [репозитория лабораторной работы](https://github.com/Kurtyanik/LR6/) в личное хранилище (_см. [рис. 2](https://github.com/Slavyan1krut/LR6/blob/report/screenshots/2.png)_).
## Пункт 3
Соглано лабораторной работе, необходимо установить Git (_см. [рис. 3](https://github.com/Slavyan1krut/LR6/blob/report/screenshots/3.png)_).
## Пункт 4
Далее с помощью _git config --global user_name_ и _git config --global user_email_ был настроен клиент git (_см. [рис. 4](https://github.com/Slavyan1krut/LR6/blob/report/screenshots/4.png)_).
## Пункт 5
Затем на диске С в папке labs была создана копия своего личного удалённого репозитория на компьютер (_см. [рис. 5](https://github.com/Slavyan1krut/LR6/blob/report/screenshots/5.png)_).
## Пункт 6
Теперь нужно добавить файл через интерфейс GitHub и подтянуть изменения в локальный репозиторий. На скриншоте 6 (_см. [рис. 6](https://github.com/Slavyan1krut/LR6/blob/report/screenshots/6.png)_) представлены файлы, находящиеся в локальном репозитории, до обновленния данных и после. Их поиск осуществляется командой _ls -1_, а обновление информации - _git pull_.
## Пункты 7, 8
Далее необходимо получить историю операций для веток и просмотреть последние изменения. Первое осуществлялось с помощью команды _git reflog branch_name_, а второе - с помощью _log_ (_см. [рис. 7](https://github.com/Slavyan1krut/LR6/blob/report/screenshots/7.png)_).
## Пункт 9
Затем нужно выполнить слияние в ветку master и разрешить конфликт слияния веток. С помощью команды _git merge branch_name_ ветки _master_ и _branch1_ были объединены (содержимое branch1 появилось в ветке master, _см. [рис. 8](https://github.com/Slavyan1krut/LR6/blob/report/screenshots/8.png), [рис. 9](https://github.com/Slavyan1krut/LR6/blob/report/screenshots/9.png), [рис. 10](https://github.com/Slavyan1krut/LR6/blob/report/screenshots/10.png)_).
## Пункт 10
Теперь необходимо удалить побочную ветку в GitHub и на устройстве. Для этого были использованы команды _git push --delete branch_name_ и _git branch -d branch_name_ (_см. [рис. 11](https://github.com/Slavyan1krut/LR6/blob/report/screenshots/11.png)_).
## Пункт 11
Для наглядной работы с репозиторием необходимо сделать изменения и зафиксировать их, оставляя комментарии. Поочередно в репозиторий были добавлены три текстовых файла: file1.txt, file2.txt, file3.txt, созданные командой _echo "text" >> name.txt_. Извенения фиксировались командой _git add_, для создания коммита - _git commit -m "text"_, для обновления информации в репозитории - _git push_ (_см. [рис. 12](https://github.com/Slavyan1krut/LR6/blob/report/screenshots/12.png); [рис. 13](https://github.com/Slavyan1krut/LR6/blob/report/screenshots/13.png); [рис. 14](https://github.com/Slavyan1krut/LR6/blob/report/screenshots/14.png)_).
## Пункт 12
С помощью _git revert HEAD --no-edit_ был осуществлен откат коммита (_см. [рис. 15](https://github.com/Slavyan1krut/LR6/blob/report/screenshots/15.png)_).

# Лог команд
git config --global user.name "4315 Кайль В. С."

git config --global user.email "Slavyan2krut@gmail.com"

cd C:/Users/Пользователь/Documents/guap/labs

git clone https://github.com/Slavyan1krut/LR6

ls -1

git pull

ls -1

git reflog

git log

git checkout branch1

ls -1

git checkout master

ls -1

git merge branch1

ls -1

git branch -d branch1

git push origin --delete branch1

git commit -m "Разрешен конфликт слияния веток"

echo "It's very hard" >> file1.txt

ls

git status

git add file1.txt

git status

git commit -m "Добавлен file1"

echo "Many things in this world are not unnatainable" >> file2.txt

git status

git add file2.txt

git status

git commit -m "Добавлен file2"

echo "I hope that it's final" >> file3.txt

git status

git add file3.txt

git status

git commit -m "Добавлен file3"

git push

git revert HEAD --no-edit

git push

# История операций

e6bde66 - 2024-11-18 - Кайль В.С. 4315: Добавлены все скриншоты
4eebc11 - 2024-11-18 - Кайль В.С. 4315: добавлены скриншоты
ef48cb6 - 2024-11-16 - Кайль В.С. 4315: Revert "Добавлен file3"
ee7828f - 2024-11-16 - Кайль В.С. 4315: Добавлен file3
16cb00a - 2024-11-16 - Кайль В.С. 4315: Добавлен file2
4e01270 - 2024-11-16 - Кайль В.С. 4315: Добавлен file1
c1ab5fc - 2024-11-15 - Кайль В.С. 4315: Разрешен конфликт слияния веток
10499f4 - 2024-11-15 - Vyacheslav Kail: Create first_file
921f53b - 2020-11-21 - Kurtyanik: Обновление информации
c08a654 - 2020-11-21 - Kurtyanik: Файл создан пустым
3c6e913 - 2020-11-21 - Kurtyanik: Initial commit
