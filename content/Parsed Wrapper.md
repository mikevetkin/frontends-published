---
aliases: Обёртка с парсером
---

>[!summary]
>Цель - обернуть строку и отделить её от всех остальных строк. То есть функция `fun calculate(token: WebToken) → {// … //}` может принять только строку `WebToken` , а не какую-либо.
>
>Но в отличии от [[Simple Wrapper]] строка должна пройти этап валидации

Этот паттерн решает проблему [[Shotgun parsing]].
# Пример на TypeScript

```ts
export class AttributeName {
  public readonly string: string

  public static parse(rawString: string): Result<AttributeName, AppError> {
    if (rawString.length === 0) {
      return Result.err(attributeNameError.tooShortName)
    }

    return Result.ok(new AttributeName(rawString))
  }

  private constructor(string: string) {
    this.string = string
  }
}

```

Эта реализация чуть более сложная, чем если бы мы просто возвращали null, если строка не проходит валидацию. Но вариант с Result из библиотеки True Myth позволяет нам вернуть ошибку, которая конкретно скажет, что пошло не так

# Материалы
- https://true-myth.js.org/ - A library for safe, idiomatic null and error handling in TypeScript, with `Maybe` and `Result` types, supporting both a functional style and a more traditional method-call style.