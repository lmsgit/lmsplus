## Tworzenie produktu powiązanego z OS

#### Metoda 1

- Z menu głównego uruchom Magazyn->Nowy produkt.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-30.png)

- Wprowadź nazwę i symbol produktu.
- Producent - jeśli brakuje odpowiedniego dodaj go do słownika (Magazyn-słowniki->Producenci). Producent musi być powiązany z producentem z osprzętu sieciowego. Jeśli nie będzie nie załaduje się lista modeli w polu 'Powiąż z modelem urządzeń sieciowych'.
- Uzupełniaj 'Powiąż z modelem urządzeń sieciowych' poprzez wybranie modelu z osprzętu sieciowego.
- Uzupełnij 'Prefiks nazwy egzemplarza' (jest to opcjonalne - prefix będzie automatycznie wstawiany do nazwy każdego egzemplarza produktu). Jeśli brakuje odpowiedniego prefiksu dodaj go do słownika (Magazyn-słowniki->Prefiksy).
- Pozostałe pola są opcjonalne, ale niektóre z nich wymagają uwagi:
  - Jednostka miary - jeśli brakuje odpowiedniej jednostki dodaj ją do słownika (Magazyn-słowniki->Jednostki miar). Zwróć uwagę, aby wybrać odpowiednią jednostkę do towaru,
  - Grupa - jeśli brakuje odpowiedniej grupy dodaj ją do słownika (Magazyn-słowniki->Grupy). Uzupełnienie nie jest obowiązkowe ale pozwala lepiej kategoryzować produkty.
  - Kategoria podatkowa - poprzez odpowiednią konfigurację można wymusić jej wprowadzanie. Warto jest to pole uzupełnić ponieważ wartość tego pola będzie się automatycznie podpowiadać podczas wystawiania faktury na produkt.
- Zapisz.

Po zapisaniu symbol produktu nie podlega edycji.

Teraz możemy przejść do dodawania egzemplarzy.

###### Dodawanie egzemplarzy

Uruchom 'Katalog produktów' i z pomocą filtra wyszukaj produkt.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-31.png)

Dodawanie egzemplarza można rozpocząć po kliknięciu ikonki 'Dodaj egzemplarz' znajdującej się w wierszu produktu. Można też przejść do karty informacyjnej produktu (kliknij w wiersz z produktem) i z tego poziomu dodawać egzemplarze klikając przycisk 'Dodaj egzemplarz'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-32.png)

Obie metody prowadzą do tego samego formularza dodawania egzemplarza.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-33.png)

Musimy wprowadzić nazwę egzemplarza oraz numer seryjny. Ponieważ dla produktu 'H665G' pole 'Prefiks nazwy egzemplarza' mamy ustawione na 'ROUTER-' będzie to zawsze dodawane do nazwy każdego egzemplarza produktu 'H665G'. Do wprowadzania nazwy i symbolu można użyć czytnika kodów kreskowych.

Zaznacz opcję 'Dodaj do urządzeń sieciowych'.

Ponieważ jednocześnie chcemy dodać kilka urządzeń zaznaczamy opcję 'wyświetl ten formularz ponownie po zapisie'.

Poniżej wynik dodania trzech urządzeń. Jak widać uzupełniła się lista egzemplarzy produktu.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-34.png)

Ikonka 'Pokaż w urządzeniach sieciowych' przy produkcie informuje, że produkt jest powiązany z modelem w OS, a w przypadku egzemplarza informuje, że egzemplarz jest powiązany z urządzeniem sieciowym w OS

W momencie kiedy będziemy kupować kolejne urządzenia tego produktu nie musimy tworzyć nowego produktu tylko dodać urządzenia do egzemplarzy produktu w sposób opisany powyżej.

#### Metoda 2

Utwórz produkt i egzemplarze zgodnie z tą instrukcją [Tworzenie produktu z egzemplarzami niepowiązanego z OS](produkt_z_egz.md). Wyniki tej operacji na poniższym rysunku.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-35.png)

Należy teraz powiązać produkt z modelem z OS.

Jeśli w OS nie istnieje model o takiej nazwie jak nazwa produktu kliknij ikonkę 'Dodaj do urządzeń sieciowych', która znajduje się przy produkcie, aby utworzyć nowy model o nazwie produktu i powiązać z nim produkt.

Jeśli w OS już istnieje model o takiej nazwie jak nazwa produktu przejdź do edycji produktu i w polu 'Powiąż z modelem urządzeń sieciowych' wskaż model z OS, z którym chcesz powiązać produkt.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-36.png)

###### Dodawanie egzemplarzy

Kiedy produkt został powiązany z modelem w OS możesz przystąpić do dodawania egzemplarzy produktu jako urządzenia sieciowe w OS.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-37.png)

Dla egzemplarza kliknij ikonkę 'Dodaj do urządzeń sieciowych' pokazaną na rysunku powyżej. Lub przejdź do informacji o egzemplarzu (kliknij w wiersz z egzemplarzem) i tab uruchom przycisk 'Dodaj do urządzeń sieciowych' (rysunek poniżej).

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-38.png)

Po dodaniu egzemplarzy otrzymamy wynik z rysunku poniżej.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-39.png)
