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
```python
#input

#Output
  ```
