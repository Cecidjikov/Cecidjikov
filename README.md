# Създаване на нова папка за проект
mkdir my_local_repository

# Влизане в папката
cd my_local_repository

# Инициализация на Git хранилище
git init

# Създаване на нов текстов файл (можете да използвате nano, vim или любим текстов редактор)
echo "This is a sample file." > sample.txt

# Добавяне на файла към индекса
git add sample.txt

# Записване на промените в хранилището
git commit -m "Initial commit - added sample.txt"

# Създаване на нов клон
git clone my_local_repository my_second_clone

# Влизане в новия клон
cd my_second_clone

# Редактиране на файла (пример: добавяне на нов ред)
echo "Added a new line." >> sample.txt

# Добавяне и записване на промените в новия клон
git add sample.txt
git commit -m "Made changes in the second clone"

# Връщане в основния клон
cd ../my_local_repository

# Редактиране на файла (пример: добавяне на още един нов ред)
echo "Made additional changes in the main clone." >> sample.txt

# Добавяне и записване на допълнителните промени в основния клон
git add sample.txt
git commit -m "Made additional changes in the main clone"

# Връщане в основния клон
cd ../my_local_repository

# Сливане на промените от втория клон в основния клон
git pull origin master

# Възможно е да възникне конфликт - ръчно разрешаване на конфликта в sample.txt
# След това добавяне и записване на промените
git add sample.txt
git commit -m "Resolved conflicts with the second clone"

# Изтриване на втория клон
cd ..
rm -rf my_second_clone

# Създаване на README файл
echo "# My Git Project" > README.md
echo "This is a sample Git project." >> README.md

# Добавяне и записване на README файла в хранилището
git add README.md
git commit -m "Added README file"

