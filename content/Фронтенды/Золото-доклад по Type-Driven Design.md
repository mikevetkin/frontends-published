---
date: 2024-03-02
author: Михаил Веткин
---
![[TDD with Swift.png]]

## Комментарий к докладу

Хочу поделиться интересным докладом от iOS разработчика из American Express.

Идеи, которые он транслирует, я уже год со своими коллегами реализую в проектах Ozon Aqcuiring на языке TypeScript.

Мне кажется, будет полезно увидеть, как пишут код такие же фронты, но на другой платформе, ознакомится с оригиналом и тем, на чём он основан, а позже в серии заметок я выложу свой конспект доклада с реализацией большинства идей на TypeScript.

## Доклад

![Type-Driven Design in Swift](https://youtu.be/pbVjkY9fS8c?si=bhM0Sjom22GM34FZ)

## Темы

- Доменное моделирование на основе типов;
- Функциональные паттерны и типы;
- Превращение частичных функций в полные;
- Превращение функций с сайд эффектами в чистые
- Value Oriented Programming;
- Функциональная dependency injection.

## Мысли

- Несмотря на то, что в TS структурная, а не номинальная система типов, почти всё, что рассказано в докладе, можно реализовать на TS;
- Я теперь по-другому смотрю на Redux/useReducer. За свою практику видел много кода, где редьюсеры используются, как value setter'ы, а в миддлварах лежала бизнес логика, которая не покрывалась unit-тестами, но зато были тривиальные тесты на редьюсеры, что вообще бессмысленно. Ладно, об этом позже;
- Стоит также прочитать [Redux is half of pattern](https://dev.to/davidkpiano/redux-is-half-of-a-pattern-1-2-1hd7) . Это хорошо ляжет на доклад;
- Важно, что когда я говорю "Redux", то это про идею использования редьюсеров с однонаправленным потоком данных, а не про сам фреймворк. Я в курсе, что его [захейтил](https://habr.com/ru/companies/jugru/articles/545024/#redux) Даниил Абрамов, просто так фронту легче понять, что за концепции обсуждаются;
- Рекомендую смотреть доклад в [Obsidian](https://obsidian.md/) с использованием плагина[ Timestamp Notes](https://github.com/juliang22/ObsidianTimestampNotes);

## Вдохновляет

- Идея разрабатывать веб на связке Kotlin-JS, вместо TS-JS
- Мысль, что ты можешь работать в области 5 лет и всё равно ещё будет море вещей, которые можно узнавать и чувствовать себя Незнайкой
- Человек, придумавший мандарины без косточек
- Запах весны. Сейчас суббота, открыто окно, дует приятный ветерок, а я сижу и почему-то вместо прогулки пытаюсь понять, как перевести фамилию Luposchainsky...

## Тэги

#typeDrivenDesign #юнитТестирование #фронтенды, #valueOrientedProgramming, #чистыеФункции, #functionalProgramming, #доклад, #swift, #ios, #patterns, #fcis

## Материалы

- [Boundaries](https://www.destroyallsoftware.com/talks/boundaries) - доклад Гэри Бернхардта;
- [Parse, don’t validate](https://lexi-lambda.github.io/blog/2019/11/05/parse-don-t-validate/) - статья Алексис Кинг;
- [Domain Modeling Made Functional](https://www.amazon.com/Domain-Modeling-Made-Functional-Domain-Driven-ebook/dp/B07B44BPFB); - книга Скотт Влашин;
- [Boolean Blindness](https://existentialtype.wordpress.com/2011/03/15/boolean-blindness/) - статья Роберта Харпера;
- [Algebraic blindness](https://github.com/quchen/articles/blob/master/algebraic-blindness.md) - статья Дэвида Лупосчаинского;
- [Value-Oriented Programming](https://matt.diephouse.com/2018/08/value-oriented-programming/) - статья Мэтта Дипхауса.