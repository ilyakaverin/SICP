### Создайте процедуру sum-of-squares-of-top-two, которая принимает три числа и возвращает сумму квадратов двух наибольших чисел.

```
(define (sum-of-squares-of-top-two a b c)
  (define (max-two)
  (if (>= a b)
      (if (>= b c)
          (list a b)
          (list a c))
      (if (>= a c)
          (list b a)
          (list b c))))
  (define (sum-square x y)
    (+ (* x x) (* y y)))

  (apply sum-square (max-two)))
  ```