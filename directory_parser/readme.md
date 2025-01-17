## Третє завдання (не обов'язкове)

Розробіть скрипт, який приймає шлях до директорії в якості аргументу командного рядка і візуалізує структуру цієї
директорії, виводячи імена всіх піддиректорій та файлів. Для кращого візуального сприйняття, імена директорій та файлів
мають відрізнятися за кольором.

### Вимоги до завдання:

Створіть віртуальне оточення Python для ізоляції залежностей проєкту.
Скрипт має отримувати шлях до директорії як аргумент при запуску. Цей шлях вказує, де знаходиться директорія,
структуру якої потрібно відобразити.
Використання бібліотеки colorama для реалізації кольорового виведення.
Скрипт має коректно відображати як імена директорій, так і імена файлів, використовуючи рекурсивний спосіб обходу
директорій (можна, за бажанням, використати не рекурсивний спосіб).
Повинна бути перевірка та обробка помилок, наприклад, якщо вказаний шлях не існує або він не веде до директорії.

### Рекомендації для виконання:

Спочатку встановіть бібліотеку colorama. Для цього створіть та активуйте віртуальне оточення Python, а потім встановіть
пакет за допомогою pip.
Використовуйте модуль sys для отримання шляху до директорії як аргументу командного рядка.
Для роботи з файловою системою використовуйте модуль pathlib.
Забезпечте належне форматування виводу, використовуючи функції colorama.

### Критерії оцінювання:

Створення та використання віртуального оточення.
Правильність отримання та обробки шляху до директорії.
Точність виведення структури директорії.
Коректне застосування кольорового виведення за допомогою colorama.
Якість коду, включаючи читабельність, структурування та коментарі.

### Приклад використання:

Перейдіть в папку-корінь репозиторію та створіть віртуальне оточення:

```
python3 -m venv .venv
source .venv/bin/activate
```

Встановіть пакети, перелічені у requirements.txt

```
pip install -r requirements.txt
```

Виконайте тестування консольної команди наведеними способами

```
python3 main.py .
python3 main.py ../bot
python3 main.py salary_file.txt
python3 main.py test
```

Вийдіть із віртуального оточення

```
deactivate
```

Якщо виконати скрипт та передати йому абсолютний шлях до директорії як параметр.
python3 hw03.py /шлях/до/вашої/директорії
Це призведе до виведення в терміналі списку всіх піддиректорій та файлів у вказаній директорії з використанням різних
кольорів для піддиректорій та файлів, що полегшить візуальне сприйняття файлової структури.

Для директорії зі наступною структурою

```
📦picture
 ┣ 📂Logo
 ┃ ┣ 📜IBM+Logo.png
 ┃ ┣ 📜ibm.svg
 ┃ ┗ 📜logo-tm.png
 ┣ 📜bot-icon.png
 ┗ 📜mongodb.jpg
```

Скрипт повинен вивести схожу структуру

