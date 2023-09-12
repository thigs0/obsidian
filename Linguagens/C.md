
**Tabela de tipos**

| Int           | Float       | char |
| ------------- | ----------- | ---- |
| sort int      | float       | char |
| long int      | double      | wchar_t     |
| long long int | long double |      |

```c
// Números na base 10
0 , 1 , 3 ... 10 , 11 ... , 100 , -100
// Números na base octal inicia com 0
0, 01, 03, 07, 10, 011, ..., 100, -0100
// Números na base hexadecimal inicia com 0x
0x0, 0x1, 0xa, 0xb, 0x10...0x100, -0x100
// Para representar long usamos um l ou L somo sufixo e long long
usamos dois ll ou LL
1l, 3L, 07L, 0xal, 0x100LL, -0x100LL
// Para representar unsigned usamos um u ou U como sufixo
1u, 3U, 07U, 0xau, 0x100U, -0x100U
```


```c
switch ( expressão )
{
case numero: comandos ; break ;
case outro_numero: comandos ; break ;
default: comandos ; break ;
}
```

```c
for( inicialização ; condição ; expressão )
comando;
for( inicialização ; condição ; expressão )
{
//comandos do bloco for
}
```

[[Introdução a C]]
