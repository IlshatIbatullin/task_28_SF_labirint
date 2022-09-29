Вступление
------------
Этот репозиторий содержит финальное учебное задание по курсу тестировщик-автоматизатор на Python. 
Использован шаблон объекта страницы с Selenium и Python (PyTest + Selenium) от Тимура Нурлыгаянова.
Ссылка: https://github.com/TimurNurlygayanov/ui-tests-example

В задании выбран сайт интернет-магазина Лабиринт и созданы 65 тестов, использован PageObject, 
параметризация тестов.


Файлы
-----
(conftest.py) содержит весь необходимый код для перехвата неудачных тестовых случаев и создания скриншота
страницы на случай, если какой-либо тестовый случай завершится неудачей.

(pages/base.py) содержит реализацию шаблона объекта страницы для Python.

(pages/elements.py) содержит вспомогательный класс для определения веб-элементов на веб-страницах.

(pages/......py) содержат классы и локаторы для тестируемых объектов

(tests/test_labirint_authorization.py) содержит тесты авторизации

(tests/test_test_labirint_cart.py) содержит тесты Корзина

(tests/test_labirint_postponed.py) содержит тесты Отложено

(tests/test_labirint_search.py) содержит тесты поиска


Запуск тестов
----------------
1) Установите все требования:
    ```bash
    pip3 install -r requirements
    ```
2) Скачайте Selenium WebDriver с https://chromedriver.chromium.org/downloads 
   (выберите версию, совместимую с вашим браузером)

3) Запускайте тесты:
    ```bash
    python3 -m pytest -v --driver Chrome --driver-path ~/chrome tests/*
    ```

Note:
~/chrome в этом примере - это файл Selenium WebDriver, загруженный и разархивированный на шаге #2.
