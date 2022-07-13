## Sprzedaż produktów z magazynu - faktura na podstawie WZ

Do prowadzenia ewidencji urządzeń, które zostały sprzedane używamy dokumentu WZ (wydanie zewnętrzne). Należy pamiętać o nadaniu odpowiednich uprawnień dla użytkownika do dokumentów WZ i magazynu sprzedaży ([Uprawnienia](uprawnienia.md)).

Mechanizm objęty jest przez plugin walidacją więc w przypadku jakichkolwiek problemów użytkownik będzie o nich informowany.

Na potrzeby instrukcji zakładamy, że mamy następujące produkty w magazynie do sprzedaży:

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-130.png)

Na potrzeby instrukcji zakładamy, że klient naszej sieci przychodzi do nas i mówi, że chce od nas kupić 1 sztukę routera, bo chce u siebie na własną rękę podłączyć te urządzenie. My mamy w sprzedaży trzy modele routera (zrzut ekranu powyżej). Klient to maruda i nie może się zdecydować, który wybrać. Podejrzewamy, że jak mu sprzedamy jeden model i wystawimy fakturę, to następnego dnia wróci i będzie chciał wymienić to na inny model, a wtedy trzeba będzie robić korektę faktury i wystawiać nową na drugi model. Chcemy uniknąć papierologii więc przyjmujemy strategię 'życzliwego sprzedawcy' i mówimy klientowi tak: "Wydamy Panu po jednej sztuce każdego modelu żeby sobie Pan przetestował. Wystawimy dokument WZ na te 3 sztuki, który Pan podpisze. Jeśli w ciągu 3 dni zwróci Pan niewykorzystane urządzenia to wystawimy fakturę tylko na te, które zostało u Pana. Jeśli nie zwróci Pan tych urządzeń w ciągu 3 dni to na podstawie dokumentu WZ mamy prawo wystawić Panu fakturę na te urządzenia w cenach z WZ."

### Tworzenie WZ

Uruchom z menu głównego 'Magazyn-dokumenty->WZ'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-131.png)

Uruchom przycisk 'Dodaj dokument'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-132.png)

Uzupełnij kolejno:
- klienta,
- firmę,
- magazyn główny,
- plan numeracyjny.

Uruchom 'Zapisz'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-133.png)

Wygenerowany zostanie dokument WZ w stanie edycji, niezatwierdzony. Możemy teraz przystąpić do dodawania do dokumentu produktów.

W sekcji 'Dodaj pozycję do dokumentu' wybieramy produkt 'H640G'. Ponieważ jest to produkt z egzemplarzami pole 'ilość' zostaje automatycznie uzupełniane w momencie kiedy wybierzemy urządzenie z listy dostępnych egzemplarzy. Podajemy również cenę sprzedaży.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-134.png)

Klikamy ikonkę 'Zapisz' na końcu wiersza, aby dodać pozycję do dokumentu.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-135.png)

Dodajemy pozostałe produkty, w wyniku czego otrzymujemy:

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-136.png)

##### Edycja WZ

Dokument WZ może podlegać wielokrotnym zmianom. Dokument jest dostępny do edycji do momentu jego zatwierdzenia.

Może zaistnieć sytuacja, że podczas dodawania egzemplarza wybierzemy niewłaściwy. W takim przypadku należy edytować pozycję dokumentu, usunąć zły egzemplarz i dodać właściwy.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-137.png)

Edycja dodanego produktu możliwa jest poprzez uruchomienie ikonki 'Edytuj' znajdującej się w wierszu produktu.

Edytujemy produkt z egzemplarzami dlatego ilość jest uzupełniana automatycznie w zależności od tego ile egzemplarzy mamy na dostępnej liście. Egzemplarz możemy usunąć z listy co spowoduje, że powróci na listę wyboru dostępnych egzemplarzy i zmieni się ilość produktu.

Koniecznie należy uruchomić akcję 'Zapisz' dostępną na końcu wiersza produktu. Jeśli tego nie zrobimy zmiany wprowadzone na pozycji znikną i trzeba będzie edycję produktu wykonać od początku.

Jeśli usuwamy z dodanych pozycji produkt posiadający egzemplarze to usuwany jest on wraz ze wszystkimi dodanymi w RW egzemplarzami.

##### Usuwanie WZ

Usunąć można jedynie niezatwierdzony dokument WZ.

##### Zatwierdzanie WZ

Aby pozycje zawarte w WZ zmieniły stany magazynowe dokument WZ musi zostać zatwierdzony. Nowy stan magazynowy zaistnieje z datą zatwierdzenia dokumentu WZ.

Podczas zatwierdzania dokumentu WZ może wystąpić sytuacja kiedy żądane egzemplarze są już niedostępne w czasie zatwierdzania dokumentu. W takim przypadku zostanie wyświetlone odpowiednie ostrzeżenie i taki egzemplarz należy poddać edycji.

Poniżej widok stanu magazynowego produktu po zatwierdzeniu dokumentu WZ (porównaj ze stanem na początku artykułu).

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-138.png)

Po zatwierdzeniu dokumentu możemy wydrukować WZ. Żeby to zrobić wyświetlamy dokument (rysunek powyżej) i zaznaczmy:
- "Drukuj z cenami sprzedaży"
- "Drukuj z egzemplarzami"
- oryginał
- kopia.

Uruchamiamy "Drukuj". Wynik poniżej:

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-139.png)

Uwaga: wydruk z cenami sprzedaży jest możliwy tylko z poziomu wyświetlanego dokumentu.

Dajemy klientowi do podpisu oba egzemplarze. Jeden egzemplarz przekazujemy klientowi, drugi pozostaje dla nas. Jeśli klient podpisze WZ możemy przekazać urządzenia klientowi. Bardzo ważne jest żeby klient dostał urządzenie z taki numerem seryjnym jaki wystawiliśmy na WZ (ponieważ jest to produkt z egzemplarzami).

Plugin warehouse dodaje do kartoteki klienta panele:
- 'Dokumenty magazynowe klienta'
- 'Urządzenia sieciowe w dokumentach magazynowych'

Informacje z tych paneli pozwalają zachować historię operacji magazynowych powiązanych z klientem i jej śledzenie.

Poniżej stany magazynowe po zatwierdzeniu WZ.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-140.png)

##### Uwagi

- Dodawanie kolejnego WZ może odbyć się bez względu na to czy już istniejące WZ są zatwierdzone.
- Edycja dokumentu WZ jest możliwa do momentu zatwierdzenia dokumentu. Edycji podlegają wyłącznie pozycje dokumentu.
- Usuwanie dokumentu WZ jest możliwe tylko jeśli dokument jest niezatwierdzony.
- Po zatwierdzeniu dokumentu WZ można dokonać jego korekty za pomocą dokumentu korygującego WZk o ile nie została już wystawiona faktura do WZ (wtedy trzeba wykonać korektę faktury).

### Korekta WZ (WZk)

Na potrzeby instrukcji Założyliśmy, że klient w ciągu 3 dni zwróci niewykorzystane urządzenia. I tak też się dzieje. Klient zdecydował się zakupić urządzenie 'H660G'. Musimy zatem przed wystawieniem faktury dokonać korekty WZ na zwrócone urządzenia inaczej żeby wprowadzić zwrócone urządzenia na stany magazynowe.

Zwrot urządzeń wydanych dokumentem WZ dokumentujemy dokumentem korekty WZk. Należy pamiętać o nadaniu odpowiednich uprawnień dla użytkownika, który dokonuje korekty WZ ([Uprawnienia](uprawnienia.md)).

Dokument oryginalny WZ możemy znaleźć np. z poziomu kartoteki klienta używając dodatkowych paneli jakie dodawane są przez plugin magazynowy.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-141.png)

Po kliknięciu w wiersz zostajemy przeniesieni na stronę informacyjną oryginalnego dokumentu WZ.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-138.png)

Uruchamiamy 'Skoryguj'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-142.png)

Uzupełnij plan numeracyjny.

Uruchom 'Zapisz'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-143.png)

Wygenerowany zostanie dokument WZk w stanie edycji, niezatwierdzony. Możemy teraz przystąpić do edycji jego pozycji.

##### Korekta pozycji dokumentu

W sekcji 'Pozycje dokumentu' klikamy w ikonkę edytuj znajdującą się w wierszu z produktem. Ponieważ jest to produkt z egzemplarzami pole 'Ilość po' zostaje automatycznie uzupełniane w momencie kiedy usuwamy urządzenia z listy dostępnych egzemplarzy (przy pomocy ikonki z koszem).

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-144.png)

Tylko dla urządzenia 'H660G' nic nie zmieniamy ponieważ na to urządzenie będziemy chcieli wystawić fakturę dla klienta. Zwróćmy uwagę na wartości w polach 'ilość przed' (ilość przed korektą) i 'Ilość po' (ilość po korekcie). Przed korekta mieliśmy 1 sztukę po korekcie mamy 0 sztuk.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-145.png)

##### Edycja WZk

Dokument WZk może podlegać wielokrotnym zmianom. Dokument jest dostępny do edycji do momentu jego zatwierdzenia.

Edycja dodanego produktu możliwa jest poprzez uruchomienie ikonki 'Edytuj' znajdującej się w wierszu produktu.

Jeśli edytujemy produkt z egzemplarzami 'Ilość po' jest uzupełniana automatycznie w zależności od tego ile egzemplarzy pozostanie na liście egzemplarzy. Jeśli usuniemy egzemplarz z listy co spowoduje, że powróci na listę wyboru egzemplarzy i zmieni się ilość produktu. W razie pomyłki można egzemplarz wybrać ponownie.

Koniecznie należy uruchomić akcję 'Zapisz' dostępną na końcu wiersza produktu. Jeśli tego nie zrobimy zmiany wprowadzone na pozycji znikną i trzeba będzie edycję produktu wykonać od początku.

Usuwanie produktu z pozycji dokumentu jest niemożliwe. Jeśli produkt korygujemy w całości to w pole 'Ilość po' wstawiamy wartość '0'.

##### Usuwanie WZk

Usunąć można jedynie niezatwierdzony dokument WZk.

##### Zatwierdzanie WZk

Aby pozycje zawarte w WZk zmieniły stany magazynowe dokument WZk musi zostać zatwierdzony. Nowy stan magazynowy zaistnieje z datą zatwierdzenia dokumentu WZk.

Gotowy dokument korekty wygląda następująco:

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-146.png)

Poniżej widok stanów magazynowych dla każdego z produktów po zatwierdzeniu dokumentu WZk (porównaj ze stanem przed korektą).

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-147.png)

##### Uwagi

- Dodawanie kolejnego WZk może odbyć się bez względu na to czy już istnieją inne niezatwierdzone WZk.
- Edycja dokumentu WZk jest możliwa do momentu zatwierdzenia dokumentu. Edycji podlegają wyłącznie pozycje dokumentu.
- Usuwanie dokumentu WZk jest możliwe tylko jeśli dokument jest niezatwierdzony.
- Po zatwierdzeniu dokumentu WZk nie można wystawić kolejnej korekty.
- Lista dokumentów WZk dostępna jest z menu głównego (Magazyn-dokumenty->WZk).

### Wystawienie faktury

W tym momencie możemy wystawić fakturę.

Znajdujemy dokument oryginalny WZ. Możemy to zrobić np. z poziomu kartoteki klienta używając dodatkowych paneli jakie dodawane są przez plugin magazynowy.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-141.png)

Po kliknięciu w wiersz zostajemy przeniesieni na stronę informacyjną oryginalnego dokumentu WZ.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-138.png)

Uruchamiamy 'Utwórz dokument sprzedaży'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-148.png)

Otrzymujemy gotową fakturę tylko na towar, który pozostał u klienta z uzupełnioną ceną sprzedaży.

##### Uwagi
- Na fakturze możemy zmieniać jedynie cenę sprzedaży dla pozycji magazynowych. Domyślnie wstawiana jest cena sprzedaży z WZ a jeśli jej nie ma wstawiana jest domyślna cena sprzedaży produktu ([Domyślne ceny sprzedaży produktu](ceny_sprzedazy.md)).
- Podpowiadane są ceny zakupu produktu w celu zabezpieczenia przed sprzedażą poniżej ceny zakupu.
- Na fakturze nie możemy usuwać pozycji magazynowych.
- Jeśli faktura jest powiązana z dokumentem WZ operacja usuwania faktury się nie powiedzie.
- Jeśli korekta faktury jest powiązana z dokumentem WZk operacja usuwania korekty faktury się nie powiedzie.
- Kategoria podatkowa jest podpowiadana podczas tworzenia FV i jest definiowania na poziomie produktu dlatego jeśli na fakturze jest nieprawidłowa to należy ją zmienić z poziomu produktu i ponownie wygenerować fakturę.
- Do wystawianej faktury można dodać pozycje nie pochodzące z magazynu.

Po wystawieniu faktury przyjęte założenia zostały zrealizowane, a nasz cel osiągnięty.

##### Extra czynności

Czasami może okazać się potrzebne wykonanie kolejnych czynności. Żeby to zobrazować poczynimy na potrzeby instrukcji kolejne założenia. W pierwszej części instrukcji nasz klient dostał fakturę na urządzenie (rysunek poniżej). Zakładamy, że po 2 tygodniach urządzenie uległo awarii i klient chce wymienić urządzenie na sprawne.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-149.png)

W takim wypadku należy wystawić korektę faktury. Uruchom standardową dla LMS akcję tworzenia korekty faktury.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-150.png)

Edytujemy produkt z egzemplarzami dlatego ilość jest uzupełniana automatycznie w zależności od tego ile egzemplarzy mamy na dostępnej liście. Egzemplarz usuwamy z listy co spowoduje, że powróci na listę wyboru dostępnych egzemplarzy i zmieni się ilość produktu na '0'.

Możemy jednocześnie zmienić cenę (w tym przypadku nic to nie zmieni bo i tak wyzerowaliśmy pozycję).

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-151.png)

Uruchom "Zapisz".

W momencie zapisu tworzony jest dokument WZk, który wprowadza na magazyn sprzedaży niesprawne urządzenie klienta. Takie WZk jest już zatwierdzone.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-152.png)

Urządzenie wróciło na ten sam magazyn, z którego było rozchodowane czyli na magazyn sprzedaży. Stan magazynowy został zwiększony (rysunek poniżej)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-153.png)

##### Uwagi

Jeśli wystawiamy korektę faktury z pozycjami magazynowymi to:
  - Korygowanie pozycji magazynowych można wykonać tylko raz (tylko przy pierwszej korekcie faktury będzie generowany dokument WZk).
  - Zapisanie korekty faktury powoduje, że automatycznie tworzona jest zatwierdzona korekta dokumentu WZk dla tej faktury, który zawiera tylko pozycje magazynowe.
  - Zapisanie korekty faktury powoduje, że edycja takiej korekty faktury będzie możliwa dla pozycji magazynowych jedynie w zakresie cen.
  - Zapisanie korekty faktury powoduje, że usunięcie korekty faktury będzie niemożliwe.
  - Anulowanie korekty faktury nie powoduje żadnych akcji po stronie magazynu. Dokument WZk nadal będzie istniał i będzie zmieniał stany magazynowe.
- Jeśli korekta faktury jest powiązana z dokumentem WZk operacja usuwania korekty faktury się nie powiedzie.

###### Utylizacja urządzenia

Ponieważ zepsute urządzenie poprzez WZk zostało przyjęte na magazyn sprzedaży musimy się go z tego magazynu pozbyć, ponieważ inny pracownik mógłby je wystawić do sprzedaży dla kolejnego klienta, a tego nie chcemy. W tej instrukcji  [Utylizacja urządzeń](utylizacja_urzadzen.md) zostało opisane jak tego dokonać.
