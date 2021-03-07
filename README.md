<h1 text-align="center">El lenguaje de programación Mango</h1>

Mango es un lenguaje de programación de juguete, desarrollado en V, generando código fuente en C++.
El lenguaje tiene sintaxis en inglés, respetando la tradición de los lenguajes de programación, pero,
viene con mensajes de errores y advertencias en español.

## ¿Por qué keywords y palabras en inglés, y no en español?

Esto es solo un lenguaje de juguete, su fin es el aprender a crear compiladores. Así que por eso su
sintaxis es mixta.

## ¿Osea qué esto no será algo serio a futuro?

No, no será algo serio, será solo un juguete de experimentación. También tiene como fines el
descubrir fallas en el compilador del lenguaje V.

**Ejemplo**

```rust
mod mymod {
	pub fn say(msg: string) {
		println("mymod::say: {}", msg);
	}
}

struct MyStruct {
	pub field1: string;
	pub field2: i32;
}

from mymod use say;

fn main() {
	println("Hola mundo!");
	var my_var = MyStruct{
		field1: "Field 1",
		field2: 666
	};
	println(my_var.str());
	say("Hello world! x2");
}
```

* * *

(C) 2021 Mango DevTeam - Todos los derechos reservados
