# Primos p tales que p³ − 4p + 9 es cuadrado perfecto

## Enunciado

Hallar todos los números primos $p$ tales que $p^3 - 4p + 9$ es un cuadrado perfecto.

---

> **Mariano:** Hallar todos los números primos p tales que p^3 - 4 p + 9 es un cuadrado perfecto.

**Claude:**

### Solución

Buscamos todos los primos $p$ tales que $p^3 - 4p + 9 = k^2$ para algún entero $k \geq 0$.

**Verificación de primos pequeños**

| $p$ | $p^3 - 4p + 9$ | ¿Cuadrado? |
|-----|-----------------|------------|
| 2   | $9 = 3^2$       | **Sí** |
| 3   | $24$            | No |
| 5   | $114$           | No |
| 7   | $324 = 18^2$    | **Sí** |
| 11  | $1296 = 36^2$   | **Sí** |
| 13  | $2154$          | No |

**Demostración de que no hay más soluciones**

Como $k^2 = p^3 - 4p + 9$, se tiene $k^2 \equiv 9 \pmod{p}$, por lo que $k \equiv \pm 3 \pmod{p}$.

**Caso 1: $k = mp + 3$** para algún entero $m \geq 0$.

Sustituyendo:

$$m^2p^2 + 6mp + 9 = p^3 - 4p + 9 \implies p(p - m^2) = 6m + 4$$

El lado derecho es positivo, así que $p > m^2$. Como $p \mid (6m+4)$, se tiene $p \leq 6m + 4$. Combinando: $m^2 < 6m + 4$, lo que da $m \leq 6$.

Probando cada valor:
- $m = 0$: $p^2 = 4 \Rightarrow p = 2$ ✓
- $m = 3$: $p^2 - 9p - 22 = 0 \Rightarrow p = \frac{9+13}{2} = 11$ ✓
- Los demás valores ($m = 1,2,4,5,6$) no dan enteros.

**Caso 2: $k = (m+1)p - 3$** para algún entero $m \geq 0$. Sea $n = m+1$.

Sustituyendo:

$$p(n^2 - p) = 6n - 4$$

Entonces $p \mid (6n-4)$ y $n^2 > p$. Escribiendo $p = n^2 - q$ con $6n - 4 = (n^2 - q)q$, se obtiene la ecuación:

$$q^2 - n^2q + 6n - 4 = 0 \implies q = \frac{n^2 \pm \sqrt{n^4 - 24n + 16}}{2}$$

Para $n \geq 12$: $(n^2-1)^2 < n^4 - 24n + 16 < (n^2)^2$, así que no hay cuadrado perfecto.

Verificando $n = 1$ a $11$, solo $n = 3$ da discriminante perfecto: $81 - 72 + 16 = 25 = 5^2$.
- $q = 7 \Rightarrow p = 9 - 7 = 2$ ✓
- $q = 2 \Rightarrow p = 9 - 2 = 7$ ✓

**Respuesta**

$$\boxed{p \in \{2,\, 7,\, 11\}}$$

Con $2^3 - 8 + 9 = 3^2$, $\;7^3 - 28 + 9 = 18^2$, $\;11^3 - 44 + 9 = 36^2$.

---

> **Mariano:** No entendí por qué esta parte, creo que no la demostraste:
>
> Para $n \geq 12$: $(n^2-1)^2 < n^4 - 24n + 16 < (n^2)^2$, así que no hay cuadrado perfecto.

**Claude:**

Tenés razón, lo afirmé sin justificarlo. Acá va la demostración:

**Prueba de que $n^4 - 24n + 16$ no es cuadrado perfecto para $n \geq 12$**

Queremos mostrar que para $n \geq 12$:

$$(n^2 - 1)^2 < n^4 - 24n + 16 < (n^2)^2$$

**Cota superior:** $n^4 - 24n + 16 < n^4$ es inmediato pues $24n > 16$ para todo $n \geq 1$.

**Cota inferior:** Expandimos $(n^2-1)^2 = n^4 - 2n^2 + 1$. Necesitamos:

$$n^4 - 2n^2 + 1 < n^4 - 24n + 16$$

$$\iff 0 < 2n^2 - 24n + 15$$

El discriminante es $576 - 120 = 456$, con raíces $\frac{24 \pm \sqrt{456}}{4} \approx \frac{24 \pm 21.35}{4}$, es decir $\approx 0.66$ y $\approx 11.34$.

Entonces $2n^2 - 24n + 15 > 0$ para todo $n \geq 12$. $\square$

**Conclusión:** Para $n \geq 12$, el valor $n^4 - 24n + 16$ queda estrictamente entre dos cuadrados perfectos consecutivos ($(n^2-1)^2$ y $(n^2)^2$), por lo que no puede ser él mismo un cuadrado perfecto.
