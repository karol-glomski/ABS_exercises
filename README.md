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

### liczby niecałkowite vs całkowite
1. `10/2`
2. `2+3`

różnica jest taka, że raz mamy `5.0` a raz bez zera `5`, bo Python nie traktuje ich tak samo (powód nie jest trywialny i nie ma co na razie tracic na to czasu, kiedyś do tego wrócimy)

3. `'abc '* 5.0` - ERROR **TypeError: can't multiply sequence by non-int of type 'float'**

podsumujmy jakie rodzaje danych rozróżnia Python:
- `int` - liczby całkowite (ang. integers)
- `float` - liczby z przecinkiem (dziwna nazwa, powód jak wyżej było wspomniane nie jest trywialny i kiedyś do tego wrócimy)
- `str` - wyrazy (ang. string, w pythonie )




### 4. na koniec usuwamy stworzony projekt w PyCharmie (usuwamy folder)
