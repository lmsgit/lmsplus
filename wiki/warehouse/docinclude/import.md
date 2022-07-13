
## Import (od wersji > 1.9.4)

Funkcja importu umożliwia zaczytanie do magazynu produktów, usług oraz egzemplarzy produktu z plików _.csv_, _.xls_, _.ods_, _.xlsx_.

###### Informacje wstępne

- Aby uruchomić procedurę importu należy z menu głównego z sekcji "Magazyn" wybrać "Import".
- Funkcja dostępna jest jedynie dla użytkownika z rolą "(MAGAZYN) Administracja magazynem".
- Proces importu przebiega w dwóch etapach. W pierwszym etapie następuje walidacja struktury pliku importu i danych w pliku. Po pomyślnej walidacji danych możliwy jest import danych.
- Importować można dane tylko z jednego pliku. Dla plików _.xls_, _.ods_, _.xlsx_ importowane są dane wyłącznie z pierwszego arkusza.
- Plik importu może zawierać jedynie określony zestaw pól, który zależy od typu importu.
- Każdy plik powinien zawierać nagłówek określający nazwy pól.
- Kolejność pól w nagłówku pliku powinna odpowiadać kolejności pól w poszczególnych wierszach pliku.
- Kolejność pól w pliku importu jest dowolna.
- Oprócz pól obowiązkowych i opcjonalnych inne pola nie są dozwolone.
- Jeśli proces walidacji danych przebiegnie pomyślnie zostaną wyświetlone dane w formie w jakiej będą zaimportowane do bazy danych, aby przed uruchomieniem importu ostatecznie poddać je ocenie co do prawidłowości.
- Jeśli w procesie walidacji danych zostaną wykryte błędy, to dla każdego błędnego wiersza z pliku zostaną one wyświetlone w dodatkowej kolumnie, co ułatwia ich lokalizację i eliminację.
- Aby zaimportować plik, proces walidacji musi zakończyć się bez błędów.
- W procesie samego importu mogą pojawić się błędy SQL ponieważ nie wszystko można sprawdzić na etapie walidacji. Jednak akcja importu objęta jest transakcją bazodanową, zatem można powiedzieć, że albo wczyta się wszystko z pliku albo nic (Niekoniecznie może to być prawdziwe dla bazy danych MySQL).
- Pola obowiązkowe muszą znaleźć się w pliku i musi być podana wartość pola w wierszu pliku.
- Pola opcjonalne mogą, ale nie muszą znaleźć się w pliku, a wartość pola w wierszu pliku może, ale nie musi być podawana. Z tym, że jeśli pole znajdzie się w nagłówku pliku, to również musi znaleźć się w wierszu (niezależnie od tego czy ma wartość, czy nie).
- Dla każdego typu importu można podać zestaw danych domyślnych. Dane domyślne są ustawiane w przypadku kiedy brakuje ich w pliku.

Można przeprowadzić następujące typy importu danych:
- import produktów - pozwala zaimportować dane produktów,
- import egzemplarzy produktu - pozwala zaimportować dane egzemplarzy dla już istniejącego w bazie produktu,
- import usług - pozwala zaimportować dane usług,

###### Jak przygotować plik

Poniżej przykładowy plik z produktami, które chcemy zaimportować. Ponieważ pole "group" oraz "comment" są opcjonalne, dlatego w wierszu 2 i 3 nie zostały uzupełnione bo nie ma takiego obowiązku.

```
"r_n"|"symbol"|"barcode"|"name"|"tax"|"measure"|"taxcategory"|"guarantee_period"|"producer"|"group"|"pkwiu"|"sww"|"comment"
"1"|"PROD-ZNTS3B0BD964"|"B0BD964"|"PROD-SGN8601GR1B2007290896"|"23.00"|"szt."|"1"|"12"|"TEST1"|"Sieciowe"|"pkwiu-1"|"sww1"|"asd567"
"2"|"PROD-ZNTS3B0BD7C8"|"B0BD7C8"|"PROD-SGN8601GR1B2007290852"|"zw."|"szt."|"12"|"12"|"TEST1"|""|"pkwiu-2"|"sww2"|""
"3"|"PROD-ZNTS3B0BDBDE"|"B0BDBDE"|"PROD-SGN8601GR1B2007290853"|"22.00"|"szt."|"6"|"60"|"TEST1"|""|"pkwiu-3"|"sww3"|""
```

Jeśli dla takiego pliku podczas importu w formularzu importu ustawimy wartość domyślną dla grupy na "Inne", to dla każdego wiersza w którym brakuje wartości w polu _group_ zostanie wstawiona wartość "Inne".

Jeśli chcemy dla wszystkich wierszy ustawić wartość _group_ na "Sieciowe", to mamy dwie możliwości:
- dla każdego wiersza podajemy w polu _group_ wartość "Sieciowe",
- w ogóle nie wstawiamy do pliku kolumny _group_, ale w formularzu importu wybieramy wartość domyślną dla pola _group_.

Jeśli dla każdego wiersza w ogóle nie chcemy podawać grupy produktu, wtedy po prostu w pliku nie podajemy pola _group_ i danych dotyczących tego pola. Możemy tak zrobić, bo jest to pole opcjonalne.

Powyższa zasada dotyczy wszystkich typów importu i obejmuje większość dopuszczalnych do użycia w imporcie pól.

###### Import produktów

Obowiązkowe pola pliku importu:
- 'r_n' - numer wiersza,
- 'name' - nazwa produktu,
- 'symbol' - symbol produktu,
- 'tax' - wartość podatku,
- 'measure' - nazwa jednostki miary (Musi być zdefiniowana w słowniku.),
- 'producer' - nazwa producenta (Pole jest obowiązkowe tylko jeśli zaznaczono "Dodaj do urządzeń sieciowych", w przeciwnym wypadku jest opcjonalne.).

Opcjonalne pola pliku importu:
- 'barcode' -kod kreskowy,
- 'group' - nazwa grupy produktu (musi być zdefiniowana w słowniku),
- 'pkwiu',
- 'sww',
- 'comment' - komentarz,
- 'taxcategory'- kod kategorii podatkowej (dostępne wartości w pliku _definitions.php_ w tablicy _$TAX_CATEGORIES_. Wartość _'0'_ oznacza brak kategorii.)
- "guarantee_period" - kod okresu gwarancyjnego (dostępne wartości w pliku _definitions.php_ w tablicy _$GUARANTEEPERIODS_.)
- 'producer' - nazwa producenta (Pole jest opcjonalne tylko jeśli nie zaznaczono "Dodaj do urządzeń sieciowych", w przeciwnym wypadku jest obowiązkowe.).

Poniżej przykładowy plik z produktami, które chcemy zaimportować.
```
"r_n"|"symbol"|"barcode"|"name"|"tax"|"measure"|"taxcategory"|"guarantee_period"|"producer"|"pkwiu"|"sww"|"comment"
"1"|"PROD-ZNTS3B0BD964"|"B0BD964"|"PROD-SGN8601GR1B2007290896"|"23"|"szt."|""|""|"DASAN"|"pkwiu-2"|"sww3"|"asd567"
"2"|"PROD-ZNTS3B0BD7C8"|"B0BD7C8"|"PROD-SGN8601GR1B2007290852"|"23"|"szt."|""|"12"|"ZTE"|"pkwiu-1"|"sww1"|"asd556"
"3"|"PROD-ZNTS3B0BDBDE"|"B0BDBDE"|"PROD-SGN8601GR1B2007290853"|"22"|"szt."|"6"|"12"|"DASAN"|"pkwiu-2"|"sww3"|"asd345"
```
Jak widać brakuje tam kolumny _group_ ponieważ jest opcjonalna, a w niektórych wierszach wartości dla pól _taxcategory_ oraz _guarantee_period_ są puste.

Chcemy, aby dla każdego produktu jaki znajduje się w pliku została przypisana grupa "Sieciowe", a w przypadku braku kategorii podatkowej lub okresu gwarancji zostały wstawione wartości domyślne.

1. Uzupełniamy formularz

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-227.png)

Zaznaczenie opcji "Dodaj do urządzeń sieciowych" oznacza, że chcemy aby produkty z pliku zostały jednocześnie dodane jako modele w urządzeniach sieciowych. Uruchamia to dodatkowe procesy walidacji danych i importu.

2. Wykonaj akcję "Walidacja".

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-228.png)

Na powyższym obrazku wyświetlona została próbka danych zatem walidacja przebiegła pomyślnie, a przycisk "Import" jest aktywny.

Poniżej przykład nieudanej walidacji:

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-229.png)

Jak widać zwrócone są odpowiednie komunikaty błędów, a przycisk "Importuj" nie jest aktywny.

3. Wykonaj akcję "Importuj".

Poniżej obrazek z wynikiem importu.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-300.png)

###### Import usług

Obowiązkowe pola pliku importu:
- 'r_n' - numer wiersza,
- 'name' - nazwa produktu,
- 'symbol' - symbol produktu,
- 'tax' - wartość podatku,
- 'measure' - nazwa jednostki miary (Musi być zdefiniowana w słowniku.).

Opcjonalne pola pliku importu:
- 'group' - nazwa grupy produktu (musi być zdefiniowana w słowniku),
- 'comment' - komentarz.

Poniżej przykładowy plik z usługami, które chcemy zaimportować.
```
'r_n';'symbol';'name'
'1';'U-ZNTS3B0BD964';'U-SGN8601GR1B2007290896'
'2';'U-ZNTS3B0BD7C8';'U-SGN8601GR1B2007290852'
'3';'U-ZNTS3B0BDBDE';'U-SGN8601GR1B2007290853'
```
W tym przypadku użyto znaku _;_ jako znaku separatora pól oraz znaku _'_ jako znaku ogranicznika pola. zatem formularz importu należy wypełnić jak poniżej.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-301.png)

Pozostałe etapy importu usług przebiegają identycznie jak dla importu produktów.

###### Import egzemplarzy produktu

Obowiązkowe pola pliku importu:
- 'r_n' - numer wiersza,
- 'item_name' - nazwa egzemplarza produktu,
- 'sn' - numer seryjny egzemplarza produktu,
- 'mac%i' - adres MAC,
- 'mac_label%i' - etykieta adresu MAC,
- 'mac_main%i' - określenie czy adres MAC ma być adresem podstawowym (wartość "1"), czy nie (wartość "0" lub pusta).

Pola dotyczące MAC są obowiązkowe tylko jeśli chcemy takie dane zaimportować w przeciwnym wypadku w ogóle nie umieszczamy tych pól w pliku importu.

Opcjonalne pola pliku importu:
- 'multipack_code' - kod opakowania zbiorczego,
- 'comment' - komentarz.

Istnieje możliwość dodania kilku adresów MAC dla egzemplarza. Jeśli zdecydujemy się na import adresów MAC to dodatkowo do obowiązkowych pól dołączą pola:
- 'mac%x' - adres MAC,
- 'mac_label%x' - etykieta adresu MAC,
- 'mac_main%x' - określenie czy adres MAC ma być adresem podstawowym (wartość "1"), czy nie (wartość "0" lub pusta),

gdzie _%x_ to numer MAC. Zatem jeśli chcemy wczytać jeden adres MAC, to musimy dodać pola `"mac1"|"mac_label1"|"mac_main1"`. Natomiast jeśli chcemy dodać 2 adresy MAC, to musimy dodać pola `"mac1"|"mac_label1"|"mac_main1"|"mac2"|"mac_label2"|"mac_main2"`, itd.

Uwagi do adresów MAC:
- Każdy pole "mac%x" musi mieć unikalną wartość w obrębie bazy danych.
- Każdy pole "mac_label%x" musi mieć unikalną wartość na poziomie egzemplarza.
- Pole "mac_main%x" na poziomie egzemplarza może przyjąć wartość "1" tylko dla jednego pola "mac_main%x", lub przyjąć wartość "0" lub pustą dla wszystkich pól "mac_main%x". Inaczej mówiąc tylko jeden MAC możemy ustawić jako podstawowy.

Poniżej przykładowy plik z egzemplarzami, które chcemy zaimportować do wybranego produktu.
```
"r_n"|"item_name"|"sn"|"mac1"|"mac_label1"|"mac_main1"|"mac2"|"mac_label2"|"mac_main2"|"mac3"|"mac_label3"|"mac_main3"|"multipack_code"
"1"|"ZNTS3B0BD964"|"SGN8601GR1B2007290896"|"78303B0BD964"|"WAN"|"1"|"78303B0BDB01"|"LAN"|""|"78303B0BDB36"|"WAN1"|""|"S4T-1"
"2"|"ZNTS3B0BD7C8"|"SGN8601GR1B2007290852"|"78303B0BDBA9"|"WAN"|"1"|"78303B0BD7F2"|"LAN"|""|"78303B0BD7EF"|"WAN1"|""|"S4T-1"
"3"|"ZNTS3B0BDBDE"|"SGN8601GR1B2007290853"|"78303B0BDBDE"|"WAN"|"1"|"78303B0BDA83"|"LAN"|""|"78303B0BDBCB"|"WAN1"|""|"S4T-1"
```
Należy zwrócić uwagę, że w tym przypadku importujemy dla każdego egzemplarza trzy różne adresy MAC, a jednocześnie dla każdego egzemplarza pierwszy adres MAC będzie adresem podstawowym. Nie chcemy dodawać komentarza dla wszystkich egzemplarzy, zatem nie umieszczamy pola "comment", bo jest fakultatywne.

1. Uzupełnij formularz

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-302.png)

Zaznaczenie opcji "Dodaj do urządzeń sieciowych" oznacza, że chcemy aby egzemplarze produktu zostały jednocześnie dodane jako urządzenia sieciowe. Uruchamia to dodatkowe procesy walidacji danych i importu.

2. Wykonaj akcję "Walidacja".

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-303.png)

Na powyższym obrazku wyświetlona została próbka danych zatem walidacja przebiegła pomyślnie, a przycisk "Import" jest aktywny.

3. Wykonaj akcję "Importuj".

Poniżej obrazek z wynikiem importu.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-304.png)

**UWAGI:**
- Walidacja danych nie uwzględnia sytuacji kiedy użytkownik dane umieści w niewłaściwych polach, np. w polu "item_name" poda numery seryjne. Z tego powodu przed uruchomieniem opcji importu należy bardzo dokładnie sprawdzić wyświetloną próbkę danych, jaką otrzymamy po udanej walidacji, aby zweryfikować umiejscowienie danych oraz same dane.
- W przypadku importu bardzo dużej ilości wierszy proces walidacji i importu może trwać długo i zakończyć się niepowodzeniem, dlatego zalecane jest podzielenie jednego pliku na kilka mniejszych. Wielkość cząstkowych plików pozostaje w decyzji użytkownika, ale każdy z plików musi spełniać opisane w instrukcji wymagania.
