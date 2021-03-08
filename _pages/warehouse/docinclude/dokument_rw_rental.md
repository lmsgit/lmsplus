## Dzierżawa urządzeń

Do prowadzenia ewidencji urządzeń, które są dzierżawione używamy produktów z egzemplarzami. Zalecane też jest żeby urządzenie było powiązane z osprzętem sieciowym.

Do prowadzenia ewidencji urządzeń, które zostały wydane w dzierżawę dzierżawione używamy dokumentu RW (rozchód wewnętrzny). Należy pamiętać o nadaniu odpowiednich uprawnień dla użytkownika, który dokonuje rozchodu wewnętrznego produktów ([Uprawnienia](uprawnienia.md)).

Na potrzeby instrukcji zakładamy, że chcemy podpisać umowę na świadczenie usług internetowych z klientem 'BOYD Jean'. Na czas trwania usługi chcemy oddać klientowi w dzierżawę konkretny egzemplarz urządzenia 'H640G'. Niech to będzie egzemplarz o nazwie 'ROUTER-00197754315' i SN '00197754315'.

Ponieważ nasze urządzenie fizycznie opuści magazyn musimy to zarejestrować w magazynie używając dokumentu RW.

##### Tworzenie RW

Przed wykonaniem RW sprawdźmy stany magazynowy produktu co będzie stanowić punkt odniesienia, który na koniec pozwoli nam zobaczyć jak dokument RW wpłynął na stan magazynowy (rysunek poniżej) ([Stany magazynowe](stany_magazynowe.md)). Pokażmy też jak wygląda urządzenie w osprzęcie sieciowym.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-100.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-105.png)

Jak widzimy egzemplarz jest na magazynie.

Uruchom z menu głównego 'Magazyn-dokumenty->RW'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-81.png)

Uruchom przycisk 'Dodaj dokument'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-101.png)

Uzupełnij kolejno:
- zaznacz opcję "Dzierżawa" i wybierz klienta
- firmę,
- magazyn główny,
- plan numeracyjny.

Uruchom 'Zapisz'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-102.png)

Wygenerowany zostanie dokument RW w stanie edycji, niezatwierdzony. Możemy teraz przystąpić do dodawania do dokumentu produktu.

W sekcji 'Dodaj pozycję do dokumentu' wybieramy produkt 'H640G'. Ponieważ jest to produkt z egzemplarzami pole 'ilość' zostaje automatycznie uzupełniane w momencie kiedy wybierzemy urządzenie z listy dostępnych egzemplarzy.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-103.png)

Klikamy ikonkę 'Zapisz' na końcu wiersza aby dodać pozycję do dokumentu.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-104.png)

##### Edycja RW

Dokument RW może podlegać wielokrotnym zmianom. Dokument jest dostępny do edycji do momentu jego zatwierdzenia.

Może zaistnieć sytuacja, że podczas dodawania egzemplarza wybierzemy niewłaściwy. W takim przypadku należy wyedytować pozycję dokumentu, usunąć zły egzemplarz i dodać właściwy.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-106.png)

Edycja dodanego produktu możliwa jest poprzez uruchomienie ikonki 'Edytuj' znajdującej się w wierszu produktu.

Edytujemy produkt z egzemplarzami dlatego ilość jest uzupełniana automatycznie w zależności od tego ile egzemplarzy mamy na dostępnej liście. Egzemplarz możemy usunąć z listy co spowoduje, że powróci na listę wyboru dostępnych egzemplarzy i zmieni się ilość produktu.

Koniecznie należy uruchomić akcję 'Zapisz' dostępną na końcu wiersza produktu. Jeśli tego nie zrobimy zmiany wprowadzone na pozycji znikną i trzeba będzie edycję produktu wykonać od początku.

Jeśli usuwamy z dodanych pozycji produkt posiadający egzemplarze to usuwany jest on wraz ze wszystkimi dodanymi w RW egzemplarzami.

##### Usuwanie RW

Usunąć można jedynie niezatwierdzony dokument RW.

##### Zatwierdzanie RW

Aby pozycje zawarte w RW zmieniły stany magazynowe dokument RW musi zostać zatwierdzony. Nowy stan magazynowy zaistnieje z datą zatwierdzenia dokumentu RW.

Podczas zatwierdzania dokumentu RW może wystąpić sytuacja kiedy żądane egzemplarze są już niedostępne w czasie zatwierdzania dokumentu. W takim przypadku zostanie wyświetlone odpowiednie ostrzeżenie i taki egzemplarz należy poddać edycji.

Poniżej widok stanu magazynowego produktu po zatwierdzeniu dokumentu RW (porównaj ze stanem na początku artykułu).

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-107.png)

Czynność zatwierdzenia dokumentu powoduje też automatyczne przypisanie klienta do urządzenia sieciowego, o ile przed wystawieniem RW nie było już przypisanego klienta do urządzenia. Przypisanie klienta do urządzenia jest możliwe wyłącznie jeśli egzemplarz w magazynie jest powiązany z urządzeniem w osprzęcie sieciowym.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-108.png)

Po zatwierdzeniu dokumentu możemy przekazać urządzenie klientowi. Bardzo ważne jest żeby klient dostał urządzenie z taki numerem seryjnym jaki wystawiliśmy na RW.

##### Kartoteka klienta

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-109.png)

Plugin warehouse dodaje do kartoteki klienta panele:
- 'Dokumenty magazynowe klienta'
- 'Urządzenia sieciowe w dokumentach magazynowych'

Informacje z tych paneli pozwalają zachować historię operacji magazynowych powiązanych z klientem i jej śledzenie.

##### Uwagi

- Dodawanie kolejnego RW może odbyć się bez względu na to czy już istniejące RW są zatwierdzone.
- Edycja dokumentu RW jest możliwa do momentu zatwierdzenia dokumentu. Edycji podlegają wyłącznie pozycje dokumentu.
- Usuwanie dokumentu RW jest możliwe tylko jeśli dokument jest niezatwierdzony.
- Po zatwierdzeniu dokumentu RW można dokonać jego korekty za pomocą dokumentu korygującego RWk.
- Należy pamiętać że dokument RW jest dokumentem wewnętrznym firmy i jako taki nie stanowi podstawy do potwierdzenia przez klienta odbioru urządzenia. Klient powinien potwierdzić odbiór urządzenia np. dokumentem 'Protokół odbioru', lub podobnym dokumentem, w zależności co stosowane jest w firmie.

## Zwrot dzierżawionego urządzenia

Zwrot dzierżawionego urządzenia w magazynie dokumentujemy dokumentem korekty RWk. Należy pamiętać o nadaniu odpowiednich uprawnień dla użytkownika, który dokonuje korekty rozchodu wewnętrznego ([Uprawnienia](uprawnienia.md)).

Dokument oryginalny RW możemy znaleźć np. z poziomu kartoteki klienta używając dodatkowych paneli jakie dodawane są przez plugin magazynowy.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-110.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-111.png)

Po kliknięciu w wiersz zostajemy przeniesieni na stronę informacyjną oryginalnego dokumentu RW.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-112.png)

Uruchamiamy 'Skoryguj' i dalej postępujemy analogicznie jak przy korekcie standardowego dokumentu RW ([Rozchód wewnętrzny i korekta rozchodu (RW) (RWk)](dokument_rw.md)).

Gotowy dokument korekty wygląda następująco:

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-113.png)

Informacje na karcie klienta wyglądają następująco:

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-114.png)

Warto zauważyć, że po korekcie urządzenie sieciowe już nie jest przypisane do klienta. Ta czynność została wykonana automatycznie podczas zatwierdzania dokumentu korekty.

##### Uwagi

- Korekta dokumentu dzierżawy jest dokumentem RWk i jako taki podlega tym samych zasadom używania, które dotyczą standardowej korekty RWk.
- Lista dokumentów RWk dostępna jest z menu głównego (Magazyn-dokumenty->RWk)
