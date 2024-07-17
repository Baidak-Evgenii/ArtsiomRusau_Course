# 📌 git

Git — это система контроля версий, доступная на компьютере каждого разработчика. Это позволяет легко разветвлять и объединять. В то же время GitHub значительно упрощает индивидуальному и командному использованию Git для контроля версий и совместной работы. 🤝

Я рад поделиться некоторыми командами git, которые я использовал для создания своего портфолио на GitHub. 

## Navigation

- [Создание, клонирование, отправка и извлечение репозиториев](#task-1)
- [Создание, добавление удаленных репозиториев](#task-2)

## Task 1

##### Creating, cloning, pushing and pulling repositories  
```git
git init osukhorukova                                       # Создайте репозиторий с тем же именем, что и ваше имя пользователя.
git clone git@github.com:Baidak-Evgenii/Baidak-Evgenii.git  # Клонируйте репозиторий на своем компьютере в отдельную папку.
git clone git@github.com:testrusau/testrusau.git            # Клонируйте github.com/testrusau/testrusau на своем компьютере в отдельную папку.
cd testrusau                                                # Перенесите данные из репозитория testrusau в свой собственный.
git push git@github.com:Baidak-Evgenii/Baidak-Evgenii.git main:main
git commit -m "commited change description"                 # Откройте файл README.md и замените каждый блок отдельным коммитом.
git push 

```
## Task 2

##### Creating, adding remote repositories  
```git
git init sql                                                  # Создайте отдельный репозиторий для элемента портфолио.
git remote add sql https://github.com/Baidak-Evgenii/sql.git  # Объявить репозиторий удаленно.
README.md edited manually                                     # Добавьте ссылки на ваши репозитории в файл README.md
git commit -m "commited change description"                   # Отправить изменения в удаленный репозиторий
git push                                                     




```
