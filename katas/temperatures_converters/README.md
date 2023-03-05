### 1. Celem ćwiczenia jest napisanie (zaimplementowanie) dwóch funkcji, które będą konwertować temperaturę:
- pierwsza funkcja ze skali Farenheita do Celsjusza
- druga funkcja ze skali Celsjusza do Kelvina.

### 2. Ćwiczenie jest rozbite na etapy, każdy etap składa się z małych kroków.
Wykonuj ćwiczenie w ten sposób: najpierw naucz się na pamięć małych kroków z pierwszego etapu,
potem spróbuj zrobić pierwszy etap z pamięci. Jak jakiegoś kroku nie będziesz pamiętać to śmiało zobacz
w instrukcję.

Jak zapamiętasz pierwszy etap (bez patrzenia do instrukcji), to dopiero wtedy zacznij wykonywać drugi etap.

Ćwiczenie powinno się wykonywać 20-30 minut, niezależnie ile kroków/etapów uda się wykonać.

Każdy etap zacznij dopiero jak zapamiętasz poprzedni etap.

Za każdym razem zaczynaj ćwiczenie od początku (czyli jak w poniedziałek nauczysz się pierwszego etapu i kilku kroków z
drugiego etapu, to we wtorek i tak zaczynasz od 1 etapu - z czasem będziesz robić je coraz szybciej i w te 30 minut się
wyrobisz z całym ćwiczeniem).


Etapy:
#### 1.1. Najpierw tworzymy zwykłą zmienną która będzie trzymała temperaturę w skali Fahrenheita:
```python
fahrenheit = 90
```
jak uruchomimy program to co się wyświetli? - nic, bo nie używamy `print`
#### 1.2. Wyliczamy stopnie w celsjuszach za pomocą formuły: od temperatury w skali Fahrenheita odjać 32 i wynik pomnożyć razy 5/9:
```python
fahrenheit = 90
celcius = (fahrenheit - 32)*5/9
```
uruchamiamy program (zielona strzałka w PyCharmie) - znowu nic się nie wydarzyło, bo nie printujemy.
#### 1.3. Dodajemy print, zeby widzieć jaki jest wynik:
```python
fahrenheit = 90
celcius = (fahrenheit - 32)*5/9
print(celcius)
```
uruchamiamy program - powinno się wyświetlić `32.(2)`

Ok, mamy działający program, teraz zmienimy ten fragment, żeby był w funkcji.


Etap 2: Dodajemy funkcję
#### 2.1 Najpierw piszemy `def` - od słowa `define`, czyli zaczynamy definicję naszej funkcji:
```python
fahrenheit = 90
celcius = (fahrenheit - 32)*5/9
print(celcius)

def
```
jak uruchomimy program to dostaniemy błąd, bo definicja funkcji nie jest skończona

#### 2.2. Teraz trzeba napisać nazwę funkcji, użyjemy nazwy która dosyć dokładnie opisuje co funkcja robi:
`fahrenheit_to_celcius`.
```python
fahrenheit = 90
celcius = (fahrenheit - 32)*5/9
print(celcius)

def fahrenheit_to_celcius
```
podobnie jak wyżej, jak uruchomimy program to dostaniemy błąd

#### 2.3. Teraz będziemy sprawiać, że nasza funkcja będzie "przyjmować argument". Chodzi o to, że jeśli nasza funkcja ma 
przekonwertować nam jedną liczbą na drugą, to musi w jakiś sposób dostać tę pierwszą liczbę. Do tego służy argument funkcji:
```python
fahrenheit = 90
celcius = (fahrenheit - 32)*5/9
print(celcius)

def fahrenheit_to_celcius(temp_fahrenheit):
```
(Pamiętaj, żeby dodać dwukropek na końcu linijki)
tutaj dalej błąd przy uruchomieniu

#### 2.4. W tym kroku dodamy "ciało funkcji", czyli to, co funkcja ma robić - przeliczać stopnie na skalę Celsjusza.
```python
fahrenheit = 90
celcius = (fahrenheit - 32)*5/9
print(celcius)

def fahrenheit_to_celcius(temp_fahrenheit):
    celcius = (temp_fahrenheit - 32)*5/9
```
Tutaj możemy uruchomić program, pytanie co się stanie?
Po prostu wykona się to co pod koniec etapu 1., bo ciągle mamy kod z tego etapu.

#### 2.5. Usuńmy kod z 1 etapu (teraz ta sama formuła jest w "ciele funkcji" `fahrenheit_to_celcius`):
```python
def fahrenheit_to_celcius(temp_fahrenheit):
    celcius = (temp_fahrenheit - 32)*5/9
```
uruchamiamy program - nic się nie wyświetla. Dlaczego? Bo mamy tylko definicję funkcji, ale nigdzie jej nie wywołujemy.

#### 2.6. Dodamy wywołanie funkcji:
```python
def fahrenheit_to_celcius(temp_fahrenheit):
    celcius = (temp_fahrenheit - 32)*5/9

fahrenheit = 90
fahrenheit_to_celcius(fahrenheit)
```
Ok, mamy wywołanie funkcji. Uruchamiamy program. Nic się nie dzieje, bo nie mamy printa.

#### 2.7. Dodajemy printa:
```python
def fahrenheit_to_celcius(temp_fahrenheit):
    celcius = (temp_fahrenheit - 32)*5/9

fahrenheit = 90
print(fahrenheit_to_celcius(fahrenheit))
```
uruchamiamy, dostajemy `None`. To dlatego, bo zapomnieliśmy w funkcji "zwrócić" obliczonej wartości.

#### 2.8. Zwracamy celsjusze:
```python
def fahrenheit_to_celcius(temp_fahrenheit):
    celcius = (temp_fahrenheit - 32)*5/9
    return celcius


fahrenheit = 90
print(fahrenheit_to_celcius(fahrenheit))
```
uruchamiamy program, dostajemy `32.22222222...`.

Etap 3. Input od użytkownika.
#### 3.1. Mamy wpisaną jedną wartość do przekonwertowania: `90`, zmienimy to żeby dostać wartość od użytkownika:
```python
def fahrenheit_to_celcius(temp_fahrenheit):
    celcius = (temp_fahrenheit - 32)*5/9
    return celcius


fahrenheit = input("Please enter temperature in Fahrenheit scale: ")
print(fahrenheit_to_celcius(fahrenheit))
```
uruchamiamy program, wpisujemy `90`, klikamy `enter`. Dostajemy błąd, bo zapomnieliśmy przekonwertować inputu na `int`.

#### 3.2. Konwertujemy input
```python
def fahrenheit_to_celcius(temp_fahrenheit):
    celcius = (temp_fahrenheit - 32)*5/9
    return celcius


fahrenheit = int(input("Please enter temperature in Fahrenheit scale: "))
print(fahrenheit_to_celcius(fahrenheit))
```
uruchamiamy - dostajemy `32.2222...`.

#### 4.1 Dodajemy drugą funkcję (celsjusz -> kelvin). Tutaj już wiemy, że będzie potrzebować `def`, nazwy funkcji, oraz że
powinna przyjmować argument, więc zrobimy to w jednym kroku:
```python
def fahrenheit_to_celcius(temp_fahrenheit):
    celcius = (temp_fahrenheit - 32)*5/9
    return celcius


fahrenheit = int(input("Please enter temperature in Fahrenheit scale: "))
print(fahrenheit_to_celcius(fahrenheit))

def celcius_to_kelvin(temp_celcius):
```

#### 4.2. Dodajemy formułę do konwertowania celcius -> kelvin:
```python
def fahrenheit_to_celcius(temp_fahrenheit):
    celcius = (temp_fahrenheit - 32)*5/9
    return celcius


fahrenheit = int(input("Please enter temperature in Fahrenheit scale: "))
print(fahrenheit_to_celcius(fahrenheit))


def celsius_to_kelvin(temp_celsius):
    temp_kelvin = temp_celsius + 273.15
    return temp_kelvin
```

#### 4.3. Teraz zanim wywołamy nową funkcję, to potrzebujemy zmienną, która będzie trzymać wynik poprzedniej funkcji.
Zamiast "printować" wynik funkcji, dodamy zmienną i ją będziemy "printować":
```python
def fahrenheit_to_celcius(temp_fahrenheit):
    celcius = (temp_fahrenheit - 32)*5/9
    return celcius


fahrenheit = int(input("Please enter temperature in Fahrenheit scale: "))
celcius = fahrenheit_to_celcius(fahrenheit)
print(celcius)


def celsius_to_kelvin(temp_celsius):
    temp_kelvin = temp_celsius + 273.15
    return temp_kelvin
```

#### 4.4. Wywołanie nowej funkcji i wyświetlanie zwracanej przez nią wartości:
```python
def fahrenheit_to_celcius(temp_fahrenheit):
    celcius = (temp_fahrenheit - 32)*5/9
    return celcius


fahrenheit = int(input("Please enter temperature in Fahrenheit scale: "))
celcius = fahrenheit_to_celcius(fahrenheit)
print(celcius)


def celsius_to_kelvin(temp_celsius):
    temp_kelvin = temp_celsius + 273.15
    return temp_kelvin

kelvin = celsius_to_kelvin(celcius)
print(kelvin)
```

#### 4.5. Teraz dodamy bardziej opisowe komunikaty (usuniemy stare "printy", żeby nie zaśmiecały):
```python
def fahrenheit_to_celcius(temp_fahrenheit):
    celcius = (temp_fahrenheit - 32)*5/9
    return celcius


fahrenheit = int(input("Please enter temperature in Fahrenheit scale: "))
celcius = fahrenheit_to_celcius(fahrenheit)


def celsius_to_kelvin(temp_celsius):
    temp_kelvin = temp_celsius + 273.15
    return temp_kelvin

kelvin = celsius_to_kelvin(celcius)

print(f"{fahrenheit} fahrenheit is: {celcius} in Celcius scale, or {kelvin} in Kelvin scale")
```
#### 4.6. Przeniesiemy definicje funkcji na samą górę, żeby definicje funkcji były w jednym miejscu a ich wywoływania w drugim.

```python
def fahrenheit_to_celcius(temp_fahrenheit):
    celcius = (temp_fahrenheit - 32)*5/9
    return celcius


def celsius_to_kelvin(temp_celsius):
    temp_kelvin = temp_celsius + 273.15
    return temp_kelvin

fahrenheit = int(input("Please enter temperature in Fahrenheit scale: "))
celcius = fahrenheit_to_celcius(fahrenheit)
kelvin = celsius_to_kelvin(celcius)

print(f"{fahrenheit} fahrenheit is: {celcius} in Celcius scale, or {kelvin} in Kelvin scale")
```

Koniec