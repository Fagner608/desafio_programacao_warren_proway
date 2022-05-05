# desafio_programacao_warren_proway
desafio_programacao_warren_proway
Linguagem utulizada: R

Desafio 1
```{r}

desafio1 <- function(){
install.packages("stringi")
library(stringi)
first_sequence <- 10:100000
excluded_numbers <- seq(10,100000, 10)
first_sequence[first_sequence %in% excluded_numbers] <- NA
first_sequence <- na.omit(first_sequence)
second_sequence <- as.numeric(stri_reverse(first_sequence))
data_sequence <- data.frame(first_sequence, second_sequence)
data_sequence$results <- data_sequence$first_sequence + data_sequence$second_sequence
data_sequence[data_sequence[,3]%%2 == 0, ] <- NA
data_sequence <- na.omit(data_sequence)
data_sequence[1]
}

desafio1()

```
-------------------------------------

Desafio 02

```{r}
class_forecast <- function(){
  total_number_students <- 30 #número de estudantes matriculados
individual_arrival_tima <- round(runif(30, 1, 50), 0) #tempo individual de chagada, sorteado aleatoriamente para este problema
time_limit_arrival <- 15 #tempo limite de tolerância
minimum_students_present <- total_number_students*0.40 #presença mínima na aula de 40% da turma
results <- if (sum(individual_arrival_tima < time_limit_arrival) > minimum_students_present) { 
  print("Aula normal")
} else {
  print("Aula encerrada")
}
}

class_forecast()

```
------------------------------------

Desafio 03


```{r}

```

