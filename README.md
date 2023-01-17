### 0. PyCharm i Python są ściągnięte i zainstalowane.


### 1. Tworzymy nowy projekt

### 2. Uruchamiamy konsolę Pythona:
![python_console1](https://user-images.githubusercontent.com/20053756/212992486-5a4abfa8-0ebf-4ac6-9bbc-64c08980a8d8.png)
albo na pasku Tools/Python or  Debug Console
### 3. ćwiczenia (wszystko co jest zaznaczone w ten sposób: `3 + 3` w konsolę Pythona (bez komentarzy)):
#### 'matematyka i takie tam'

1. `2 + 2`
2. `3 * 2`
3. `5**2`
4. `5**3`
5. `2 + 6**2` 
6. generalnie wniosek jest taki, ze Python potrafi wykonywać matematyczne operacje
7. `(2+6)**2` - nawiasy też działają
8. `10/2`
9. `10/1`
10. `10/0` - ERROR **ZeroDivisionError: division by zero**
11. `11/3`
12. `11//3` (dwa znaki dzielenia), zwróci 3 (czyli dwa znaki dzielenia zostawiają tylko część całkowitą wyniku)
13. `21%5` - zwraca tylko resztę z dzielenia
14. `100%5`
### wyrazy (znane jako stringi (od angielskiego string of characters, czyli łańuch znaków)):
1. `'abc'`
2. `'łódź'` - rozumie polskie znaki
3. `'😀'` - rozumie emotikonki
4. `'abc' + '.txt'` - potrafi dodawać wyrazy
5. `'Cześć' + 'Python'` - trzeba uważać na spacje
6. `'abc '*10` - potrafi 'mnożyć' wyrazy (bonus: twórcy Pythona uznali, że skoro mnożenie np. `3 * 3 = 3 + 3 + 3`, to `'abc' * 3 = 'abc' + 'abc' + 'abc'`, stąd można 'mnożyć' wyrazy)
7. `'abc' + 3` - ERROR **TypeError: can only concatenate str (not "int") to str** (po prostu twórcy Pythona uznali, że w przeciwieństwie do mnożenia, dodawanie wyrazów do liczb nie ma sensu)
8. `str(3)` 
9. `3`

jaka jest różnica między wynikiem **8.** a **9.**? - różnica jest subtelna, **8.** ma cudzysłów, **9.** nie ma
czyli **8.** jest rozumiane jako wyraz (string) a **9.** jako liczba

10. `'abc' + str(3)` - teraz już dodajemy wyraz do wyrazu 
11. `'abc' + '3'` - tak też można, bo cyfra `3` jest w cudzysłowie
### liczby z przecinkiem (`float`)
1. `10/2`
2. `2+3`

różnica jest taka, że raz mamy `5.0` a raz bez zera `5`, bo Python nie traktuje ich tak samo (powód nie jest trywialny i nie ma co na razie tracic na to czasu, kiedyś do tego wrócimy)

3. `'abc '* 5.0` - ERROR **TypeError: can't multiply sequence by non-int of type 'float'**

podsumujmy jakie rodzaje danych rozróżnia Python:
- `int` - liczby całkowite (ang. integers)
- `float` - liczby z przecinkiem (dziwna nazwa, powód jak wyżej było wspomniane nie jest trywialny i kiedyś do tego wrócimy)
- `str` - wyrazy (ang. string, w pythonie )

### zmienne
1. `name = 'James'`
2. `age = 35`
3. `'Cześć' + name`
4. `'twój wiek: ' + age` - ERROR
5. `'twój wiek: ' + str(age)` - konwertujemy liczbę (`int`) na wyraz (`str`)
6. `age` - dalej `int`
7. `age = str(age)` - konwertujemy zmienną `age` do `str`
8. `age` - teraz już w zmiennej `age` jest str
10. `number_1 = 10`
11. `number_2 = 20`
12. `sum_of_numbers = number_1 + number_2`
13. `sum_of_numbers`
14. `average_of_numbers = sum_of_numbers/2`
15. `average_of_numbers`
16. `'average_of_numbers'` - proszę zwrócić uwagę na cudzysłów!
17. `average_of_number` - ERROR - proszę zwrócić uwagę na literówkę - brak litery 's' na końcu

dobra, co tu się dzieje? w **14.** mówimy Pythonowi "pokaż co jest w zmiennej `average_of_numbers`, dlatego zwraca nam liczbę
w **15.** mówimy Pythonowi "zwróć mi wyraz 'average_of_numbers'", ponieważ `average_of_numbers` jest objęte w cudzysłów!
a **16.** Python rozumie jako "pokaż co się znajduje w zmiennej `average_of_number`, tylko że zrobiliśmy literówkę, więc taka zmienna nie istenieje! dlatego błąd jaki wyświetli Python brzmi **NameError: name 'average_of_number' is not defined**

17. `average_of_numbers = 100`
18. `average_of_numbers`
19. `average_of_numbers = 'jakis wyraz'`
20. `average_of_numbers`

jak widać, na początku `average_of_numbers` to był `float` (liczba z przecinkiem), a w **17.** powiedzieliśmy Pythonowi "włóż do zmiennej `average_of_numbers` liczbę `100` (która jest typu `int`), potem włożyliśmy do niej wyraz `'jakis wyraz'`

### nazewnictwo zmiennych
1. `name = 'James'`
2. `naMe = 'Arthur'`
3. `name`
4. `naMe` - czyli wielkość liter robi różnicę
5. `_age = 41` - można zacząć od znaku `_`
6. `name_1 = 'James'` - może zawierać cyfry
7. `1name = 'James'` - ERROR - ale nie na pierwszy miejscu
8. `name-of-person = 'James'` - ERROR - nie może zawierać myślinika `-`
9. `name_of_person = 'James'` - ale może zawierać `_`



## Pierwszy program
#### Na razie zostawiamy konsolę Pythona i będziemy pisać w pliku.
![image](https://user-images.githubusercontent.com/20053756/213012720-b409902a-a17e-4401-bb90-aca44579a8b7.png)

#### skopiuj i wklej ten kod do PyCharma, potem wciśnij Shift+F10 (albo kliknij na zieloną strzałkę): ![image](https://user-images.githubusercontent.com/20053756/213014317-d1b11d0f-53d3-47c9-b313-c73a245f9b7a.png)


```python
print('Hello, world!')
```
teraz automatycznie powinno otworzyć się okno "Run" z tekstem "Hello, world!": ![image](https://user-images.githubusercontent.com/20053756/213014709-12bc2317-2d60-48f3-a940-a1fbb6325afa.png)

teraz dodajmy ten fragment i wciśnijmy zielony strzałkę 
```python
name = input()
print(f"Witaj {name}")
```
powinno wyświetlić się znowu okno "Run", teraz trzeba tam kliknąć myszką i wpisać swoje imię
![image](https://user-images.githubusercontent.com/20053756/213017660-5a489df2-ffa9-41b6-a261-b17ef65ff63e.png)
![image](https://user-images.githubusercontent.com/20053756/213017859-c31a12bb-9e05-48f9-be6a-a219480c9235.png)

teraz dodajmy ten fragment, uruchamiamy program, wpisujemy swoje imię:
```python
name_length = len(name)
print(f'Liczba liter w Twoim imieniu to {name_length}')
```
![image](https://user-images.githubusercontent.com/20053756/213018970-47926f17-967a-4044-ad65-30c79bec07d4.png)


### 4. na koniec usuwamy stworzony projekt w PyCharmie (usuwamy folder)
