# Multiplicación de 128×128 bits (mulx128)

Programa en C que multiplica dos números de 128 bits usando el intrínseco
`_mulx_u64` (instrucción MULX) y produce un resultado de 256 bits.

## Cómo compilar

Este código usa intrínsecos SIMD, así que necesitas indicarle a gcc que
active el conjunto de instrucciones correspondiente:

```bash
gcc -mbmi2 -o mulx128 mulx128.c
```

## Cómo ejecutar

```bash
./mulx128
```

El programa multiplica dos valores de 128 bits definidos en el código
y muestra el resultado de 256 bits en hexadecimal, byte por byte.
