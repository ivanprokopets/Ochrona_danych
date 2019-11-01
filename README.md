# Ochrona_danych
Znajdziesz tutaj omówienie algorytmów kryptologicznych, które stanowią fundamenty zabezpieczeń.

### Etap 1 - Kryptografia historyczna
Zapoznanie się z historycznymi algorytmami kryptograficznych (m.in. szyfrem Cezara, szyfrem strumieniowym RC4) i słabościami związanymi z ich stosowaniem. Zostanie wykorzystany język skryptowy Python umożliwiający szybkie rozwiązanie nawet skomplikowanego problemu. Ten etap to wprowadzanie do tematyki trybów pracy szyfrów blokowych, a także ataków brutalnej siły.

#### Opis zadań
Informacja o zadań składających się z projektu.
Przed uruchomieniem zainstaluj biblioteki:   
`pip3 install pycrypto`
- [x] 1. Za pomocą analizy statystycznej postaraj się odszyfrować tekst zaszyfrowany algorytmem przesunięcia cyklicznego o nieznanym kluczu (crypto.rot). Szyfrowane zostały wszystkie znaki o kodach z przedziału 0-255. POMINIĘTO znak spacji.
`(ord(c) + k) % 256 if c != ' '` 
frequency taken from http://en.wikipedia.org/wiki/Letter_frequency [Kode_1](./Etap_1/1.py)
- [x] 2. Porównaj rozkłady statystyczne tekstów w dwóch różnych językach. Należy wypisać co najmniej słownik z liczbą wystąpień każdego znaku tekstu. [Kode_2](./Etap_1/2.py)
- [x] 3. Szyforwanie oraz deszyfrowanie alogorytmem Cezara. [Kode_3](./Etap_1/3.py)
- [x] 4. Procent wystąpienia znaku w tekscie. [Kode_4](./Etap_1/4.py)
- [x] 5. Napisz program przeprowadzający atak brutalnej siły na kryptogram crypto.rc4. Został on zaszyfrowany trzyznakowym kluczem `3x ['a'-'z']` [Kode_5](./Etap_1/5.py)
##### Przydatne materiały dla etapu 1
* Hasła dla Google: Cezar, ROT13, Vigenere, RC4, entropy
----------------------

### Etap 2 - Szyfrowanie blokowe
Zapoznanie z blokowymi algorytmami szyfrowania symetrycznego oraz metodami przekształcania hasła na dobry klucz kryptograficzny.

#### Opis zadań
Informacja o zadań składających się z projektu.
- [x] 1. Napisz algorytm obliczający entropię. [Kode_1](./Etap_2/1.py)
- [x] 2. Porównaj entropie tekstu naturalnego z entropia kryptogramu. [Kode_2](./Etap_2/2.py)
- [x] 3. Porównaj wynik szyfrowania w trybach ECB i CBC. Jaka jest entropia kryptogramów? [Kode_3](./Etap_2/3.py)
- [x] 4. Zaproponuj algorytm tworzenia klucza na podstawie hasła podawanego przez człowieka. [Kode_4](./Etap_2/4.py)
- [x] 5. Określ ile znaków `[a-z]` należy podać, żeby entropia hasła zbliżyła się do 256-bitowego klucza AES. [Kode_5](./Etap_2/5.py)
- [x] 6. Napisz program do ataku brutalnej siły na kryptogram przy wykorzystaniu entropii jako uniwersalnego kryterium zakończenia algorytmu. [Kode_6](./Etap_2/6.py)
- [x] 7. Atak brutalnej siły na hasło użyte do zaszyfrowania danych obrazu we800_CBC_encrypted.bmp.
Wiadomo, że hasło składa się z trzech liter `[a-z]` i że zostało przekształcone w klucz za pomocą funkcji `PBKDF2` z solą `"abc"`. Dane obrazka (bez nagłówka!) zostały zaszyfrowane za pomocą algorytmu AES w trybie CBC z `IV="a"*16`.
Znajdź hasło, używając entropii jako kryterium poprawności odszyfrowania wiadomości.[Kode_7](./Etap_2/task7.py)

##### Przydatne materiały dla etapu 2
* Hasła dla Google: DES, AES, key derivation, entropy
----------------------

### Etap 3 - Funkcje hash
Zapoznanie z algorytmów kryptograficznych funkcji jednokierunkowych (hash) do ochrony bazy haseł. Poznanie zasad ataku systematycznego przeszukiwania (brute-force) na hasła.

#### Opis zadań
Informacja o zadań składających się z projektu.
- [x] 1. Napisz program korzystający z bazy wygenerowanej przez program htpasswd. Celem programu jest sprawdzenie, czy użytkownik o podanym identyfikatorze i haśle jest w pliku bazy.
- [x] 2.Napisz program umożliwiający zmianę hasła użytkownika w bazie programu htpasswd.
- [x] 3. Napisz program umożliwiający dodawanie nowych użytkowników do bazy programu htpasswd.
- [ ] 4. Przy pomocy wywołania bibliotecznej funkcji md5() odtwórz działanie programu md5sum.
- [ ] 5. Przy pomocy wywołania bibliotecznej funkcji md5() odtwórz działanie polecenia md5sum -c, czyli kontrole spójności plików.
- [ ] 6. Korzystając z polecania time sprawdź wydajność dowolnej implementacji algorytmu łamania haseł metodą brutalnej siły i oszacuj czas maksymalny czas potrzebny do złamania haseł różnej długości i składający się z małych liter i dużych liter.
- [ ] 7. Napisz program zgadujący hasła ukryte za pomocą funkcji crypt(), przechowywane w bazie programu htpasswd. Przyjmij założenie, że hasła są trzy znakowe i składają się z samych małych liter.
- [ ] 8. Przygotuj dwa dokumenty, których funkcje skrótu trivial_hash() bedą identyczne, a treść różna. Wykorzystaj paradoks urodzinowy.
- [ ] 9. Napisz program szukający kolizji z określoną wartością funkcji skrótu trivial_hash() poprzez modyfikacje ‘białych’ znaków.
- [ ] 10. Porównaj wydajność programu “John the Ripper”, z pythonowym skryptem do łamania haseł.

##### Przydatne materiały dla etapu 3
* Hasła dla Google: brute force attack, cryptographic hash function, htpasswd, md5sum, crypt function, unix password
----------------------

