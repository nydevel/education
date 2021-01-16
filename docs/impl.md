# impl

impl

### Типы:
Если impl используется для типов - это реализация данного типа.

У нас есть структура:
```rust
struct Example {
    number: i32,
}
```
И нам нужно на ее основе сделать реализацию:  
```rust
impl Example {
    fn get_number(&self) -> i32 {
        self.number
    }
}
```
Вот, мы реализовали объект с методами, и работаем с его параметрами как будто они уже в нем объявлены.

### Trait:
Трейты это описание методов для неизвестного типа.
impl для трейтов - это реализация трейтов для типов или для других трейтов.

```rust
struct Example {
    number: i32,
}

trait Thingy {
    fn do_thingy(&self);
}

impl Thingy for Example {
    fn do_thingy(&self) {
        println!("doing a thing! also, number is {}!", self.number);
    }
}
```
