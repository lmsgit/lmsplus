## Rozchód wewnętrzny (RW)

Rozchodu towaru wewnątrz firmy dokonujemy z wykorzystaniem dokumentu magazynowego RW (rozchód wewnętrzny). W ramach jednego dokumentu RW możliwe jest wydanie towaru tylko z jednego dowolnego magazynu. Należy pamiętać o nadaniu odpowiednich uprawnień dla użytkownika, który dokonuje rozchodu wewnętrznego produktów ([Uprawnienia](uprawnienia.md)).

Najczęściej dokument RW wykorzystujemy do ewidencji materiałów zużywanych na potrzeby inwestycji w infrastrukturę własną firmy lub do jej utrzymania.

Na potrzeby instrukcji zakładamy, że przyłącze do naszego klienta uległo poważnej awarii i potrzebujemy przerobić je całkowicie, co umownie potraktujemy jako działania mające na celu utrzymywanie infrastruktury własnej firmy. Potrzebujemy do tego następujących materiałów:
- kabel światłowodowy (w magazynie jest to produkt 'Światłowód Optix W-NOTKSd 1J (GJFJV) 1x9/125 ITU-T G.657A') w ilości 10 metrów,
- patchcord (w magazynie jest to produkt 'Patchcord APC G657A2') w ilości 1 sztuka,
- Router H660G (w magazynie jest to produkt 'H660G') w ilości 1 sztuka.

Produkt 'H660G' jest produktem z egzemplarzami i jest powiązany z osprzętem sieciowym. Dzięki takiej definicji po wydaniu urządzenia będziemy mogli poprzez urządzenie sieciowe stwierdzić w jakiej jest lokalizacji, a przez magazyn stwierdzić kiedy zostało wydane do montażu.

Wydanie niezbędnych materiałów musimy poddać ewidencji w magazynie używając dokumentu RW.

##### Tworzenie RW

Przed wykonaniem RW sprawdźmy stany magazynowe produktów co będzie stanowić punkt odniesienia, który na koniec pozwoli nam zobaczyć jak dokument RW wpłynął na stany magazynowe (rysunki poniżej) ([Stany magazynowe](stany_magazynowe.md)).

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-78.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-79.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-80.png)

Uruchom z menu głównego 'Magazyn-dokumenty->RW'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-81.png)

Uruchom przycisk 'Dodaj dokument'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-82.png)

Uzupełnij kolejno:
- firmę,
- magazyn główny,
- plan numeracyjny.

Uruchom 'Zapisz'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-83.png)

Wygenerowany zostanie dokument RW w stanie edycji, niezatwierdzony. Możemy teraz przystąpić do dodawania do dokumentu produktów.

##### Dodawanie produktów

###### Produkt 'H660G'

W sekcji 'Dodaj pozycję do dokumentu' wybieramy produkt. Ponieważ jest to produkt z egzemplarzami pole 'ilość' zostaje automatycznie uzupełniane w momencie kiedy wybieramy urządzenia z listy dostępnych egzemplarzy.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-84.png)

Klikamy ikonkę 'Zapisz' na końcu wiersza, aby dodać pozycję do dokumentu.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-85.png)

###### Produkt 'Petchcord APC G657A2'

W sekcji 'Dodaj pozycję do dokumentu' wybieramy produkt. Ponieważ jest to produkt bez egzemplarzy musimy uzupełnić pole 'Ilość'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-86.png)

Klikamy ikonkę 'Zapisz' na końcu wiersza, aby dodać pozycję do dokumentu.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-87.png)

###### Produkt 'Światłowód Optix W-NOTKSd 1J (GJFJV) 1x9/125 ITU-T G.657A'

Ponieważ jest to produkt bez egzemplarzy dodajemy go identycznie jak 'Patchcord APC G657A2' opisany powyżej.

##### Weryfikacja dokumentu

Poniżej wynikowy dokument.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-88.png)

Zanim zatwierdzimy dokument poddajmy go weryfikacji. Najważniejsze jest sprawdzenie czy ilość i jednostka miary dodanych produktów się zgadza. Do częstych błędów należy sytuacja, kiedy w pole ilość wpisujemy '10', bo chcemy w ten sposób zdjąć ze stanu magazynowego 10 metrów kabla. Niestety później okazuje się, że jednostka miary kabla to był kilometr, więc ze stanu magazynowego zdjęliśmy 10 kilometrów kabla. Doprowadzi to do sytuacji takiej, że będziemy mieli kable fizycznie na magazynie a nie będziemy tego widzieli w systemie.

##### Edycja RW

Dokument RW może podlegać wielokrotnym zmianom. Dokument jest dostępny do edycji do momentu jego zatwierdzenia.

Edycja dodanego produktu możliwa jest poprzez uruchomienie ikonki 'Edytuj' znajdującej się w wierszu produktu.

Jeśli edytujemy produkt z egzemplarzami ilość jest uzupełniana automatycznie w zależności od tego ile egzemplarzy mamy na dostępnej liście. Egzemplarz możemy usunąć z listy co spowoduje, że powróci na listę wyboru dostępnych egzemplarzy i zmieni się ilość produktu.

Koniecznie należy uruchomić akcję 'Zapisz' dostępną na końcu wiersza produktu. Jeśli tego nie zrobimy zmiany wprowadzone na pozycji znikną i trzeba będzie edycję produktu wykonać od początku.

Jeśli usuwamy z dodanych pozycji produkt posiadający egzemplarze to usuwany jest on wraz ze wszystkimi dodanymi w RW egzemplarzami.

##### Usuwanie RW

Usunąć można jedynie niezatwierdzony dokument RW.

##### Zatwierdzanie RW

Aby pozycje zawarte w RW zmieniły stany magazynowe dokument RW musi zostać zatwierdzony. Nowy stan magazynowy zaistnieje z datą zatwierdzenia dokumentu RW.

Podczas zatwierdzania dokumentu RW może wystąpić sytuacja kiedy żądane egzemplarze są już niedostępne w czasie zatwierdzania dokumentu. W takim przypadku zostanie wyświetlone odpowiednie ostrzeżenie i taki egzemplarz należy poddać edycji.

Poniżej widok stanów magazynowych dla każdego z produktów po zatwierdzeniu dokumentu RW (porównaj ze stanem na początku artykułu).

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-89.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-90.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-91.png)

##### Uwagi

- Dodawanie kolejnego RW może odbyć się bez względu na to czy już istniejące RW są zatwierdzone.
- Edycja dokumentu RW jest możliwa do momentu zatwierdzenia dokumentu. Edycji podlegają wyłącznie pozycje dokumentu.
- Usuwanie dokumentu RW jest możliwe tylko jeśli dokument jest niezatwierdzony.
- Po zatwierdzeniu dokumentu RW można dokonać jego korekty za pomocą dokumentu korygującego RWk.

## Korekta rozchodu wewnętrznego (RWk)

Należy pamiętać o nadaniu odpowiednich uprawnień dla użytkownika, który dokonuje korekty rozchodu wewnętrznego ([Uprawnienia](uprawnienia.md)).

Na potrzeby instrukcji założone było , że przyłącze do naszego klienta uległo poważnej awarii i potrzebujemy przerobić je całkowicie, co umownie potraktujemy jako działania mające na celu utrzymywanie infrastruktury własnej firmy. Poczyńmy kolejne założenia:
- zrobiliśmy RW na  materiały potrzebne do usunięcia usterki i przekazaliśmy je serwisantowi,
- serwisant będąc u klienta wymienił tylko patchcord (produkt o nazwie 'Patchcord APC G657A2' w magazynie), reszty materiałów, które pobrał nie zużył i chce zwrócić je na magazyn.

W w tym przypadku musimy zrobić korektę RW żeby zwrócone materiały wprowadzić na magazyn.

##### Korekta RW (RWk)

Na potrzeby instrukcji dokonamy korekty dokumentu RW, który powstał wcześniej w tej instrukcji.

Przed wykonaniem RW sprawdźmy stany magazynowe produktów co będzie stanowić punkt odniesienia, który na koniec pozwoli nam zobaczyć jak dokument RW wpłynął na stany magazynowe (rysunki poniżej) ([Stany magazynowe](stany_magazynowe.md)).

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-89.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-90.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-91.png)

Uruchom z menu głównego 'Magazyn-dokumenty->RW'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-92.png)

Wyszukujemy dokument RW, który będziemy chcieli skorygować i uruchamiamy przycisk 'Skoryguj' znajdujący się na końcu wiersza z dokumentem.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-93.png)

Uzupełnij plan numeracyjny.

Uruchom 'Zapisz'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-94.png)

Wygenerowany zostanie dokument RWk w stanie edycji, niezatwierdzony. Możemy teraz przystąpić do edycji jego pozycji.

##### Korekta pozycji dokumentu

Zgonie z poczynionym założeniem na magazyn należy zwrócić następujące produkty:
- 'H660G' w ilości 1 sztuka,
- 'Światłowód Optix W-NOTKSd 1J (GJFJV) 1x9/125 ITU-T G.657A' w ilości 10 metrów.

###### Produkt 'H660G'

W sekcji 'Pozycje dokumentu' klikamy w ikonkę edytuj znajdującą się w wierszu z produktem. Ponieważ jest to produkt z egzemplarzami pole 'Ilość po' zostaje automatycznie uzupełniane w momencie kiedy usuwamy urządzenia z listy dostępnych egzemplarzy (przy pomocy ikonki z koszem).

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-95.png)

Po dokonaniu zmian koniecznie należy użyć ikonki 'Zapisz' znajdującej się przy produkcie. Po zapisaniu otrzymujemy:

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-96.png)

Zwróćmy uwagę na wartości w polach 'ilość przed' (ilość przed korektą) i 'Ilość po' (ilość po korekcie). Przed korekta mieliśmy 1 sztukę po korekcie mamy 0 sztuk.

###### Produkt 'Światłowód Optix W-NOTKSd 1J (GJFJV) 1x9/125 ITU-T G.657A'

W sekcji 'Pozycje dokumentu' klikamy w ikonkę edytuj znajdującą się w wierszu z produktem. Ponieważ jest to produkt bez egzemplarzy pole 'Ilość po' musimy uzupełnić sami. Ponieważ kabel został zwrócony w całości wprowadzamy wartość '0'. Po dokonaniu zmian koniecznie należy użyć ikonki 'Zapisz' znajdującej się przy produkcie. Po zapisaniu otrzymujemy:

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-97.png)

##### Weryfikacja dokumentu

Zanim zatwierdzimy dokument poddajmy go weryfikacji. Najważniejsze jest sprawdzenie czy ilość i jednostka miary dodanych produktów się zgadza. Do częstych błędów należy sytuacja, kiedy w pole 'Ilość po' wpisujemy '1', bo chcemy w ten sposób wprowadzić na magazyn 1 kilometr kabla. Niestety później okazuje się, że jednostka miary kabla to był metr, więc na stan magazynowego wprowadzimy 1 metr kabla. Doprowadzi to do sytuacji takiej, że będziemy mieli kable fizycznie na magazynie a nie będziemy tego widzieli w systemie.

##### Edycja RWk

Dokument RWk może podlegać wielokrotnym zmianom. Dokument jest dostępny do edycji do momentu jego zatwierdzenia.

Edycja dodanego produktu możliwa jest poprzez uruchomienie ikonki 'Edytuj' znajdującej się w wierszu produktu.

Jeśli edytujemy produkt z egzemplarzami 'Ilość po' jest uzupełniana automatycznie w zależności od tego ile egzemplarzy pozostanie na liście egzemplarzy. Jeśli usuniemy egzemplarz z listy co spowoduje, że powróci na listę wyboru egzemplarzy i zmieni się ilość produktu. W razie pomyłki można egzemplarz wybrać ponownie.

Koniecznie należy uruchomić akcję 'Zapisz' dostępną na końcu wiersza produktu. Jeśli tego nie zrobimy zmiany wprowadzone na pozycji znikną i trzeba będzie edycję produktu wykonać od początku.

Usuwanie produktu z pozycji dokumentu jest niemożliwe. Jeśli produkt korygujemy w całości to w pole 'Ilość po' wstawiamy wartość '0'.

##### Usuwanie RWk

Usunąć można jedynie niezatwierdzony dokument RWk.

##### Zatwierdzanie RWk

Aby pozycje zawarte w RWk zmieniły stany magazynowe dokument RWk musi zostać zatwierdzony. Nowy stan magazynowy zaistnieje z datą zatwierdzenia dokumentu RWk.

Poniżej widok stanów magazynowych dla każdego z produktów po zatwierdzeniu dokumentu RWk (porównaj ze stanem przed korektą).

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-98.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-99.png)

##### Uwagi

- Dodawanie kolejnego RWk może odbyć się bez względu na to czy już istnieją inne niezatwierdzone RWk.
- Edycja dokumentu RWk jest możliwa do momentu zatwierdzenia dokumentu. Edycji podlegają wyłącznie pozycje dokumentu.
- Usuwanie dokumentu RWk jest możliwe tylko jeśli dokument jest niezatwierdzony.
- Po zatwierdzeniu dokumentu RWk nie można wystawić kolejnej korekty.
- Lista dokumentów RWk dostępna jest z menu głównego (Magazyn-dokumenty->RWk)
