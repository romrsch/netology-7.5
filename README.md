# netology-7.5
## Домашнее задание к занятию "7.5. Основы golang"



### Задача 1. Установите golang.

1. Воспользуйтесь инструкций с официального сайта: https://golang.org/.
2. Так же для тестирования кода можно использовать песочницу: https://play.golang.org/.

***Ответ:***

![alt](https://i.ibb.co/tpbqHL9/Screenshot-7.jpg)

![alt](https://i.ibb.co/1K40Zzv/Screenshot-1.jpg)

![alt](https://i.ibb.co/4YqYPKB/Screenshot-2.jpg)

---

### Задача 2. Знакомство с gotour.

У Golang есть обучающая интерактивная консоль https://tour.golang.org/. 

Рекомендуется изучить максимальное количество примеров. В консоли уже написан необходимый код, осталось только с ним ознакомиться и поэкспериментировать как написано в инструкции в левой части экрана.

***Ответ:***

https://tour.golang.org/basics/1

Функция выдает рандомное число из 100:

![alt](https://i.ibb.co/hgdFsLN/Screenshot-4.jpg)


---

### Задача 3. Написание кода.

Цель этого задания закрепить знания о базовом синтаксисе языка. Можно использовать редактор кода на своем компьютере, либо использовать песочницу: https://play.golang.org/.

```
package main

import "fmt"

func main() {
    fmt.Print("Enter a number: ")
    var input float64
    fmt.Scanf("%f", &input)

    output := input * 2

    fmt.Println(output)    
}
```

2. Напишите программу, которая найдет наименьший элемент в любом заданном списке, например:

```
x := []int{48,96,86,68,57,82,63,70,37,34,83,27,19,97,9,17,}
```

3. Напишите программу, которая выводит числа от 1 до 100, которые делятся на 3. То есть `(3, 6, 9, …).`


***Ответ:***
 
 1. >Код программы для перевода футов в метры
 ```
 package main

        import "fmt"
        import "math"

        func main() {
            fmt.Print("Enter foot: ")
            var input float64

            fmt.Scanf("%f", &input)           // округлим до 2х знаков
            output := input * float64(0.3048) // точное значение 
            rOutput := math.Round(output)     // округлим до целого
            sOutput := fmt.Sprintf("( %.2f)", output)
            fmt.Println("Value in Meters:", rOutput, sOutput )
        }
 ```
Результат работы программы:

![alt](https://i.ibb.co/k1ydkrQ/Screenshot-6.jpg)

2. >программа, которая найдет наименьший элемент в любом заданном списке


```
package main

        import "fmt"

        func main() {
             x := []int{48,96,86,68,57,82,63,70,37,34,83,27,19,97,9,17,}

            current := 0
            fmt.Println ("Список значений : ", x)
            for i, value := range x {
                if (i == 0) {
                   current = value
                } else {
                    if (value < current){
                        current = value
                    }
                }
            }
            fmt.Println("Минимальное число : ", current)
        }
```
Результат работы программы:

![alt](https://i.ibb.co/HGDv7Cn/Screenshot-9.jpg)

3. > Напишите программу, которая выводит числа от 1 до 100, которые делятся на 3. 
   > То есть `(3, 6, 9, …).`


Код программы:

```
package main
        
        import "fmt"
       
        func main() {
            
            for i := 1; i <= 100; i++ {
                if ((i-1)%10) ==0 {
                     fmt.Print(i-1," -> ")
                }            
                        
                if (i%3) == 0 {
                    fmt.Print(i,", ")
                    }
                if (i%10) ==0 {
                    fmt.Println()
                }
            }
        }
```

Результат работы программы:

![alt](https://i.ibb.co/yN8VC8J/Screenshot-10.jpg)
