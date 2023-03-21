Перед запуском тестов в файле settings указываем действующий логин, пароль зарегистрированного пользователя.
Запуск тестов осуществляем в консоле командой:
 python3 -m pytest -v --driver Chrome --driver-path <полный путь к драйверу> tests/Tests.py
В проекте я применил сценарий по позитивному и негативному тестированию. Так же примениил технику тест-дизайна "Анализ граничных значений" в проверке поля ввода "Имя" формы регистрации.

Тест-кейсы:

EXP-001 Тест авторизации с валидными значениями e-mail и пароля.

EXP-002 Проверка аутентификации пользователя с невалидным email и паролем: связка Почта+Пароль валидна, но пользователь с такими данными не зарегистрирован в системе; пустые значения.

EXP-003 Проверяем аутентификации пользователя с невалидным email и паролем: связка Почта+Пароль валидна, но пользователь с такими данными не зарегистрирован в системе; пустые значения.

EXP-004 Проверяем Формы "Авторизация" на наличие основных элементов.

EXP-005 Проверяем названия табов в меню выбора типа авторизации.

EXP-006 Проверка выбора таба по умолчанию в Меню выбора типа авторизации.

EXP-007 Тест смены полей ввода при смене типа авторизации.

EXP-008 Тест перехода к форме "восстановление пароля".

EXP-009 Тест перехода к форме "Регистрация".

EXP-010 Проверка блока с продуктовым слоганом компании на странице "Регистрация".

EXP-011 Проверка Формы "Регистрация" на наличие основных элементов.

EXP-012 Проверка Формы "Регистрация" на соответствие названий элементов блока требованию.

EXP-013 Проверка Регистрации пользователя с валидными данными: "Имя" и "Фамилия" написанных кириллицей.

EXP-014 Проверка на уникальность введенного e-mail в форме "Регистрация".

EXP-015 Тест формы "Авторизация" после нажатия кнопки "Войти" при регистрации пользователя e-mail, который уже был использован ранее для регистрации.

EXP-016 Тест поля ввода "Имя" формы "Регистрация" допустимыми валидными значениями: буквы кириллицы в количестве 2 ; 3 ; 15 ; 29 ; 30 .

EXP-017 Тест поля ввода "Имя" формы "Регистрация" невалидными значениями: пустое значение; буквы кириллицы в количестве 1 ; 100 ; 256 ; латиницы буквы; китайские иероглифы; спецсимволы; числа.

EXP-018 Тест поля ввода "Пароль" формы "Регистрация" валидными значениями: символы из букв латиницы прописью и строчные+числа в количестве 8 ; 15 ; 20 .

EXP-019 Тест поля ввода "Пароль" и "Подтвердить пароль" формы «Регистрация» валидными значениями(пароли совпадают).

EXP-020 Тест поля ввода "Пароль" и "Подтвердить пароль" формы «Регистрация» невалидными значениями(пароли не совпадают).