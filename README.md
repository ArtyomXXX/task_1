# Timer
Тестовое задание 1 на позицию Junior Frontend-разработчика в международную команду amoCRM

Напишите реализацию таймера.<br>
Шаг анимации таймера 1 секунда.<br>
Форматирование таймера “hh:mm:ss”.<br>
Например 01:12:59 - один час, 12 минут, 59 секунд.

---

## Stack
[![My Skills](https://skillicons.dev/icons?i=html,js)](https://skillicons.dev)

### Ссылка на [GitHub Pages](https://artyomxxx.github.io/task_1/)

## Реализация
В этом коде реализован таймер, который позволяет пользователю вводить количество секунд и начать обратный отсчёт при нажатии на кнопку Start.
Краткое описание каждого шага в коде:

1. Выбираем элементы DOM с помощью querySelector:
- inputEl - поле ввода, в который пользователь вводит количество секунд.
- buttonEl - кнопка "Start", при нажатии срабатывает обратный отсчёт.
- timerEl - элемент отображающий обратный отчёт времени в формате “hh:mm:ss”.

2. Функция formatTime принимает количество секунд и преобразует его в формат “hh:mm:ss”. Функция использует Math.floor для вычисления количества часов, минут и оставшихся секунд. Затем функция преобразует каждое значение в строку с помощью toString и дополняет ведущими нулями до двух символов с помощью padStart. Наконец, функция объединяет отформатированные значения, разделяя их двоеточием и возвращает результат.

3. Функция createTimerAnimator создает новый таймер-аниматор, который начинает обратный отсчет на основе введенных секунд. Он также предотвращает наложение нескольких таймеров путем очистки предыдущего таймера с помощью clearInterval.

4. Функция animateTimer инициализируется с помощью createTimerAnimator().

5. Обработчик события input фильтрует ввод пользователя, оставляя только числа с помощью регулярного выражения.

6. Функция startTimer начинает обратный отсчет и обновляет текст enteredValueEl на основе введенного количества секунд.

7. Обработчик события keydown отслеживает нажатие клавиши "Enter" в поле ввода и вызывает функцию startTimer, если пользователь нажал "Enter".

8. Обработчик события click отслеживает нажатие кнопки "Start" и вызывает функцию startTimer.