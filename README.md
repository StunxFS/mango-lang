# El lenguaje de programación Mango

Mango es un lenguaje de programación de juguete, desarrollado en Python usando LLVM como backend ([llvmlite](https://github.com/numba/llvmlite)).
El lenguaje tiene sintaxis en inglés, respetando la tradición de los lenguajes de programación, pero, viene con mensajes de errores y advertencias
en español.

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

fn require_in_heap(arg1: ^MyStruct) {
	println(arg1.field1);
}

from mymod use say;

fn main() {
	println("Hola mundo!");
	var my_var = MyStruct{
		field1: "Field 1",
		field2: 666
	};
	println(my_var.str());
	const my_var_in_heap = new MyStruct{
		field1: "333+333+111",
		field2: 777
	};
	require_in_heap(my_var_in_heap);
	println(my_var_in_heap);
	free my_var_in_heap;
	say("free!");
}
```

* * *

(C) 2021 Mango DevTeam - Todos los derechos reservados
