## Ceny sprzedaży produktów

Dla każdego produktu w katalogu produktów możemy ustalić politykę cenową braną pod uwagę podczas tworzenia dokumentu handlowego zawierającego pozycję magazynową.

##### Tworzenie rodzajów cen

Uruchom z menu głównego 'Magazyn-Słowniki->Rodzaje Cen'.

Do słownika ma dostęp jedynie użytkownik z pełnymi prawami lub rolą "Administrator magazynu".

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-165.png)

Ponieważ nie ma jeszcze zdefiniowanych rodzajów cen dodamy kilka. W tym celu uruchamiamy "Nowy rodzaj ceny".

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-166.png)

Podajemy nazwę, opis i zapisujemy.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-167.png)

Na liście rodzajów cen pojawiła się nowa cena. W ten sam sposób dodamy kolejne ceny na potrzeby instrukcji.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-168.png)

##### Definiowanie rodzajów cen dla produktu

Uruchom z menu głównego 'Magazyn->Katalog produktów'.
Wyszukaj produkt i kliknij w wiersz produktu, aby przejść do informacji o nim.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-164.png)

W zakładce "Rodzaje cen sprzedaży" uruchom "Dodaj rodzaj ceny".

**Cena netto powinna być wyższa niż potencjalna cena zakupu produktu.**

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-169.png)

Wybieramy rodzaj ceny, podajemy wartość netto lub brutto (przeliczanie automatyczne) i zapisujemy.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-170.png)

Cena została dodana jako cena domyślna.

Teraz na potrzeby instrukcji dodamy kolejno pozostałe ceny.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-171.png)

Domyślną cena sprzedaży netto jest cena detaliczna. Teraz w momencie kiedy będziemy tworzyć dokument handlowy będzie ona od razu podpowiadana w momencie wybrania produktu. Pracownik BOK nie będzie musiał się zastanawiać jaką cenę wprowadzić.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-172.png)

Jeśli zajdzie potrzeba zmiany rodzaju ceny domyślnej podpowiadanej do dokumentu handlowego należy tego dokonać z poziomu rodzajów cen produktu poprzez zmianę ceny domyślnej. Dla przykładu ustawimy jako cenę domyślną
cenę "Promocja".

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-171.png)

Klikamy na ikonkę edycji znajdującą się w wierszu z ceną.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-173.png)

Zaznaczamy "Domyślna cena sprzedaży" i zapisujemy.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-174.png)

Teraz cena "Promocja" będzie podpowiadana jako cena sprzedaży netto w dokumencie handlowym.

##### Uwagi

- Ze słownika nie można usuwać rodzaju ceny już użytej w produktach.
- Ceny domyślnej nie można usunąć. Trzeba najpierw ustawić inną cenę jako domyślną a następnie usunąć cenę.
- Tylko cena domyślna może być podpowiadana na dokumencie handlowym. Wyjątkiem jest sytuacja kiedy tworzymy fakturę na podstawie WZ. Wtedy jest podpowiadana cena sprzedaży z dokumentu WZ, jeśli była podana, jeśli nie podpowiadana jest cena domyślna sprzedaży.
- Definiowanie cen nie jest obowiązkowe. W przypadku braku ceny domyślnej sprzedaży ceny nie będą podpowiadane na dokumencie handlowym.
