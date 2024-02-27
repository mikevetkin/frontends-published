---
aliases: Простая обёртка
---
>[!summary]
>Цель - обернуть строку и отделить её от всех остальных строк. То есть функция `fun calculate(token: WebToken) → {// … //}` может принять только строку `WebToken` , а не какую-либо.

>[!warning]
>Это не просто тайп алиас, который всего навсего присваивает типу `string` другое название

# Пример на TypeScript

```ts
class WebToken {
	public readonly string: string;

	constructor(rawString: string) {
		this.string = rawString;
	}
}
```