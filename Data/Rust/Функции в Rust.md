Функции в [[Rust|Rust]] имеют некоторые синтаксические особенности, по сравнению с другими языками. Например, для возврата значения можно использовать строку без точки запятой на конце или классическое ключевое слово `return` .

**Пример объявления функции:**

```Rust
fn is_even(n: i32) -> bool {
    if n % 2 == 0 {
        return true
    }
    return false
}
```

**Пример объявления функции без return:**

```Rust
fn add(a: i32, b: i32) -> i32 {
	a + b  // Без точки запятой на конце
}
```

