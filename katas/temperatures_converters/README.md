### 1. Celem ćwiczenia jest napisanie (zaimplementowanie) dwóch funkcji, które będą konwertować temperaturę:
- pierwsza funkcja ze skali Farenheita do Celsjusza
- druga funkcja ze skali Celsjusza do Kelvina.

### 2. Jak wykonywać ćwiczenie.
Ćwiczenie jest rozbite na etapy, każdy etap składa się z małych kroków.

Wykonuj ćwiczenie w ten sposób: czytaj instrukcję i jednocześnie wykonuj kolejne kroki w PyCharmie.
Jak dojdziesz do końca etapu, to usuń cały kod z tego etapu i spróbuj zrobić ten sam etap z pamięci.
Jak jakiegoś kroku nie będziesz pamiętać to śmiało zaglądaj do instrukcji.

Kolejny etap zacznij dopiero jak będziesz w stanie zrobić cały poprzedni z pamięci.

Ćwiczenie powinno się wykonywać kilka dni z rzędu, maksymalnie 20-30 minut, niezależnie ile kroków/etapów 
uda się wykonać/zapamiętać. (20-30 minut, żeby sie nie przemęczyć i chcieć usiąść do niego następnego dnia).

Każdego dnia zaczynaj od 1 etapu (usuń kod z poprzedniego dnia).

Za każdym razem ćwiczenie powinno zajmować coraz mniej czasu i pod koniec myślę że bedzie zajmować 5-10 minut.


### Etap 1.: Konwersja z fahrenheita do celsjusza.
#### 1.1. Najpierw tworzymy zwykłą zmienną która będzie trzymała temperaturę w skali Fahrenheita:
```python
fahrenheit = 90
```
jak uruchomimy program to co się wyświetli? - nic, bo nie używamy `print`
#### 1.2. Wyliczamy stopnie w celsjuszach za pomocą formuły: od temperatury w skali Fahrenheita odjać 32 i wynik pomnożyć razy 5/9:
```python
fahrenheit = 90
celsius = (fahrenheit - 32)*5/9
```
uruchamiamy program (zielona strzałka w PyCharmie) - znowu nic się nie wydarzyło, bo nie printujemy.
#### 1.3. Dodajemy print, zeby widzieć jaki jest wynik:
```python
fahrenheit = 90
celsius = (fahrenheit - 32)*5/9
print(celsius)
```
uruchamiamy program - powinno się wyświetlić `32.(2)`

Ok, mamy działający program, teraz zmienimy ten fragment, żeby był w funkcji.


### Etap 2: Dodajemy funkcję
#### 2.1 Najpierw piszemy `def` - od słowa `define`, czyli zaczynamy definicję naszej funkcji:
```python
fahrenheit = 90
celsius = (fahrenheit - 32)*5/9
print(celsius)

def
```
jak uruchomimy program to dostaniemy błąd, bo definicja funkcji nie jest skończona

#### 2.2. Teraz trzeba napisać nazwę funkcji, użyjemy nazwy która dosyć dokładnie opisuje co funkcja robi:
`fahrenheit_to_celsius`.
```python
fahrenheit = 90
celsius = (fahrenheit - 32)*5/9
print(celsius)

def fahrenheit_to_celsius
```
podobnie jak wyżej, jak uruchomimy program to dostaniemy błąd

#### 2.3. Teraz będziemy sprawiać, że nasza funkcja będzie "przyjmować argument". Chodzi o to, że jeśli nasza funkcja ma 
przekonwertować nam jedną liczbą na drugą, to musi w jakiś sposób dostać tę pierwszą liczbę. Do tego służy argument funkcji:
```python
fahrenheit = 90
celsius = (fahrenheit - 32)*5/9
print(celsius)

def fahrenheit_to_celsius(temp_fahrenheit):
```
(Pamiętaj, żeby dodać dwukropek na końcu linijki)
tutaj dalej błąd przy uruchomieniu

#### 2.4. W tym kroku dodamy "ciało funkcji", czyli to, co funkcja ma robić - przeliczać stopnie na skalę Celsjusza.
```python
fahrenheit = 90
celsius = (fahrenheit - 32)*5/9
print(celsius)

def fahrenheit_to_celsius(temp_fahrenheit):
    celsius = (temp_fahrenheit - 32)*5/9
```
Tutaj możemy uruchomić program, pytanie co się stanie?
Po prostu wykona się to co pod koniec etapu 1., bo ciągle mamy kod z tego etapu.

#### 2.5. Usuńmy kod z 1 etapu (teraz ta sama formuła jest w "ciele funkcji" `fahrenheit_to_celsius`):
```python
def fahrenheit_to_celsius(temp_fahrenheit):
    celsius = (temp_fahrenheit - 32)*5/9
```
uruchamiamy program - nic się nie wyświetla. Dlaczego? Bo mamy tylko definicję funkcji, ale nigdzie jej nie wywołujemy.

#### 2.6. Dodamy wywołanie funkcji:
```python
def fahrenheit_to_celsius(temp_fahrenheit):
    celsius = (temp_fahrenheit - 32)*5/9

fahrenheit = 90
fahrenheit_to_celsius(fahrenheit)
```
Ok, mamy wywołanie funkcji. Uruchamiamy program. Nic się nie dzieje, bo nie mamy printa.

#### 2.7. Dodajemy printa:
```python
def fahrenheit_to_celsius(temp_fahrenheit):
    celsius = (temp_fahrenheit - 32)*5/9

fahrenheit = 90
print(fahrenheit_to_celsius(fahrenheit))
```
uruchamiamy, dostajemy `None`. To dlatego, bo zapomnieliśmy w funkcji "zwrócić" obliczonej wartości.

#### 2.8. Zwracamy celsjusze:
```python
def fahrenheit_to_celsius(temp_fahrenheit):
    celsius = (temp_fahrenheit - 32)*5/9
    return celsius


fahrenheit = 90
print(fahrenheit_to_celsius(fahrenheit))
```
uruchamiamy program, dostajemy `32.22222222...`.

### Etap 3. Input od użytkownika.
#### 3.1. Mamy wpisaną jedną wartość do przekonwertowania: `90`, zmienimy to żeby dostać wartość od użytkownika:
```python
def fahrenheit_to_celsius(temp_fahrenheit):
    celsius = (temp_fahrenheit - 32)*5/9
    return celsius


fahrenheit = input("Please enter temperature in Fahrenheit scale: ")
print(fahrenheit_to_celsius(fahrenheit))
```
uruchamiamy program, wpisujemy `90`, klikamy `enter`. Dostajemy błąd, bo zapomnieliśmy przekonwertować inputu na `int`.

#### 3.2. Konwertujemy input
```python
def fahrenheit_to_celsius(temp_fahrenheit):
    celsius = (temp_fahrenheit - 32)*5/9
    return celsius


fahrenheit = int(input("Please enter temperature in Fahrenheit scale: "))
print(fahrenheit_to_celsius(fahrenheit))
```
uruchamiamy - dostajemy `32.2222...`.
### Etap 4. Celsjusz -> kelvin.
#### 4.1 Dodajemy drugą funkcję (celsjusz -> kelvin). Tutaj już wiemy, że będzie potrzebować `def`, nazwy funkcji, oraz że powinna przyjmować argument, więc zrobimy to w jednym kroku:
```python
def fahrenheit_to_celsius(temp_fahrenheit):
    celsius = (temp_fahrenheit - 32)*5/9
    return celsius


fahrenheit = int(input("Please enter temperature in Fahrenheit scale: "))
print(fahrenheit_to_celsius(fahrenheit))

def celsius_to_kelvin(temp_celsius):
```

#### 4.2. Dodajemy formułę do konwertowania celsius -> kelvin:
```python
def fahrenheit_to_celsius(temp_fahrenheit):
    celsius = (temp_fahrenheit - 32)*5/9
    return celsius


fahrenheit = int(input("Please enter temperature in Fahrenheit scale: "))
print(fahrenheit_to_celsius(fahrenheit))


def celsius_to_kelvin(temp_celsius):
    temp_kelvin = temp_celsius + 273.15
    return temp_kelvin
```

#### 4.3. Teraz zanim wywołamy nową funkcję, to potrzebujemy zmienną, która będzie trzymać wynik poprzedniej funkcji.
Zamiast "printować" wynik funkcji, dodamy zmienną i ją będziemy "printować":
```python
def fahrenheit_to_celsius(temp_fahrenheit):
    celsius = (temp_fahrenheit - 32)*5/9
    return celsius


fahrenheit = int(input("Please enter temperature in Fahrenheit scale: "))
celsius = fahrenheit_to_celsius(fahrenheit)
print(celsius)


def celsius_to_kelvin(temp_celsius):
    temp_kelvin = temp_celsius + 273.15
    return temp_kelvin
```

#### 4.4. Wywołanie nowej funkcji i wyświetlanie zwracanej przez nią wartości:
```python
def fahrenheit_to_celsius(temp_fahrenheit):
    celsius = (temp_fahrenheit - 32)*5/9
    return celsius


fahrenheit = int(input("Please enter temperature in Fahrenheit scale: "))
celsius = fahrenheit_to_celsius(fahrenheit)
print(celsius)


def celsius_to_kelvin(temp_celsius):
    temp_kelvin = temp_celsius + 273.15
    return temp_kelvin

kelvin = celsius_to_kelvin(celsius)
print(kelvin)
```

#### 4.5. Teraz dodamy bardziej opisowe komunikaty (usuniemy stare "printy", żeby nie zaśmiecały):
```python
def fahrenheit_to_celsius(temp_fahrenheit):
    celsius = (temp_fahrenheit - 32)*5/9
    return celsius


fahrenheit = int(input("Please enter temperature in Fahrenheit scale: "))
celsius = fahrenheit_to_celsius(fahrenheit)


def celsius_to_kelvin(temp_celsius):
    temp_kelvin = temp_celsius + 273.15
    return temp_kelvin

kelvin = celsius_to_kelvin(celsius)

print(f"{fahrenheit} fahrenheit is: {celsius} in Celsius scale, or {kelvin} in Kelvin scale")
```
#### 4.6. Przeniesiemy definicje funkcji na samą górę, żeby definicje funkcji były w jednym miejscu a ich wywoływania w drugim.

```python
def fahrenheit_to_celsius(temp_fahrenheit):
    celsius = (temp_fahrenheit - 32)*5/9
    return celsius


def celsius_to_kelvin(temp_celsius):
    temp_kelvin = temp_celsius + 273.15
    return temp_kelvin

fahrenheit = int(input("Please enter temperature in Fahrenheit scale: "))
celsius = fahrenheit_to_celsius(fahrenheit)
kelvin = celsius_to_kelvin(celsius)

print(f"{fahrenheit} fahrenheit is: {celsius} in Celsius scale, or {kelvin} in Kelvin scale")
```

Koniec