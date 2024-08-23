## Lenguajes de Programación
### Evaluación Semanal 3

#### 📝 Instrucciones

- El semanal podrá resolverse **en equipos de 3**.
- Se deberá entregar por medio de GitHub Classroom a más tardar a las **23:59:59 del martes 27 de agosto de 2024**. **No habrán prórrogas**. En caso de requerir más tiempo, se descontará un punto por cada día de entrega tardío.
- Cualquier duda podrá extenarse en la clase, por correo o por medio de Telegram en un horario de 9:00 a 18:00.
- Deberá entregarse en formato LaTeX (pueden consultar el siguiente paquete para generar reglas de inferencia: [`bussproofs.sty`](https://ctan.math.illinois.edu/macros/latex/contrib/bussproofs/BussGuide2.pdf)).
- No es necesario que vuelvan a escribir los ejercicios completos, basta con que los numeren y entreguen **en orden**.

#### 🚀 Ejercicios

1. Dadas las siguientes expresiones en sintaxis concreta de nuestro lenguaje **MiniLisp** (a) obtener su sintaxis abstracta, (b) evaluarlas usando las reglas de semántica natural y (c) evaluarlas usando las reglas de semántica estructural. Todas las reglas las podrán consultar en la [Nota de Clase 6](https://lambdasspace.github.io/LDP/notas/ldpn06.pdf) y la [Nota de Clase 7](https://lambdasspace.github.io/LDP/notas/ldpn07.pdf).

   -  `(- (+ 20 3) (- -18 (+ 50 20)))`
   -  `(not (+ 1 (- 3 (+ -8 1))))`
   -  `(not (not (+ 3 5)))`

2. Como segundo ejercicio deberán extener la batería de operaciones de **MiniLisp**, para ello deberán (a) dar la gramática libre de contexto modificada (en notación EBNF) añadiendo las nuevas construcciones del lenguaje, (b) modificar las reglas de sintaxis abstracta para considerar los nuevos constructores y finalmente (c) extender las reglas de semántica natural y estructural. En los tres casos, deberás usar la notación formal que vimos en clase.

   - Especificar un nuevo constructor `*` para la multiplicación binaria de expresiones aritméticas. Por ejemplo:
     
      ```lisp
      > (* 20 2)
      40
      ```
      
   - Especificar un nuevo constructor `/` para la división binaria de expresiones aritméticas. Consideren que no se pueden realizar divisiones entre cero. Por ejemplo: 
     
      ```lisp
      > (/ 20 2)
      10
      > (/ 10 0)
      error: División entre cero
      ```
      
   - Especificar un nuevo constructor `add1` que dada una expresión, incrementa en uno su valor. Por ejemplo:
     
      ```lisp
      > (add1 10)
      11
      ```
      
   - Especificar un nuevo constructor `sub1` que dada una expresión, decrementa en uno su valor. Por ejemplo: 
     
      ```lisp
      > (sub1 10)
      9
      ```
      
   - Especificar un nuevo constructor `sqrt` que dada una expresión, obtiene la raíz cuadrada de dicha expresión. Consideren que no se pueden calcular raíces cuadradas de números negativos. Por ejemplo: 
     
      ```lisp
      > (sqrt 81)
      9
      > (sqrt -2)
      error: Raíz negativa
      ```
      
