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
  setCountries = {'col', 'mex', 'bol',col}
  size = len(setCountries)
  print(size)

  print('col' in setCountries)
  print('pe' in setCountries)
  
#Output
  3
  True
  False
  ```

```python
#input
#Output

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
```python
#input
  
#Output

  ```
```python
#input
  
#Output

  ```

