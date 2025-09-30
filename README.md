<p align="center"><b>МОНУ НТУУ КПІ ім. Ігоря Сікорського ФПМ СПіСКС</b></p>

<p align="center">
<b>Звіт з лабораторної роботи №1</b><br/>
<i>"Обробка списків з використанням базових функцій"</i><br/>
дисципліни <b>"Вступ до функціонального програмування"</b>
</p>

<p align="right"><b>Студент(-ка):</b> Корольов Юрій Ігорович, КВ-23</p>
<p align="right"><b>Рік:</b> 2025</p>

---

# Лабораторна робота 1  
**Тема:** Обробка списків з використанням базових функцій  

---

## Мета роботи
Ознайомитись із базовими типами даних та функціями **Common Lisp**, отримати практичні навички роботи зі списками.  

Опис базових типів даних, базових функцій, а також особливостей роботи з REPL та внутрішньої організації списків наведено в розділах 2–5 навчального посібника.  

Термін виконання роботи (*дедлайн*) визначається викладачем під час видачі завдання.

---

## Лістинг виконаного завдання

### Пункт 1  
```lisp
CL-USER> (defvar var1 nil)
VAR1
CL-USER> (setq var1 (list 'nil 'var 11 (cons 'k (cons '0 (list 'r 'o 'l 'y 'o 'v))) 'yurii))
(NIL VAR 11 (K 0 R O L Y O V) YURII)
CL-USER> var1
(NIL VAR 11 (K 0 R O L Y O V) YURII)
````

### Пункт 2

```lisp
CL-USER> (car var1)
NIL
```

### Пункт 3

```lisp
CL-USER> (cdr var1)
(VAR 11 (K 0 R O L Y O V) YURII)
```

### Пункт 4

```lisp
CL-USER> (third var1)
11
```

### Пункт 5

```lisp
CL-USER> (nth 4 var1)
YURII
```

### Пункт 6

```lisp
CL-USER> var1
(NIL VAR 11 (K 0 R O L Y O V) YURII)

CL-USER> (atom (first var1))
T
CL-USER> (atom (third var1))
T
CL-USER> (atom (nth 3 var1))
NIL
CL-USER> (listp (nth 3 var1))
T
CL-USER> (listp (first var1))
T
CL-USER> (listp (second var1))
NIL
```

### Пункт 7

```lisp
CL-USER> (eq (first var1) (second var1))
NIL
CL-USER> (numberp (second var1))
NIL
CL-USER> (numberp (third var1))
T
CL-USER> (plusp (third var1))
T
```

### Пункт 8

```lisp
CL-USER> (append var1 (nth 3 var1))
(NIL VAR 11 (K 0 R O L Y O V) YURII K 0 R O L Y O V)
```

---

## Варіант 11
<p align="center">
<img src="lab-1-variant.png">
</p>
```lisp
;; тут має бути лістинг (текст) виконання завдання за варіантом - також бажано
;; у вигляді пословності виконання команд в REPL і отриманого результату