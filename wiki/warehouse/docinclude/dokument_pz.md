## Przyjęcie zewnętrzne

Przyjęcia towaru dokonujemy z wykorzystaniem dokumentu magazynowego PZ (przyjęcie zewnętrzne). Produkty możemy wprowadzić na dowolny magazyn firmy. Należy pamiętać o nadaniu odpowiednich uprawnień dla użytkownika, który dokonuje przyjęcia produktów ([Uprawnienia](uprawnienia.md)).

**Uwaga!**
- Jeśli podczas tworzenia pierwszego dokumentu przyjęcia PZ produkt nie miał przypisanych egzemplarzy, to ten produkt przez cały czas użytkowania w magazynie będzie widziany jako produkt bez egzemplarzy,
- Jeśli podczas tworzenia pierwszego dokumentu przyjęcia PZ produkt miał przypisane egzemplarze, to ten produkt przez cały czas użytkowania w magazynie będzie widziany jako produkt z egzemplarzami.

Na potrzeby instrukcji zakładamy, że:
- Kupiliśmy produkty i otrzymaliśmy fakturę zakupu FV/1/2020 od dostawcy 'ARBUCKLE' na łączną wartość netto 2055 zł netto.
- Towar od sprzedawcy otrzymaliśmy w dniu 20/04/2020.
- Fakturę od sprzedawcy otrzymaliśmy w dniu 21/04/2020.
- Na fakturze mamy następujące pozycje:
  - 'Router H640G' w ilości 3szt.. Cena za sztukę 145 zł netto. Otrzymaliśmy też do tego specyfikację numerów seryjnych w postaci kodów kreskowych. Kody kreskowe są następujące: 00216600316, 00208450915, 00208380915.
  - 'Router H665' w ilości 3szt.. Cena za sztukę 170 zł netto. Otrzymaliśmy też do tego specyfikację numerów seryjnych w postaci kodów kreskowych. Kody kreskowe są następujące: 00211860915, 00208300915, 00211920915.
  - 'Kabel UTP CAT5E CCA' w ilości 2km. Cena za kilometr kabla 430 zł netto.
  - 'Patchcord światłowodowy APC G657A2' w ilości 20 sztuk. Cena za sztukę 12,5 zł netto.
- Posiadamy już na magazynie pewną ilość produktu 'Router H640G'. W magazynie jest on oznaczony nazwą 'H640G'. Produkt 'H640G' jest produktem z egzemplarzami i jest powiązany z OS.
- Nigdy nie posiadaliśmy produktu 'Router H665'. Nie będziemy go wprowadzać do osprzętu sieciowego ponieważ jest to towar na sprzedaż. Chcemy żeby to był produkt z egzemplarzami, bo chcemy wiedzieć jaki był SN sprzedawanego urządzenia.
- Posiadamy już na magazynie pewną ilość produktu 'Kabel UTP CAT5E CCA'. W magazynie jest on oznaczony nazwą 'KABEL SIECIOWY UTP SKRĘTKA CAT5E CCA'.
- Nigdy nie posiadaliśmy produktu 'Patchcord światłowodowy APC G657A2'.

##### Uzupełnienie katalogu produktów.

Przed wykonaniem PZ sprawdźmy czy produkty z faktury zakupu FV/1/2020 znajdują się w katalogu produktów (rysunki poniżej).

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-53.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-54.png)

- Produkt 'H640G' jest w katalogu produktów więc musimy do niego wprowadzić kolejne egzemplarze z faktury zakupu. Robimy to przy pomocy tej instrukcji [Tworzenie produktu powiązanego z OS](produkt_z_egz_os.md) korzystając z sekcji 'Dodawanie egzemplarza'.
- Produkt 'KABEL SIECIOWY UTP SKRĘTKA CAT5E CCA' znajduje się w katalogu produktów więc nie musimy go dodawać ponownie.
- Produktu 'Router H665' nie ma w katalogu produktów więc musimy go do niego dodać. Zakładaliśmy, że ma być produktem z egzemplarzami ale nie chcemy wiązać go z osprzętem sieciowym, więc tworzymy go według tej instrukcji [Tworzenie produktu z egzemplarzami niepowiązanego z OS](produkt_z_egz.md).
- Produktu 'Patchcord światłowodowy APC G657A2' nie ma w katalogu produktów więc musimy go utworzyć zgodnie z tą instrukcją [Tworzenie produktu bez egzemplarzy](produkt_bez_egz.md).

W katalogu produktów otrzymujemy następujące wyniki:

- dla produktu 'H640G'

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-55.png)

- dla produktu 'H665'

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-56.png)

- dla produktu 'KABEL SIECIOWY UTP SKRĘTKA CAT5E CCA'

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-54.png)

- dla produktu 'Petchcord APC G657A2'

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-57.png)

Proszę zwrócić uwagę, że nazwy produktów jakie użyliśmy różnią się od nazw na fakturze zakupu. Nie ma obowiązku, żeby przyjmować nazwy producenta jednak nasza nazwa musi nawiązywać do nazwy z faktury zakupu żeby można było ją powiązać z odpowiednią pozycją faktury zakupu.

Po uzupełnieniu katalogu produktów możemy przejść do tworzenia dokumentu PZ

##### Tworzenie PZ

Przed wykonaniem PZ sprawdźmy stany magazynowe produktów z faktury zakupu będzie to stanowić punkt odniesienia, który na koniec pozwoli nam zobaczyć jak dokument PZ wpłynął na stany magazynowe (rysunki poniżej). Ponieważ
tylko dwa produkty były już wcześniej ewidencjonowane, tylko dla nich możemy sprawdzić stan magazynowy ([Stany magazynowe](stany_magazynowe.md)).

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-58.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-59.png)

Uruchom z menu głównego 'Magazyn-dokumenty->PZ'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-60.png)

Uruchom przycisk 'Dodaj dokument'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-62.png)

Uzupełnij kolejno:
- firmę,
- magazyn główny,
- plan numeracyjny,
- dostawcę (jeśli nie ma na liście skorzystaj z instrukcji [Dostawcy](dostawcy.md), aby utworzyć dostawcę. Na liście dostawców pojawią się tylko ci, którzy jako klienci należą do wybranej wcześniej firmy,
- datę otrzymania (nasz przykładowy towar otrzymaliśmy 20/04/2020),
- numer specyfikacji (nasza przykładowa faktura zakupu miała numer FV/1/2020),
- datę specyfikacji (naszą przykładową fakturę zakupu wystawiono 21/04/2020).

Uruchom 'Zapisz'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-63.png)

Wygenerowany zostanie dokument PZ w stanie edycji, niezatwierdzony. Możemy teraz przystąpić do dodawania do dokumentu produktów pochodzących z przykładowej faktury zakupu.

##### Dodawanie produktów

###### Produkt 'H640G'

Metoda 1:

W sekcji 'Dodaj pozycję do dokumentu' wybieramy produkt 'H640G' i podajemy jego cenę netto zakupu jaką płacimy za jednostkę miary. Następnie z listy dostępnych egzemplarzy wybieramy te, które chcemy dodać. Za każdym razem kiedy dodamy egzemplarz ilość sztuk zostanie automatycznie zmieniona i przeliczona wartość.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-65.png)

Kiedy uzupełnimy te dane należy uruchomić ikonkę 'Zapisz' znajdującą się na końcu wiersza dodawanego produktu. Po zapisaniu produkt trafia na listę
pozycji dokumentu.

Metoda 2:

Dodawanie produktów jeden po drugim może być uciążliwym procesem, szczególnie w przypadku kiedy produkt posiada bardzo dużo egzemplarzy, dlatego możemy skorzystać z hurtowego dodawania produktów, które przyśpiesza pracę.

W sekcji 'Dodaj pozycję do dokumentu' wybieramy produkt 'H640G' i uruchamiamy  'Dodaj wiele'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-66.png)

Na formularzu, który się wyświetli należy wyselekcjonować produkt 'H640G', zaznaczyć i uruchomić 'Dodaj zaznaczone'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-67.png)

Produkt został dodany do listy wraz ze wszystkimi egzemplarzami, które były możliwe do dodania (takimi, które nigdy wcześniej nie były dodane innym PZ lub BO). Pozostaje jedynie edytować pozycję, żeby określić jej cenę netto zakupu za jednostkę miary. Edycja dodanego produktu możliwa jest poprzez uruchomienie ikonki 'Edytuj' znajdującej się w wierszu produktu. Należy pamiętać aby po zakończonej edycji uruchomić ikonkę 'Zapisz' znajdującą się przy edytowanym produkcie. Jeśli tego nie zrobimy zmienione dane zostaną utracone.

Po uzupełnieniu ceny otrzymujemy zamierzony rezultat (rysunek poniżej).

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-68.png)

Możemy przejść do dodawania kolejnego produktu

###### Produkt 'H665'

Produkt 'H665' jest produktem z egzemplarzami w związku z powyższym możemy użyć dokładnie tej samej metody dodawania go do dokumentu co w przypadku produktu 'H640G' opisanego wcześniej.

Po dodaniu produktu 'H665' otrzymujemy zamierzony rezultat (rysunek poniżej).

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-69.png)

###### Produkt 'Petchcord APC G657A2'

W sekcji 'Dodaj pozycję do dokumentu' wybieramy produkt. Jest to produkt bez egzemplarzy więc podajemy jego cenę netto zakupu jaką płacimy za jednostkę miary (cena za kilometr) oraz ilość. Uruchamiamy ikonkę 'Zapisz' znajdującą się przy dodawanym produkcie.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-70.png)

Po dodaniu produktu otrzymujemy zamierzony rezultat (rysunek poniżej).

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-71.png)

###### Produkt 'KABEL SIECIOWY UTP SKRĘTKA CAT5E CCA'

Produkt jest produktem bez egzemplarzy dlatego dodajemy go identycznie jak produkt 'Patchcord APC G657A2' opisany powyżej. Należy jednak zwrócić uwagę że jednostka miary produktu to kilometr.


##### Weryfikacja dokumentu

Poniżej wynikowy dokument.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-72.png)

Zanim zatwierdzimy dokument poddajmy go weryfikacji. W naszym przypadku kwota netto naszego PZ jest taka sama jak kwota netto faktury zakupu i wynosi 2055 zł netto. Wygląda na to, że jest dobrze, ale należy jeszcze sprawdzić każdą pozycję pod względem tego, czy ilość i cena są wprowadzone do odpowiednich rubryk. Dlaczego to takie ważne? Załóżmy, że chcemy dodać  produkt A w cenie 1zł i ilości 100szt. Wartość pozycji wynosi 100zł. Jeśli w pole ilość wprowadzimy '1' a w pole cena '100' to wartość pozycji też będzie wynosić 100zł, ale będzie to błąd bo na magazyn przyjmiemy 1 sztukę zamiast 100 sztuk.

##### Edycja PZ

Dokument PZ może podlegać wielokrotnym zmianom. Dokument jest dostępny do edycji do momentu jego zatwierdzenia.

Edycja dodanego produktu możliwa jest poprzez uruchomienie ikonki 'Edytuj' znajdującej się w wierszu produktu.

Jeśli edytujemy produkt z egzemplarzami możemy podać cenę netto jednego egzemplarza lub wartość wszystkich egzemplarzy, które zostały dodane. Ilość jest uzupełniana automatycznie w zależności od tego ile egzemplarzy mamy na dostępnej liście. Egzemplarz możemy usunąć z listy co spowoduje, że powróci na listę wyboru dostępnych egzemplarzy i zmieni się ilość produktu.

Pod wpływem zmian w jednym polu pozostałe wyliczają się automatycznie.

Koniecznie należy uruchomić akcję 'Zapisz' dostępną na końcu wiersza produktu. Jeśli tego nie zrobimy zmiany wprowadzone na pozycji znikną i trzeba będzie edycję produktu wykona od początku.

Jeśli usuwamy z dodanych pozycji produkt posiadający egzemplarze to usuwany jest on wraz ze wszystkimi dodanymi w PZ egzemplarzami.

##### Usuwanie PZ

Usunąć można jedynie niezatwierdzony dokument PZ.

##### Zatwierdzanie PZ

Aby pozycje zawarte w PZ pojawiły się w stanach magazynowych dokument PZ musi zostać zatwierdzony. Stan magazynowy zaistnieje z datą zatwierdzenia dokumentu PZ.

Podczas zatwierdzania dokumentu PZ może wystąpić sytuacja kiedy żądane egzemplarze są już niedostępne w czasie zatwierdzania dokumentu. W takim przypadku zostanie wyświetlone odpowiednie ostrzeżenie i taki egzemplarz należy usunąć z dokumentu.

Poniżej widok stanów magazynowych dla każdego z produktów dodanych dokumentem PZ.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-73.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-74.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-75.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-76.png)

##### Uwagi

- Dodawanie kolejnego PZ może odbyć się bez względu na to czy już istniejące PZ są zatwierdzone.
- Edycja dokumentu PZ jest możliwa do momentu zatwierdzenia dokumentu. Edycji podlegają wyłącznie pozycje dokumentu.
- Usuwanie dokumentu PZ jest możliwe tylko jeśli dokument jest niezatwierdzony.
- Po zatwierdzeniu dokumentu PZ jego wycofanie jest niemożliwe z poziomu interfejsu programu. Wycofanie PZ może również okazać się niemożliwa nawet z pominięciem interfejsu użytkownika dlatego zaleca się jego skrupulatną weryfikację przed zatwierdzeniem.
