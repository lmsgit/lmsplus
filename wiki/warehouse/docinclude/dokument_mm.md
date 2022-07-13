## Przesunięcie między magazynami

Do prowadzenia ewidencji przesunięć produktów pomiędzy magazynami używamy dokumentu MM (przesunięcie między magazynami). Należy pamiętać o nadaniu odpowiednich uprawnień dla użytkownika, który dokonuje przesunięć między magazynami zarówno do dokumentów jak i magazynów ([Uprawnienia](uprawnienia.md)).

Na potrzeby instrukcji zakładamy, że:
- Mamy utworzony magazyn do sprzedaży o nazwie 'Magazyn sprzedaży'.
- Na magazynie sprzedaży nie mamy jeszcze żadnych produktów.
- Chcemy przeznaczyć na sprzedaż 2 sztuki produktu 'H665G', który jest na magazynie głównym.
- Chcemy przeznaczyć na sprzedaż wszystkie urządzenia 'H665', które mamy na magazynie głównym.
- Chcemy przeznaczyć na sprzedaż 250mb kabla 'KABEL SIECIOWY UTP SKRĘTKA CAT5E CCA', który mamy na magazynie głównym.

Z działania pluginu wiemy, że możemy sprzedawać jedynie produkty z magazynu sprzedaży, tymczasem nasze produkty znajdują się na magazynie głównym. Musimy zatem przesunąć produkty z magazynu głównego na magazyn sprzedaży dokumentem MM.

##### Tworzenie MM

Przed wykonaniem MM sprawdźmy stany magazynowe co będzie stanowić punkt odniesienia, który na koniec pozwoli nam zobaczyć jak dokument MM wpłynął na stany magazynowe (rysunek poniżej) ([Stany magazynowe](stany_magazynowe.md)). Magazyn sprzedaży według założenia jest pusty więc nie będzie w nim żadnych produktów.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-115.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-116.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-123.png)

Uruchom z menu głównego 'Magazyn-dokumenty->RW'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-117.png)

Uruchom przycisk 'Dodaj dokument'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-118.png)

Uzupełnij kolejno:
- firmę,
- z jakiego magazynu pobrać produkty,
- do jakiego magazynu przenieść produkty,
- plan numeracyjny.

Uruchom 'Zapisz'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-119.png)

Wygenerowany zostanie dokument MM w stanie edycji, niezatwierdzony. Możemy teraz przystąpić do dodawania do dokumentu produktu.

W sekcji 'Dodaj pozycję do dokumentu' wybieramy produkt 'H665G'. Ponieważ jest to produkt z egzemplarzami pole 'ilość' zostaje automatycznie uzupełniane w momencie kiedy wybierzemy urządzenie z listy dostępnych egzemplarzy.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-120.png)

Klikamy ikonkę 'Zapisz' na końcu wiersza, aby dodać pozycję do dokumentu.

Powtarzamy czynność dla produktu 'H665G'.

Dodajemy do dokumentu produkt 'KABEL SIECIOWY UTP SKRĘTKA CAT5E CCA' podając jego ilość.

W wyniku otrzymujemy:

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-121.png)

##### Edycja MM

Dokument MM może podlegać wielokrotnym zmianom. Dokument jest dostępny do edycji do momentu jego zatwierdzenia.

Może zaistnieć sytuacja, że podczas dodawania egzemplarza wybierzemy niewłaściwy. W takim przypadku należy edytować pozycję dokumentu, usunąć zły egzemplarz i dodać właściwy.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-122.png)

Edycja dodanego produktu możliwa jest poprzez uruchomienie ikonki 'Edytuj' znajdującej się w wierszu produktu.

Edytujemy produkt z egzemplarzami dlatego ilość jest uzupełniana automatycznie w zależności od tego ile egzemplarzy mamy na dostępnej liście. Egzemplarz możemy usunąć z listy co spowoduje, że powróci na listę wyboru dostępnych egzemplarzy i zmieni się ilość produktu.

Koniecznie należy uruchomić akcję 'Zapisz' dostępną na końcu wiersza produktu. Jeśli tego nie zrobimy zmiany wprowadzone na pozycji znikną i trzeba będzie edycję produktu wykonać od początku.

Jeśli usuwamy z dodanych pozycji produkt posiadający egzemplarze to usuwany jest on wraz ze wszystkimi dodanymi w MM egzemplarzami.

##### Usuwanie RW

Usunąć można jedynie niezatwierdzony dokument MM.

##### Zatwierdzanie MM

Aby pozycje zawarte w MM zmieniły stany magazynowe dokument MM musi zostać zatwierdzony. Nowy stany magazynowe zaistnieją z datą zatwierdzenia dokumentu MM.

Podczas zatwierdzania dokumentu MM może wystąpić sytuacja kiedy żądane egzemplarze są już niedostępne w czasie zatwierdzania dokumentu. W takim przypadku zostanie wyświetlone odpowiednie ostrzeżenie i taki egzemplarz należy poddać edycji.

Na poniższych obrazkach widzimy jak wyglądają stany magazynowe produktów po zatwierdzeniu MM (porównaj ze stanami pokazanymi na początku instrukcji).

Na magazynie głównym mamy:

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-124.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-125.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-126.png)

Widzimy, że stany magazynowe uległy zmniejszeniu.

Na magazynie sprzedaży mamy:

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-127.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-128.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-129.png)

Widzimy, że stany magazynowe uległy zwiększeniu.

Osiągnęliśmy nasz zamierzony cel. Magazyn sprzedaży mamy uzupełniony o produkty więc będziemy mogli je sprzedawać i jednocześnie poddawać ewidencji magazynowej.

##### Korekta MM

Dokumentu MM nie można korygować inaczej jak tylko przez wystawienie kolejnego dokumentu MM, który odwróci sytuację.

##### Uwagi

- Dodawanie kolejnego MM może odbyć się bez względu na to czy już istniejące MM są zatwierdzone.
- Edycja dokumentu MM jest możliwa do momentu zatwierdzenia dokumentu. Edycji podlegają wyłącznie pozycje dokumentu.
- Usuwanie dokumentu MM jest możliwe tylko jeśli dokument jest niezatwierdzony.
- Podczas zatwierdzania dokumentu MM może wystąpić sytuacja kiedy żądana ilość produktu jest już niedostępna w czasie zatwierdzania dokumentu. W takim przypadku zostanie wyświetlone odpowiednie ostrzeżenie i taki egzemplarz należy poddać edycji w dokumencie.
- Nieco personifikując dokument MM, możemy powiedzieć, że jest dla niego wszystko jedno czy produkt jest z egzemplarzami, czy bez oraz czy jest powiązany z osprzętem, czy nie. On zwyczajnie przenosi produkt takim jaki jest z jednego magazynu do drugiego.
