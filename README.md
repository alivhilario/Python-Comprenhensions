# Python-Comprenhensions
<div><h2>Python Zen</h2></div>
<div><h3>Sets</h3></div>
  -Sets items are unordered, unchangeable, and do not allow duplicate values.
  
```python
#input
   #No DUPLICATE!!
  setCountries = {'col', 'mex', 'bol','col'}
  print(setCountries)
  print(type(setCountries))

  setNumbers = {1,2,3,4,4,6,7,7,}
  print(setNumbers)
#Output
  {'col', 'mex', 'bol'}
  <class 'set'>
  {1, 2, 3, 4, 6, 7}

  ```

-Different Types✅✅

```python
  setTypes = {11,'hey', False, 23.55}
  print(setTypes)
  ```
-A set in set!
```python
#input
  setFromString = set('Hey')
  print(setFromString)
#Output
  {'e', 'y', 'H'}
  ```
-Sets in Tuples
-A tuple always between braces 
```python
#input
  setFromTuples = set(('abd', 'cde', 'fgh', 'as', 'cdf'))
  print(setFromTuples)

#Output
  {'fgh', 'cdf', 'cde', 'as', 'abd'}
  ```
Ordering a list as a Set
```python
#input
  numbers = [1, 2, 2, 4, 5, 2, 1, 9, 9, 10]
  setNumbers = set(numbers)
  print(setNumbers)
  uniqueNumbers = list(setNumbers)
  print(uniqueNumbers)
#Output
  {1, 2, 3, 4, 5, 6, 7, 8, 9, 10}
  [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
  ```
<h2>Modifiying "Sets"</h2>

```python
#input
  setCountries = {'col', 'mex', 'bol','col'}
  size = len(setCountries)
  print(size)

  print('col' in setCountries)
  print('pe' in setCountries)
  
#Output
  3
  True
  False
  ```

-add
```python
#input
  setCountries.add('pe')
  print(setCountries)
  setCountries.add('pe')
  print(setCountries)
#Output
  {'pe', 'col', 'bol', 'mex'}
  {'pe', 'col', 'bol', 'mex'}
  ```
-update
```python
#input
  setCountries.update({'arg', 'ecu', 'pe'})
  print(setCountries)
#Output
  {'pe', 'arg', 'col', 'bol', 'ecu', 'mex'}
  ```
-remove
```python
#input
  set_countries.remove('col')
  print(set_countries)
  
  set_countries.remove('ar')
  set_countries.discard('arg')
  print(set_countries)
  set_countries.add('arg')
  print(set_countries)
  set_countries.clear()
  print(set_countries)
  print(len(set_countries))
#Output
  {'bol', 'ecua', 'pe', 'mex', 'ar'}
  {'bol', 'ecua', 'pe', 'mex'}
  {'bol', 'ecua', 'pe', 'arg', 'mex'}
  set()
  0

  ```
-Sets:
-UNION
```python
#input
  setA = {'col', 'mex', 'bol'}
  setB = {'pe', 'bol'}
  
  setC = setA.union(setB)
  print(setC)
  print(setA | setB)
#Output
  {'bol', 'col', 'pe', 'mex'}
  {'bol', 'col', 'pe', 'mex'}
  ```
INTERSECTION
```python
#input
  setC = setA.intersection(setB)
  print(setC)
  print(setA & setB)
  
#Output
  {'bol'}
  {'bol'}
  ```
Difference:
  Removemos los elementos del elemento B del A
```python
#input
  setC = setA.difference(setB)
  print(setC)
  print(setA - setB)
#Output
  {'col', 'mex'}
  {'col', 'mex'}
  ```
symmetric difference
  Union of elements without the common.
```python
#input
  setC = setA.symmetric_difference(setB)
  print(setC)
  print(setA ^ setB)
#Output
  {'pe', 'col', 'mex'}
  {'pe', 'col', 'mex'}
  ```
<h3>List Comprehension</h3>

-Normal Way
```python
#input
numbers = []
for e in range(1, 11):
numbers.append(e)

print(numbers)

#Output
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
  ```
-2 lines of code
```python
#input
numbersV2 = [element for element in range (1,11)]
print(numbersV2)
#Output
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

  ```
-Using a list
```python
#input
numbersV3 = list(range(1,11))
print(numbersV3)
#Output
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
  ```
-Element / for element in iterable 
```python
#input
numbersV4 = [e * 2 for e in range (1,11)]
#Output
[2, 4, 6, 8, 10, 12, 14, 16, 18, 20]
  ```
Element / for element in iterable if condition
```python
#input
numbersV5 = [e * 2 for e in range (1,11) if e % 2 == 0]
print(numbersV5)
#Output
[4, 8, 12, 16, 20]
  ```
<h3>Diccionaries</h3>
-Element / for element in iterable if condition

```python
#input
dict = {}
for i in range (1,5):
  dict[i] = i * 2
print(dict)

#short way
dicV2 = {i: i * 2 for i in range(1,5)}
print(dicV2)
#Output
{1: 2, 2: 4, 3: 6, 4: 8}
{1: 2, 2: 4, 3: 6, 4: 8}
  ```

Random 
```python
#input
import random 
countries = ['col', 'mex', 'bol', 'pe']
population = {}
for c in countries:
  population[c] = random.randint(1,100)
print(population)
#Output
{'col': 82, 'mex': 51, 'bol': 98, 'pe': 31}
  ```
```python
#input
populationV2 = {c: random.randint(1,100) for c in countries}
#Output
{'col': 21, 'mex': 26, 'bol': 88, 'pe': 90}
  ```
Using ZIP:
-Iterable objects that will be joined together
```python
#input
names = ['nico', 'zule', 'santi']
ages = [12, 56, 98]

print(list(zip(names, ages)))
newDict = {name: age for (name, age) in zip(names, ages)}
print(newDict)

#Output
[('nico', 12), ('zule', 56), ('santi', 98)]
{'nico': 12, 'zule': 56, 'santi': 98}
  ```
<h2>Diccionary comprenhention</h2>

```python
#input
import random
countries = ['col', 'mex', 'bol', 'pe']
population = {country: random.randint(1, 100) for country in countries}
print(population)

result = {country: population for (country, population) in population.items() if population > 20}
print(result)
#Output
{'col': 79, 'mex': 90, 'bol': 47, 'pe': 74}
{'col': 79, 'mex': 90, 'bol': 47, 'pe': 74}
  ```
```python
#input
text = 'Hey, I am Nicolas'
unique = {c: c.upper() for c in text if c in 'aeiou'}
print(unique)
#Output
{'e': 'E', 'a': 'A', 'i': 'I', 'o': 'O'}
  ```
<h3>List vs Tuples vs Sets</h3>

- List can be; ORDERED, CHANGEBLE, ALLOW DUPLICATES values, items has an INDEX. if you add items must be placed at the end of the list.
- Tuples; can not be MODIFIED.
- Sets: Can be MODIFIED; remove or add new items, UNORDER; not referred as KEY or INDEX, No DUPLICATES, UNCHANGEABLE.  

## Functions
```python
#input
def sum (a,b):
  print(a + b) 
sum(4,6)
 
#Output
10
  ```
```python
#input
def sum_with_range(min, max):
  sum = 0
  for x in range(min, max):
    sum += x
  return sum
result = sum_with_range(1, 100)
print(result)
#Output
4950
  ```
### Return ↩️
```python
#input
def findVolume(lenght=20, width=7, depth=9):
  return lenght * width * depth, width, 'hey'

result = findVolume(width=5)
print(result[1])
result,width, text = findVolume(width=5)
print(result)
print(width)
print(text)
#Output
5
900
5
hey
  ```
### Scope 
```python
#input
price = 100 #GLOBAL
def increment():
  price = 400
  result = price * 100
  print(price)
  return(result)
print(price, ' first')
increment()
print(price, ' second')
#Output
100  first
400
100  second
  ```
### Game using functions
```python
#input
import random

#1st function
def choose_options():
  options = ('piedra', 'papel', 'tijera')
  user_option = input('piedra, papel o tijera => ')
  user_option = user_option.lower()

  if not user_option in options:
    print('esa opcion no es valida')
    # continue
    return None, None

  computer_option = random.choice(options)

  print('User option =>', user_option)
  print('Computer option =>', computer_option)
  return user_option, computer_option

#2nd function
def check_rules(user_option, computer_option, user_wins, computer_wins):
  if user_option == computer_option:
    print('Empate!')
  elif user_option == 'piedra':
    if computer_option == 'tijera':
      print('piedra gana a tijera')
      print('user gano!')
      user_wins += 1
    else:
      print('Papel gana a piedra')
      print('computer gano!')
      computer_wins += 1
  elif user_option == 'papel':
    if computer_option == 'piedra':
      print('papel gana a piedra')
      print('user gano')
      user_wins += 1
    else:
      print('tijera gana a papel')
      print('computer gano!')
      computer_wins += 1
  elif user_option == 'tijera':
    if computer_option == 'papel':
      print('tijera gana a papel')
      print('user gano!')
      user_wins += 1
    else:
      print('piedra gana a tijera')
      print('computer gano!')
      computer_wins += 1
  return user_wins, computer_wins

#3rd function
def run_game():
  computer_wins = 0
  user_wins = 0  
  rounds = 1
  while True:
    print('*' * 10)
    print('ROUND', rounds)
    print('*' * 10)

    print('computer_wins', computer_wins)
    print('user_wins', user_wins)
    rounds += 1

    user_option, computer_option = choose_options()
    user_wins, computer_wins = check_rules(user_option, computer_option, user_wins, computer_wins)

    if computer_wins == 2:
      print('El ganador es la computadora')
      break

    if user_wins == 2:
      print('El ganador es el usuario')
      break

run_game()
#Output
  ```
### Small challenge
```python
#input
def message_creator(text):
   # Escribe tu solución 👇

   respuestas = {'computadora' : "Con mi computadora puedo programar usando Python", 
                    'celular' : "En mi celular puedo aprender usando la app de Platzi",
                    'cable' : "¡Hay un cable en mi bota!"}

   if text in respuestas.keys(): 
      return respuestas[text]
   else: 
      return 'Artículo no encontrado'

text = 'computadora'
response = message_creator(text)
print(response)

#otherwise
def message_creator(text):
  messages = {
      'computadora': '"Con mi computadora puedo programar usando Python"',
      'celular': '"En mi celular puedo aprender usando la app de Platzi"',
      'cable': '"¡Hay un cable en mi bota!"'
  }

  return messages.get(text, "Artículo no encontrado")

text = 'celular'
response = message_creator(text)
print(response)
def message_creator(text):
  ```
## Lambda
```python
#input
def increment(x):
  return x + 1

result = increment(10)
print(result)

# lambda function
incrementV2 = lambda x : x +  1
result = incrementV2(20)
print(result)
# lambda function with 2 parameters
full_name = lambda name, last_name: f'Full name is {name.title()} {last_name.title()}'
text = full_name('nicolas', 'perez casas')
print(text)

#Output
11
21
Full name is Nicolas Perez Casas

  ```
## Higher Order Function

```python
#input
def increment(x):
  return x + 1
#replacing the function increment with lambda
increment_v2 = lambda x : x + 1


#replace the function high_ord_func with lambda
def highOrderFuntion(x, func):
  return x + func(x)
result = highOrderFuntion(2, increment)
print(result)

hof = lambda x, func: x + func(x)
result = hof(2, increment_v2)
print(result)
#There is no need to use the name of the function, because it is already defined
result = hof(2, lambda x: x + 2)
print(result)
result = hof(2, lambda x: x * 5)
print(result)

#Output
5
5
6
12
  ```
### Map
```python
#input
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
numbers_v2 = []
for i in numbers:
  numbers_v2.append(i * 5)
print('numbers_v2 => ', numbers_v2)

numbers_v3 = list(map(lambda i: i * 2, numbers))
print('Version 3 => ',numbers_v3)

#Short way
numbers_v3 = [i * 2 for i in numbers]
print('Short way => ',numbers_v3)

#Short way with condition
numbers_v3 = [i * 2 for i in numbers if i % 2 == 0]
print('Short way with condition => ',numbers_v3)

#Short way with condition and map
numbers_v3 = list(map(lambda i: i * 2, numbers))
print('Short way with condition and map => ',numbers_v3)

#another way to use "Map"
numbers_1 = [1, 2, 3, 4]
numbers_2 = [5, 6, 7]

print('numbers_1 => ', numbers_1)
print('numbers_2 => ', numbers_2)
result = list(map(lambda x, y: x + y, numbers_1, numbers_2))
print('result => ', result)


#Output
numbers_v2 =>  [5, 10, 15, 20, 25, 30, 35, 40, 45, 50]
Version 3 =>  [2, 4, 6, 8, 10, 12, 14, 16, 18, 20]
Short way =>  [2, 4, 6, 8, 10, 12, 14, 16, 18, 20]
Short way with condition =>  [4, 8, 12, 16, 20]
Short way with condition and map =>  [2, 4, 6, 8, 10, 12, 14, 16, 18, 20]
numbers_1 =>  [1, 2, 3, 4]
numbers_2 =>  [5, 6, 7]
result =>  [6, 8, 10]

  ```
## Map and Dics
```python
#input
items = [
  {
    'product': 'camisa',
    'price': 100
  },
  {
    'product': 'pantalones',
    'price': 300
  },
  {
    'product': 'pantalones 2',
    'price': 200
  }
]

#just prices
prices = list(map(lambda item: item['price'], items))
print('The normal dic => ',items)
print(prices)
#using "List"
prices = [item['price'] for item in items]
print('prices => ',prices)
print('The normal dic => ',items)
#add tax
def add_taxes(item):  
  new_item = item.copy()
  new_item['taxes'] = new_item['price'] * .19
  return new_item
new_items = list(map(add_taxes, items))
print('new items dic => ', new_items)
print('Just normal "items! => " ', items)

#Output
The normal dic =>  [{'product': 'camisa', 'price': 100}, {'product': 'pantalones', 'price': 300}, {'product': 'pantalones 2', 'price': 200}]
[100, 300, 200]
prices =>  [100, 300, 200]
The normal dic =>  [{'product': 'camisa', 'price': 100}, {'product': 'pantalones', 'price': 300}, {'product': 'pantalones 2', 'price': 200}]
new items dic =>  [{'product': 'camisa', 'price': 100, 'taxes': 19.0}, {'product': 'pantalones', 'price': 300, 'taxes': 57.0}, {'product': 'pantalones 2', 'price': 200, 'taxes': 38.0}]
Just normal "items! => "  [{'product': 'camisa', 'price': 100}, {'product': 'pantalones', 'price': 300}, {'product': 'pantalones 2', 'price': 200}]
  ```
##Maps and inmutability
```python
#input
items = [
  {
    'product': 'camisa',
    'price': 100
  },
  {
    'product': 'pantalones',
    'price': 300
  },
  {
    'product': 'pantalones 2',
    'price': 200
  }
]

#The dicc has been modified 🚨🚨🚨🚨🚨
def add_taxes(item):
  #The error is here cus the dicc is a copy in the memory, so the changes are not reflected in the original dicc
  new_item = item.copy() #We can use the copy method to avoid this problem
  new_item['taxes'] = item['price'] * .19
  return item
new_items = list(map(add_taxes, items))
print('new list')
print(new_items)
print('old list')
print(items)

#Output
new list
[{'product': 'camisa', 'price': 100}, {'product': 'pantalones', 'price': 300}, {'product': 'pantalones 2', 'price': 200}]
old list
[{'product': 'camisa', 'price': 100}, {'product': 'pantalones', 'price': 300}, {'product': 'pantalones 2', 'price': 200}]
  ```

```python

#input
items = [
  {
    'product': 'camisa',
    'price': 100,
  },
  {
    'product': 'pantalones',
    'price': 300
  },
  {
    'product': 'pantalones 2',
    'price': 200
  }
]

def add_taxes(item):
  new_item = item.copy()
  new_item['taxes'] = new_item['price'] * .19
  return new_item

new_items = list(map(add_taxes, items))
print('New list')
print(new_items)
print('Old list')
print(items

#Output

  ```
### Little challenge
```python

#input
def multiply_numbers(numbers):
  # Escribe tu solución 👇
  result = list(map(lambda number: number * 2, numbers))
  return result  

numbers = [1, 2, 3, 4]
response = multiply_numbers(numbers)
print(response)

#Remeber you can use List !
result = [number * 2 for number in numbers]
#Output
[2, 4, 6, 8]
  ```
###Filter
```python

#input
numbers = [1,2,3,4,5,6,7,8,9,10]
new_numbers = list(filter(lambda x: x % 2 == 0, numbers))
print(new_numbers)
print(numbers) 

#Output
[2, 4, 6, 8, 10]
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
  ```

```python

#input
matches = [
  {
    'home_team': 'Bolivia',
    'away_team': 'Uruguay',
    'home_team_score': 3,
    'away_team_score': 1,
    'home_team_result': 'Win'
  },
  {
    'home_team': 'Brazil',
    'away_team': 'Mexico',
    'home_team_score': 1,
    'away_team_score': 1,
    'home_team_result': 'Draw'
  },
  {
    'home_team': 'Ecuador',
    'away_team': 'Venezuela',
    'home_team_score': 5,
    'away_team_score': 0,
    'home_team_result': 'Win'
  },
]

print(matches)
print(len(matches))

new_list = list(filter(lambda item: item['home_team_result'] == 'Win', matches))

print(new_list)
print(len(new_list))
print(matches)
print(len(matches))
# new_list = list(map(lambda item: item['home_team_result'] == 'Win
#new_list = [item['home_team]' for item in matches if item['home_team_result'] == 'Win']
#print(new_list)
#print(len(new_list))

#Output
[{'home_team': 'Bolivia', 'away_team': 'Uruguay', 'home_team_score': 3, 'away_team_score': 1, 'home_team_result': 'Win'}, {'home_team': 'Brazil', 'away_team': 'Mexico', 'home_team_score': 1, 'away_team_score': 1, 'home_team_result': 'Draw'}, {'home_team': 'Ecuador', 'away_team': 'Venezuela', 'home_team_score': 5, 'away_team_score': 0, 'home_team_result': 'Win'}]
3
[{'home_team': 'Bolivia', 'away_team': 'Uruguay', 'home_team_score': 3, 'away_team_score': 1, 'home_team_result': 'Win'}, {'home_team': 'Ecuador', 'away_team': 'Venezuela', 'home_team_score': 5, 'away_team_score': 0, 'home_team_result': 'Win'}]
2
#There is no changes 
[{'home_team': 'Bolivia', 'away_team': 'Uruguay', 'home_team_score': 3, 'away_team_score': 1, 'home_team_result': 'Win'}, {'home_team': 'Brazil', 'away_team': 'Mexico', 'home_team_score': 1, 'away_team_score': 1, 'home_team_result': 'Draw'}, {'home_team': 'Ecuador', 'away_team': 'Venezuela', 'home_team_score': 5, 'away_team_score': 0, 'home_team_result': 'Win'}]
3

  ```
###little challenge
```python

#input
def filter_by_length(words):
   # Escribe tu solución 👇
   #new_list = list(filter(lambda item: len(item) >= 4, words))
    new_list = [item for item in words if len(item) >= 4]
    return new_list

words = ['amor', 'sol', 'piedra', 'día']
response = filter_by_length(words)
print(response)
#Output
['amor', 'piedra']
  ```
##Reduce
```python

#input
import functools

numbers = [1, 2, 3, 4]

result = functools.reduce(lambda counter, item: counter + item, numbers)

print(result)

#Output
10
  ```
##Modules
```python

#input
import sys
print(sys.path)

#Output
['/home/runner/Python', '/nix/store/icx0zbk2r2qrpnqpd41q4h4xzr856d4f-python3.10-setuptools-67.4.0/lib/python3.10/site-packages', '/nix/store/xf54733x4chbawkh1qvy9i1i4mlscy1c-python3-3.10.11/lib/python3.10', '/home/runner/Python/.pythonlibs/lib/python3.10/site-packages', '/nix/store/s4cbcvnm0miclkjwj6g8fxcn8fgb78s1-python3.10-pip-21.2.dev0/lib/python3.10/site-packages', '/nix/store/xf54733x4chbawkh1qvy9i1i4mlscy1c-python3-3.10.11/lib/python310.zip', '/nix/store/xf54733x4chbawkh1qvy9i1i4mlscy1c-python3-3.10.11/lib/python3.10/lib-dynload', '/nix/store/xf54733x4chbawkh1qvy9i1i4mlscy1c-python3-3.10.11/lib/python3.10/site-packages']

#input
import re 
text = 'Mi numero de telefono es 311 123 121, el codigo del pais es 57, mi numero de la suerte es 3'
result = re.findall('[0-9]+', text)
print(result)

#output
['311', '123', '121', '57', '3']

#input
import time
timestamp = time.time()
local = time.localtime()
result = time.asctime(local)
print(result)

#output
Wed Feb 14 15:45:34 2024

#input
import collections 
numbers = [1,1,2,1,2,1,4,5,3,3,21]
counter = collections.Counter(numbers)
print(counter)
#Output
Counter({1: 4, 2: 2, 3: 2, 4: 1, 5: 1, 21: 1})
  ```
###Own Modules

```python
#in folder: app two files:
#In file mod.py
#input
def get_population():
  keys = ['col','bol']
  values = [300,400]
  return keys, values

def population_by_country(data, country):
  result = list(filter(lambda item: item['Country'] == country, data))
  return result
-----------------------------
#Then in file: main.py:
#input
import mod 

keys, values = mod.get_population()
print(keys, values)

data = [
  {
    'Country': 'Colombia',
    'Population': 500
  },
  {
    'Country': 'Bolivia',
    'Population': 300
  }
]

country = input('Type Country => ')
result = mod.population_by_country(data, country)
print(result)

#output
~/Python$ python app/main.py
['col', 'bol'] [300, 400]
Type Country => Colombia
[{'Country': 'Colombia', 'Population': 500}]
```
###Running scripts
Cuando utilizamos name == 'main' estamos dando dualidad a cierta función para que sea ejecutada en dos archivos distintos.

Para ello debemos tener en cuenta que su uso esta catalogado de dos maneras:

Se puede ejecutar el archivo como un script.
Importando el codding de un archivo a otro archivo python.
Para Python, es independiente cual de las dos formas estemos utilizando el código, ya que python define una variable especial llamada __name__ la cual contiene un string y cuyo resultado dependerá de la forma en como sea usada.

Como en el ejemplo, se observa que el primer archivo que denominamos main.py.

main.py
```python
#input
import utils

keys, values = utils.get_population()
print(keys, values)

data = [
  {
    'country': 'Colombia',
    'Population': 500
  },
  {
    'country': 'Peru',
    'Population': 250
  },
  {
    'country': 'Argentina',
    'Population': 350
  }
]

def run():
  keys, values = utils.get_population()
  print(keys, values)

  country = input('Digite el país: ')
  result = utils.population_by_countrie(data, country)
  print(result)

if __name__ == '__main__':
  run()
```

```python
#input
#output
```

```python
#input
#output
```

```python
#input
#output
```

```python
#input
#output
```

```python
#input
#output
```
