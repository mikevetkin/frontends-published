---
type: article
category: development
---
>[!summary]
>Тип, который позволяет сказать, что передан не пустой массив

```ts
type NonEmptyArray<T> = [T, ...T[]];
```

```ts
const statuses: NonEmptyArray<string> = [];

//  Type '[]' is not assignable to type 'NonEmptyArray<string>'.
//  Source has 0 element(s) but target requires 1.
```

```ts
const statuses: NonEmptyArray<string> = ['active'];
```
# Материалы
- https://hackage.haskell.org/package/base-4.15.0.0/docs/Data-List-NonEmpty.html;
- https://github.com/pointfreeco/swift-nonempty - Реализация на Swift;
- https://github.com/typelift/Swiftz - Библиотека для FP в Swift;
- https://stackoverflow.com/a/56006703 - Реализация на [[TypeScript]];
- https://github.com/jbranchaud/til/blob/master/typescript/create-a-non-empty-array-type.md - ещё одна реализация на [[TypeScript]].