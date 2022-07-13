## Tworzenie bilansu otwarcia magazynu

Stworzenie bilansu otwarcia ma na celu określenie początkowych stanów magazynowych już posiadanych produktów. W tym celu należy:
- zainicjować katalog produktów, które będą wprowadzone dokumentem bilansu:
  - w przypadku kiedy do katalogu produktów chcemy wprowadzić urządzenia sieciowe należy skorzystać z synchronizacji ([Synchronizacja masowa](synchronizacja_masowa.md)),
  - w przypadku kiedy do katalogu produktów chcemy wprowadzić towar nie będący urządzeniami sieciowymi należy użyć metody dodawania produktu niepowiązanego z OS. Pomocne będą następujące artykuły:
    - [Tworzenie produktu bez egzemplarzy](produkt_bez_egz.md)
    - [Tworzenie produktu z egzemplarzami niepowiązanego z OS](produkt_z_egz.md)

Bilans otwarcia możemy wykonać poprzez dokument BO lub dokument PZ (przyjęcie zewnętrzne). Oba dokumenty działają bardzo podobnie. Dokument BO (bilans otwarcia) jest szczególnym przypadkiem dokumentu PZ. Należy uzgodnić z księgowym, który z nich zastosować.

Zastosowanie BO głównie pozwala nam po nazwie dokumentu zdecydowanie wyróżnić dokument od innych PZ, które będą standardowymi dokumentami przyjęcia od dostawców zewnętrznych.

Dokument PZ (w odróżnieniu oz BO) wymaga podania dostawcy. Jeśli bilans otwarcia robimy tworząc PZ, to musimy utworzyć swoja firmę jako klienta, który jest dostawcą zewnętrznym (klient z zaznaczoną opcją 'Dostawca').

W tej instrukcji posłużymy się dokumentem BO natomiast sposób tworzenia dokumentu PZ opisany jest tutaj [Przyjęcie zewnętrzne (PZ)](dokument_pz.md)

**Uwaga!**
- Jeśli podczas tworzenia pierwszego dokumentu przyjęcia BO produkt nie miał przypisanych egzemplarzy, to ten produkt przez cały czas użytkowania w magazynie będzie widziany jako produkt bez egzemplarzy,
- Jeśli podczas tworzenia pierwszego dokumentu przyjęcia BO produkt miał przypisane egzemplarze, to ten produkt przez cały czas użytkowania w magazynie będzie widziany jako produkt z egzemplarzami.

##### Tworzenie BO.

Plugin "Warehouse" umożliwia każdej firmie występującej w LMS prowadzenie własnej ewidencji magazynowej dlatego każda firma w LMS powinna stworzyć własny dokument BO.

Może istnieć tylko jeden dokument BO w ramach firmy i jest on zawsze tworzony dla magazynu głównego firmy. Jeśli chcemy rozpocząć ewidencjonowanie już posiadanego sprzętu, to zalecane jest utworzenie dokumentu BO jako pierwszego dokumentu magazynowego w firmie i dopiero po jego zatwierdzeniu rozpoczęcie pracy z pozostałymi dokumentami magazynowymi.

Jeśli prowadzimy ewidencję dla kliku firm to zalecane jest (tylko ze względu na wygodę pracy) utworzenie i zatwierdzenie BO dla każdej firmy zanim rozpocznie się pracę z dokumentami w firmach.

**Dodanie nowego BO jest możliwe tylko jeśli nie ma jeszcze żadnego dokumentu BO dla danej firmy i nie ma niezatwierdzonych BO innych firm.**


Przed wykonaniem bilansu stany magazynowe nie istnieją (rysunek poniżej).

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-40.png)

Katalog produktów, które będziemy dodawać do dokumentu (rysunek poniżej).

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-41.png)

Dla użytkowników zaangażowanych w tworzenie dokumentu nadaj prawa dostępu do magazynu głównego oraz nadaj odpowiednie uprawnienia do dokumentu BO.

Uruchom z menu głównego 'Magazyn-dokumenty->BO'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-42.png)

Uruchom przycisk 'Dodaj dokument'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-43.png)

Wybierz firmę, następnie magazyn główny, następnie plan numeracyjny i zapisz.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-44.png)

Wygenerowany zostanie dokument BO w stanie edycji. Do dokumentu można dodawać wszystkie dostępne produkty magazynowe i ich egzemplarze. W przypadku produktów z egzemplarzami "Dostępne" egzemplarze to takie, które nie zostały wcześniej dodane do innych dokumentów BO lub PZ. Daje to możliwość współdzielenia tych samych indeksów przez różne firmy, a nawet przypisania poszczególnych egzemplarzy tego samego produktu różnym firmom. Inaczej mówiąc, wszystko czego nie dodamy do BO dla firmy X będziemy mogli dodać do BO firmy Y, a z kolei jeśli czegoś nie dodamy do BO firmy Y, trafi do BO firmy Z itd..

**Jeśli jakiś produkt lub egzemplarz produktu nie znajdzie się w żadnym dokumencie BO żadnej firmy to nie będzie on podlegał ewidencji magazynowej.**

Możemy teraz przystąpić do dodawania produktów do dokumentu.

##### Dodawanie produktów jeden po drugim

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-45.png)

W sekcji 'Dodaj pozycję do dokumentu' wybieramy produkt i podajemy jego cenę netto zakupu jaką płacimy za jednostkę miary. Jeśli jest to produkt bez egzemplarzy to podajemy również ilość. Jeśli jest to produkt z egzemplarzami ilości nie podajemy, będzie się ona zmieniać w zależności od tego ile egzemplarzy wybierzemy z listy dostępnych egzemplarzy. Egzemplarze wybieramy jeden po drugim. Jeśli się pomylimy w wyborze egzemplarza możemy go usunąć z listy co spowoduje, że powróci na listę wyboru dostępnych egzemplarzy.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-46.png)

Kiedy uzupełnimy te dane należy uruchomić ikonkę 'Zapisz' znajdującą się na końcu wiersza dodawanego produktu. Po zapisaniu produkt trafia na listę
pozycji dokumentu.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-47.png)

Powyższe czynności powtarzamy dla kolejnych produktów

##### Dodawanie hurtowe produktów

Dodawanie produktów jeden po drugim może być uciążliwym procesem, szczególnie w przypadku kiedy produkt posiada bardzo dużo egzemplarzy, dlatego możemy skorzystać z hurtowego dodawania produktów, które przyśpiesza pracę.

Uruchom 'Dodaj wiele' w sekcji 'Dodaj pozycję do dokumentu'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-48.png)

Przeniesieni zostajemy na stronę, gdzie możemy wybrać dowolną ilość produktów, które na raz zostaną dodane do dokumentu BO.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-49.png)

'Dodaj zaznaczone' - doda do dokumentu zaznaczone produkty wraz z ich egzemplarzami (jeśli istnieją)
'Dodaj wszystkie' - doda do dokumentu wszystkie produkty z katalogu produktów wraz z ich egzemplarzami (jeśli istnieją).

Ponieważ chcemy dodać wszystko z katalogu produktów uruchamiamy 'Dodaj wszystkie'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-50.png)

Wszystkie produkty zostały dodane do listy. Pozostaje jedynie edytować każdą pozycję, żeby określić jej ilość i cenę netto zakupu za jednostkę miary.

##### Edycja BO

Dokument BO może podlegać wielokrotnym zmianom. Dokument jest dostępny do edycji do momentu jego zatwierdzenia.

Dla każdego produktu należy wprowadzić:
- cenę jednostkową netto zakupu (jeśli indeks posiada egzemplarze podać średnią cenę dla wszystkich egzemplarzy),
- ilość jednostek (jeśli indeks posiada przypisane egzemplarze zmiana ilości jednostek jest możliwa jedynie poprzez dodawanie lub usuwanie egzemplarzy z dokumentu BO),
- wartość netto wszystkich jednostek

Edycja dodanego produktu możliwa jest poprzez uruchomienie ikonki 'Edytuj' znajdującej się w wierszu produktu.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-51.png)

Jeśli edytujemy produkt z egzemplarzami możemy podać cenę netto jednego egzemplarza lub wartość wszystkich egzemplarzy, które zostały dodane. Ilość jest uzupełniana automatycznie w zależności od tego ile egzemplarzy mamy na dostępnej liście. Egzemplarz możemy usunąć z listy co spowoduje, że powróci na listę wyboru dostępnych egzemplarzy i zmieni się ilość produktu.

Pod wpływem zmian w jednym polu pozostałe wyliczają się automatycznie.

Koniecznie należy uruchomić akcję 'Zapisz' dostępną na końcu wiersza produktu. Jeśli tego nie zrobimy zmiany wprowadzone na pozycji znikną i trzeba będzie edycję produktu wykona od początku.

Jeśli usuwamy z dodanych pozycji produkt posiadający egzemplarze to usuwany jest on wraz ze wszystkimi dodanymi w BO egzemplarzami.

##### Usuwanie BO

Usunąć można jedynie niezatwierdzony dokument BO.

##### Zatwierdzanie BO

Ważne:
- Przed zatwierdzeniem BO należy usunąć wszystkie produkty, z zerowymi ilościami.
- Przed zatwierdzeniem BO należy zweryfikować wszystkie produkty, z zerowymi cenami.
- Zatwierdzenie dokumentu BO dla firmy powoduje, że wprowadzone w nim stany magazynowe zaczynają obowiązywać.

Po zatwierdzeniu dokumentu uzupełnione zostały stany magazynowe.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-52.png)

##### Uwagi

Po rozpoczęciu wystawiania dokumentów magazynowych naprawa błędów w BO może okazać się niemożliwa nawet z pominięciem interfejsu użytkownika dlatego zaleca się jego skrupulatną weryfikację przed zatwierdzeniem. To samo dotyczy dokumentu PZ użytego do zrobienia bilansu otwarcia.

W dowolnym momencie można dodać do magazynu kolejną firmę. Dla takiej nowej firmy podczas tworzenia BO do dokumentu będą mogły trafić wszystkie indeksy bez egzemplarzy oraz indeksy z egzemplarzami, które to egzemplarze jeszcze nigdy nie były powiązane z żadnym zatwierdzonym dokumentem  magazynowym.
