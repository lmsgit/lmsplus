##  Katalog produktów

Prowadzenie ewidencji magazynowej opiera się na tworzeniu odpowiednich dokumentów magazynowych obrazujących przychody i rozchody towaru w magazynach. Na każdym dokumencie, który będziemy wystawiać, musimy umieścić listę produktów, których rozchód lub przychód dokumentujemy. Żeby dodać produkt do listy produktów w dokumencie musimy wybrać go z listy produktów, która to lista pochodzi z katalogu produktów. Zatem można powiedzieć, że jeśli produktu nie ma w katalogu produktów to nie może on zostać dodany do dokumentu magazynowego.

##### Czym jest produkt w katalogu produktów.

Produkt można traktować jako opis cech towaru, tzw. kartę towaru.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-9.png)

Istnienie produktu w katalogu stanowi pewnego rodzaju deklarację z naszej strony, że produkt będziemy chcieli ewidencjonować. To, że produkt znajduje się w katalogu produktów nie oznacza, że podlega ewidencji. Podlegać jej zaczyna dopiero kiedy zostanie wprowadzony na magazyn dokumentem przyjęcia (PZ lub BO). Wtedy jego określona ilość, po określonej cenie, zostaje dodana do określonego magazynu. Wtedy też może być poddany kolejnym procesom magazynowym.

W magazynie możemy wyróżnić dwa typy produktów:
- produkt z egzemplarzami
- produkt bez egzemplarzy

Dodatkowo produkt może być:
- powiązany z osprzętem sieciowym
- niepowiązany z osprzętem sieciowym

**Uwaga!**
- Jeśli podczas tworzenia pierwszego dokumentu przyjęcia (PZ lub BO) produkt nie miał przypisanych egzemplarzy, to ten produkt przez cały czas użytkowania w magazynie będzie widziany jako produkt bez egzemplarzy,
- Jeśli podczas tworzenia pierwszego dokumentu przyjęcia (PZ lub BO) produkt miał przypisane egzemplarze, to ten produkt przez cały czas użytkowania w magazynie będzie widziany jako produkt z egzemplarzami.

##### Produkty powiązane z osprzętem sieciowym (produkty z egzemplarzami)

Istotę tego typu produktów opisują następujące artykuły:

[Czym jest synchronizacja?](synchronizacja_wyjasnienie.md)

[Synchronizacja masowa](synchronizacja_masowa.md)

[Synchronizacja selektywna](synchronizacja_selektywna.md)

Produkty powiązane z osprzętem sieciowym są zawsze produktami z egzemplarzami.

##### Produkty z egzemplarzami

Istotę tego typu produktów opisują następujące artykuły:

[Czym jest synchronizacja?](synchronizacja_wyjasnienie.md)

[Synchronizacja masowa](synchronizacja_masowa.md)

[Synchronizacja selektywna](synchronizacja_selektywna.md)

Produkt z egzemplarzami może być powiązany z osprzętem sieciowym, ale nie musi.

[Tworzenie produktu z egzemplarzami niepowiązanego z OS](produkt_z_egz.md)

##### Produkty bez egzemplarzy

[Tworzenie produktu bez egzemplarzy](produkt_bez_egz.md)

Przykład: Chcemy prowadzić sprzedaż produktu o nazwie 'RouterA'. Zakładamy że sprzedając klientowi router nie interesuje nas, który egzemplarz dostanie. Ważne żeby to był router 'RouterA'. W takim przypadku tworzymy produkt bez egzemplarzy. Dla takiego typu produktu w magazynie nigdzie nie zostanie przechowana informacja jaki SN miał 'RouterA' kupiony przez klienta.

Produkt bez egzemplarzy stosujemy również dla towaru takiego jak kable, złączki, haki, etc.

##### Czy muszę tworzyć oddzielne produkty w katalogu produktów dla różnych firm?

Nie. Katalog produktów jest wspólny dla wszystkich firm. Dopiero w momencie tworzenia dokumentu magazynowego określamy jaka ilość, w jakiej cenie jest wydawana z magazynu bądź przyjmowana na magazyn konkretnej firmy.


##### Kiedy stosować produkt z egzemplarzami, który nie jest powiązany z OS.

Przykład: Prowadzimy sprzedaż bardzo popularnego na rynku routera o nazwie 'RouterA'. W urządzeniach sieciowych nie przechowujemy informacji o tych routerach, czyli mamy produkt niepowiązany z OS. Sprzedajemy klientowi 'RouterA' a po 2 dniach klient przychodzi do nas i mówi, że router nie działa. Klient jednak zataił, że nie jest to ten router, który kupił od nas ale jest to router sąsiada który był kupiony w innej firmie. Zgadza się tylko model routera, ale numer seryjny jest inny. W takiej sytuacji:
- jeśli w magazynie 'RouterA' był produktem bez egzemplarzy nie będziemy mogli stwierdzić jaki numer seryjny został sprzedany dla klienta i dlatego nie jesteśmy zabezpieczeni przed takim oszustwem. Będziemy jedynie wiedzieć że taki produkt sprzedaliśmy.
- jeśli w magazynie 'RouterA' był produktem z egzemplarzami podczas sprzedaży zostanie zarejestrowany numer seryjny sprzedanego urządzenia i jesteśmy zabezpieczeni przed tego typu oszustwami. Należy jednak pamiętać, żeby w momencie sprzedaży wydrukować WZ z egzemplarzem, bez cen i dać do podpisu dla klienta ponieważ na FV drukowana jest tylko nazwa produktu, a nie pojawia się SN egzemplarza.

Generalnie produkt z egzemplarzami stosujemy w momencie kiedy chcemy rejestrować w magazynie operacje na każdym egzemplarzu.

##### Uwagi:

- Usuwanie produktu jest możliwe wyłącznie jeśli nie posiada przypisanych egzemplarzy i cen sprzedaży oraz nie był dodany do dokumentu magazynowego.
- Usuwanie egzemplarza produktu jest możliwe wyłącznie jeśli nie był dodany do dokumentu magazynowego.
- Jeśli z MAG usuwamy producenta powiązanego z producentem w OS to jest on usuwany wyłącznie z MAG. Producent w OS pozostaje nieruszony. Taka operacja jedynie usuwa powiązanie.
- Jeśli z MAG usuwamy produkt powiązany z modelem w OS to jest on usuwany wyłącznie z MAG. Model w OS pozostaje nieruszony. Taka operacja jedynie usuwa powiązanie.
- Jeśli z MAG usuwamy egzemplarz produktu powiązany z urządzeniem sieciowym w OS to jest on usuwany wyłącznie z MAG. Model w OS pozostaje nieruszony. Taka operacja jedynie usuwa powiązanie.
- Jeśli producent w WH jest powiązany z OS to zmiana nazwy producenta po stronie WH skutkować będzie zmianami nazwy producenta w OS i na odwrót.
- Jeśli produkt w WH jest powiązany z modelem w OS to zmiana nazwy produktu po stronie WH skutkować będzie zmianami nazwy modelu w OS i na odwrót.
- Jeśli egzemplarz produktu w WH jest powiązany z urządzeniem sieciowym w OS to zmiana nazwy i numeru seryjnego egzemplarza produktu po stronie WH skutkować będzie zmianami nazwy i numeru seryjnego urządzenia sieciowego w OS i na odwrót.
- Unikalność nazwy egzemplarza jest na poziomie produktu tzn. ta sama nazwa egzemplarza nie może być użyta w ramach jednego produktu ale może być użyta dla innego produktu. Zalecane jest jednak utrzymywanie unikalności nazwy egzemplarzy na poziomie całego magazynu.
- Nazwy producentów, produktów i egzemplarzy w WH są niewrażliwe na wielkość liter np. nazwa 'device' , 'DEVICE' i 'Device' są traktowane jako takie same.
