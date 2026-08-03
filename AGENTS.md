\# Правила роботи з тестами



Коли користувач просить створити/додати новий тест:



1\. Визнач slug — назва тесту в kebab-case, транслітерація латиницею,

&#x20;  унікальна (якщо файл із такою назвою вже є — додай суфікс -2, -3 і т.д.)

2\. Збережи HTML-файл тесту рівно у: tests/<slug>.html

&#x20;  (кожен тест — окремий файл, ніколи не перезаписуй існуючі)

3\. Виконай у терміналі:

&#x20;  git add tests/<slug>.html

&#x20;  git commit -m "Add test: <slug>"

&#x20;  git push origin main

4\. Виведи користувачу готове посилання у форматі:

&#x20;  https://ilyazdovbel-sys.github.io/english/tests/<slug>.html

5\. Попередь, що посилання стане активним приблизно через 1 хвилину після пушу.

## Сценарій 2: Урок у дизайні "Talk It Out" (одна сторінка = один урок)

Коли користувач просить створити урок (а не простий тест):

1. Візьми за основу файл LESSON-TEMPLATE.html — весь CSS, екран реєстрації
   (gate), логіку перевірки та відправки EmailJS НЕ ЗМІНЮВАТИ.
2. Заміни лише: заголовок уроку (h1), crumbs (Block/Lesson), type-pill,
   lesson-goal, блок warm-up, навчальний контент (chunk-table / dialogue /
   grammar-table / passage / note — використовуй ці ж CSS-класи),
   масив EXERCISES, та список Homework — відповідно до теми користувача.
3. Визнач slug (kebab-case, транслітерація, унікальний).
4. Збережи у: tests/<slug>.html
5. git add / commit "Add lesson: <slug>" / push origin main
6. Дай посилання: https://ilyazdovbel-sys.github.io/english/tests/<slug>.html

