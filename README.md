# RETO-9 

### PUNTO 1

De los retos anteriores selecione 3 funciones y escribalas en forma de lambdas.

##### EJEMPLO 1

Una función matemática para calcular el volumen y el área superficial. Cree dos funciones en python para calcular los valores antes establecidos, al ingresar por teclado r1, r2 y h. Revise como utilizar el valor de pi usando import math y math.pi

Ejemplo sin lambda

```
# EJEMPLO 1 , PUNTO 1, RETO 6 SIN LAMBDA

import math as m #importar libreria math
p= m.pi #importar el valor exacto de pi
def Volumen_figura(radio1:float, altura_cono:float, radio2:float) -> float:
  vol = ((4*p*(radio1**3))/3) + ((altura_cono*p*(radio2**2))/3)
  return vol  #se definio la variable del volumen

def Area_superficial_figura(radio1:float, altura_cono:float, radio2:float) -> float:
  area_sup = (4*p*(radio1**2)) + (p*radio2*(radio2+((radio2**2)+(altura_cono**2)**0.5)))
  return area_sup #se definio la variable del area superficial

if __name__ == "__main__":
  radio1 = float(input("El radio de la esfera:"))
  altura_cono = float(input("La altura del cono:"))
  radio2 = float(input("El radio del cono:"))
  volumen = Volumen_figura(radio1, altura_cono, radio2)
  area_superficial = Area_superficial_figura(radio1, altura_cono, radio2)
  print("El volumen de la figura es " + str(volumen)+ " y el area superficial es " +str(area_superficial)) #se puso condicional if que defina las variables con teclado y me imprima los valores de volumeny area superficial
```

Ejemplo con lambda

```
# EJEMPLO 1, PUNTO 1, RETO 6 LAMBDA
import math as m
if __name__ == "__main__":
  radio1 = float(input("El radio de la esfera:"))
  altura_cono = float(input("La altura del cono:"))
  radio2 = float(input("El radio del cono:"))
  p = m.pi
  vol = (lambda radio1, altura_cono, radio2: ((4*p*(radio1**3))/3) + ((altura_cono*p*(radio2**2))/3))(radio1,altura_cono,radio2)
  area_sup= (lambda radio1, altura_cono, radio2: (4*p*(radio1**2)) + (p*radio2*(radio2+((radio2**2)+(altura_cono**2)**0.5))))(radio1,altura_cono,radio2)
  print("El volumen de esta figura es: " +str(vol))
  print("El area superficial de la figura es: " +str(area_sup))
```
##### EJEMPLO 2

Una función matemática para calcular el área y el perimetro. Cree dos funciones en python para calcular los valores antes establecidos, al ingresar por teclado r, a y b. Revise como utilizar el valor de pi usando import math y math.pi

Ejemplo sin lambda

```
# EJEMPLO 2, PUNTO 2, RETO 6 sin LAMBDA
import math as m #importar libreria math
p= m.pi #importar el valor exacto de pi
def area_2_figura(base:float, altura:float, radio:float) -> float:
  area_2 = (base*altura) + 2*(p*(radio)**2)
  return area_2  #se definio la variable del Area

def perimetro_2_figura(base:float, altura:float, radio:float) -> float:
  per_2 = ((2*base)+(2*altura)) + (2*p*radio)
  return per_2 #se definio la variable del perimetro

if __name__ == "__main__":
  radio = float(input("El radio del circulo:"))
  base = float(input("La base de la figura:"))
  altura = float(input("La altura de la figura:"))
  area_ = area_2_figura(base, altura, radio)
  perimetro_ = perimetro_2_figura(base, altura, radio)
  print("El area de la figura es " + str(area_)+ " y  area superficial es " +str(perimetro_)) #se puso condicional if que defina las variables con teclado y me imprima los valores de area y permietro
```

Ejemplo con lambda

```
# EJEMPLO 2, PUNTO 2, RETO 6 LAMBDA
import math as m
p= m.pi
if __name__ == "__main__":
  radio = float(input("El radio del circulo:"))
  base = float(input("La base de la figura:"))
  altura = float(input("La altura de la figura:"))
  area_ = (lambda base, altura, radio: ((base*altura) + 2*(p*(radio)**2)))(base, altura, radio)
  perimetro_ = (lambda base, altura, radio: (((2*base)+(2*altura)) + (2*p*radio)))(base, altura, radio)
  print("El area de la figura es " + str(area_)+ " y  area superficial es " +str(perimetro_))
```
##### EJEMPLO 3

Haga un programa que utilice una función para calcular el valor de un préstamo C usando interés compuesto del i por n meses.

Ejemplo sin labda
```
# EJEMPLO 3, PUNTO 5, RETO 6 SIN LAMBDA
def prestamo(cantidad_dinero_prestamo:float, interes:float, meses:float) -> float:
  dinero_en_prestamo = (cantidad_dinero_prestamo*(((1+(interes*0.01))**meses)))
  return dinero_en_prestamo  #se definio la variable para calcular el valor del prestamo


if __name__ == "__main__":
  cantidad_dinero_prestamo = float(input("Ingresa el dinero que deseas que te presten en pesos:"))
  interes = float(input("Ingresa el interes del prestamos:"))
  meses = float(input("Tiempo en el que quieres pagarlo:"))
  prestamo_ = prestamo(cantidad_dinero_prestamo, interes, meses)
  print("El valor del prestamo sera de " +str(prestamo_)+ " pesos, solicitando un dinero total de " +str(cantidad_dinero_prestamo)+ " con un interes de " + str(interes)+ " en un plazo de " +str(meses)+ " meses")
  #codigo if que determina el valor del prestamo
``````

Ejemplo con lambda 

```
# EJEMPLO 3, PUNTO 5, RETO 6  LAMBDA
if __name__ == "__main__":
  cantidad_dinero_prestamo = float(input("Ingresa el dinero que deseas que te presten en pesos:"))
  interes = float(input("Ingresa el interes del prestamos:"))
  meses = float(input("Tiempo en el que quieres pagarlo:"))
  vol = (lambda cantidad_dinero_prestamo, interes, meses: (cantidad_dinero_prestamo*(((1+(interes*0.01)))**meses)))(cantidad_dinero_prestamo, interes, meses)
  print("El valor del prestamo sera de " +str(prestamo_)+ " pesos, solicitando un dinero total de " +str(cantidad_dinero_prestamo)+ " con un interes de " + str(interes)+ " en un plazo de " +str(meses)+ " meses")
```

### PUNTO 2

De los retos anteriores selecione 3 funciones y escribalas con argumentos no definidos (*args)

##### EJEMPLO 1

Sin args

```
# Ejemplo punto 3, reto 6, peso 5 sin args*
masa_gina: int =6
masa_galo: int=7
masa_poll: int=1

#Se definieron las masas de las gallinas, gallos, pollitos, como constantes

import math as m #importar libreria math

def carne_(gallina:float, gallo:float, pollitos:float) -> float:
  c_carne = (gallina*masa_gina + gallo*masa_galo + pollitos*masa_poll)
  return c_carne  #se definio la variable de cantidad de carne


if __name__ == "__main__":
  gallina = float(input("Cantidad de gallinas:"))
  gallo = float(input("Cantidad de gallos:"))
  pollitos = float(input("Cantidad de pollitos:"))
  carne_total = carne_(gallina, gallo, pollitos)
  print("La cantidad de carne es " + str(carne_total)+ " kilos") #se puso condicional if que defina las variables con teclado y me imprima la cantidad total de carne
```

Con args

```
# Ejemplo punto 7, taller 1, promedio 5 números con args*
def peso_t(*args)-> int:
  peso = (6*gallina)+(7*gallo)+(pollo)
  return peso

if __name__ == "__main__":
  gallina = int(input("Ingrese numero de gallinas: "))
  gallo = int(input("Ingrese numero de gallos: "))
  pollo = int(input("Ingrese numero de pollos: "))
  print("El promedio de los cinco números es " + str(peso_t(gallina, gallo, pollo))+ " kilos")
```

##### EJEMPLO 2

Escriba un programa que pida 5 números reales y calcule las siguientes operaciones:

El promedio

Sin args

```
# Ejemplo punto 7, taller 1, promedio 5 números sin args*
def numeros(numero_1:float, numero_2:float, numero_3:float, numero_4:float, numero_5: float) -> float:
  promedio = ((numero_1 + numero_2 + numero_3 + numero_4 + numero_5)/5)
  return promedio  #se definio la variable para calcular el promedio

if __name__ == "__main__":
  numero_1 = float(input("Ingresa el número 1:"))
  numero_2 = float(input("Ingresa el número 2:"))
  numero_3 = float(input("Ingresa el número 3:"))
  numero_4 = float(input("Ingresa el número 4:"))
  numero_5 = float(input("Ingresa el número 5:"))
  prom = numeros(numero_1, numero_2, numero_3, numero_4, numero_5) 
  print("El promedio de los 5 numeros es " +str(prom))
```

Con args

```
# Ejemplo punto 7, taller 1, promedio 5 números con args*
def prom_numeros(*args)-> int:
  suma : int = 0
  n : int = 0
  for num in args:
    suma +=  num
    n += 1
  suma = suma/n
  return suma

if __name__ == "__main__":
  a = int(input("Ingrese numero a: "))
  b = int(input("Ingrese numero b: "))
  c = int(input("Ingrese numero c: "))
  d = int(input("Ingrese numero d: "))
  e = int(input("Ingrese numero e: "))
  print("El promedio de los cinco números es " + str(prom_numeros(a, b, c, d, e)))
```

##### EJEMPLO 3

Escriba un programa que pida 5 números reales y calcule las siguientes operaciones:

El promedio multiplicativo (multilplica todos y luego calcula la raíz de la cantidad de operandos)

Sin args

```
# Ejemplo punto 7, taller 1, promedio multiplicativo 5 números sin args*
def numeros_(numero_1:float, numero_2:float, numero_3:float, numero_4:float, numero_5: float) -> float:
    promedio_multiplicativo = ((numero_1*numero_2*numero_3*numero_4*numero_5)**0.2)
    return promedio_multiplicativo #se definio la variable para calcular el promedio multiplicativo
if __name__ == "__main__":
  numero_1 = float(input("Ingresa el número 1:"))
  numero_2 = float(input("Ingresa el número 2:"))
  numero_3 = float(input("Ingresa el número 3:"))
  numero_4 = float(input("Ingresa el número 4:"))
  numero_5 = float(input("Ingresa el número 5:"))
  prom_mult = numeros_(numero_1, numero_2, numero_3, numero_4, numero_5) 
  print("El promedio multiplicativo de los 5 números es " +str(prom_mult))
```

Con args

```
# Ejemplo punto 7, taller 1, promedio 5 números con args*
def promult_numeros(*args)-> int:
  mult : int = 1
  n : int = 0
  for num in args:
    mult *=  num
    n += 1
  mult = mult**(1/n)
  return mult

if __name__ == "__main__":
  a = int(input("Ingrese numero a: "))
  b = int(input("Ingrese numero b: "))
  c = int(input("Ingrese numero c: "))
  d = int(input("Ingrese numero d: "))
  e = int(input("Ingrese numero e: "))
  print("El promedio de los cinco números es " + str(promult_numeros(a, b, c, d, e)))
```

### PUNTO 3

Escriba una función recursiva para calcular la operación de la potencia.

Para este punto usamos la función recursiva en la que se llame a si misma  y multiplique la base por si misma, el número de veces que se multiplicara la base la determinara el exponente, ademas establecemos algunas condiciones basicas siguiendo las reglas de la potenciación, como por ejemplo si la base es 1, sea cual sea el exponente el resultado sera 1.

```
#Punto 3
def potencia_num(bas, exp):
  if exp == 0:
    return 1
  elif exp == 1:
    return bas
  elif bas == 1:
    return bas
  else:
    return bas * potencia_num(bas, exp - 1)

if __name__ == "__main__":
  exp = int(input("Ingrese la potencia: "))
  bas = float(input("Ingrese la base: "))
  potencia = potencia_num(bas, exp)
  print("Si elevamos "  +str(bas)+  " a " + str(exp) + " es igual a " + str(potencia))
```

### PUNTO 4

Utilice la siguiente plantilla de code para contar el tiempo:

Para esto iniciamos importnado la libre time, y con un while que siempre estara corriendo, y una variable igual a 1. dentro del while utilizamos la funcion que cuenta el tiempo que se demora algo en interar, dentro de ese cajon introducimos toda la función de Fibonacci, en el que el número inicial sera igual a la varibale fuera del ciclo. Posterior a todo esto habar un condicional if en el que si el tiempo que se demora en iterar es mayor a 10, haga break el ciclo e imprima el valor que supere los 10 segundos y advierta al usuario que apartir de ahi en adelante el tiempo de ejecución sera considerable. EN caso de no cumplirse le sume uno a la varible externa para que se repita el ciclo una y otra vez

```
import time
bandera = True
a : int = 1
while bandera == True:
  start_time = time.time()
  def fiboRecursivo(n : int )-> int:
    if n <=1:
      # caso base
      return 1
    else:
      # condicion
      return fiboRecursivo(n-1)+fiboRecursivo(n-2)  

  if __name__ == "__main__":
    num = a
    serieFibo = fiboRecursivo(num)
    end_time = time.time()
    timer = end_time - start_time

  if timer > 10.0:
    break
  else:
    a=a+1 
    #print("La serie de Fibonacci hasta " + str(num) + " es " + str(serieFibo))  
    #print("Su tiempo de ejecución fue de +str(timer)) Estos dos por si quires analizar cada tiempo
print("La serie de Fibonacci hasta " + str(num) + " es " + str(serieFibo))
print("A partir de aqui considerar tiempo considerable")
print("Su tiempo de ejecución fue de : " +str(timer))
```

### PUNTO 5

Crear cuenta en stackoverflow y adjuntar imagen en el repo

Adjunto foto del perfil:

<img src="img.png" width="550">

### PUNTO 6

Cosas de adultos....ir a linkedin y crear perfil....NO IMPORTA que estén iniciando, si tienen tiempo para redes poco útiles como fb, insta, o tiktok tienen tiempo para crear un perfil mamalón. Dejar enlace en el repo.

Link del linkedin: https://www.linkedin.com/in/miguel-angel-acevedo-olaya-84a7a1296/?trk=public-profile-join-page 
