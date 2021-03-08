## Synchronizacja

Dla lepszego zrozumienia procesu synchronizacji można zapoznać się z informacją czym są produkty w magazynie ([Katalog produktów](produkt_wyjasnienie.md)).

Prowadzenie ewidencji magazynowej opiera się na tworzeniu odpowiednich dokumentów magazynowych obrazujących przychody i rozchody towaru w magazynach. Na każdym dokumencie, który będziemy wystawiać, musimy umieścić listę produktów, których rozchód lub przychód dokumentujemy. Żeby dodać produkt do listy produktów w dokumencie musimy wybrać go z listy produktów, która to lista pochodzi z katalogu produktów. Zatem można powiedzieć, że jeśli produktu nie ma w katalogu to nie może on zostać dodany do dokumentu magazynowego.

Załóżmy, że chcielibyśmy wystawić dokument magazynowy na jakieś urządzenie sieciowe, które mamy w osprzęcie sieciowym. Ponieważ takiego urządzenia nie mamy w katalogu produktów w magazynie, nie będzie możliwe dodanie takiej pozycji do dokumentu, a przez to jego ewidencja w magazynie staje się niemożliwa. Dzięki synchronizacji możemy automatycznie utworzyć w katalogu produktów produkt, który będzie posiadał podstawowe cechy naszego urządzenia sieciowego i będzie wskazywał na to urządzenie w osprzęcie sieciowym.

Przykład: Mamy w osprzęcie sieciowym urządzenia sieciowe należące do producenta 'DASAN' i reprezentujące ten sam model urządzeń 'H660G'. Wiemy również, że każde urządzenie sieciowe możemy jednoznacznie zidentyfikować po numerze seryjnym. Możemy powiedzieć, że każde wyświetlone urządzenie jest egzemplarzem modelu 'H660G'. Wiemy, że urządzenie sieciowe w osprzęcie sieciowym od razu wykazuje się pewnymi cechami towaru. Posiada przypisanego producenta, model i numer seryjny. Synchronizacja mapuje te cechy na cechy produktu w magazynie.

Mapowanie odbywa się etapowo:
- etap 1 - mapowanie producenta z osprzętu sieciowego na producenta w magazynie,
- etap 2 - mapowanie modelu z osprzętu sieciowego na produkt w magazynie,
- etap 3 - mapowanie urządzenia sieciowego z osprzętu sieciowego na egzemplarz produktu w magazynie.

Naszym celem jest osiągnięcie etapu 3 przy czym jest to możliwe jedynie jeśli etap 1 i 2 zakończą się powodzeniem.

Synchronizacja może przebiegać w formie:
- masowej - jedną akcją synchronizuje się wiele urządzeń - synchronizacja działa jednokierunkowo i pomaga jedynie w przeniesieniu osprzętu sieciowego do magazynu. Nie ma zastosowania w przypadku przenoszenia indeksów magazynowych do osprzętu sieciowego ([Synchronizacja masowa](synchronizacja_masowa.md)),
- selektywnej - każde z: producenta, modelu lub urządzenia sieciowego, można synchronizować indywidualnie ([Synchronizacja selektywna](synchronizacja_selektywna.md)).

W wyniku synchronizacji urządzeń sieciowych znajdujących się w osprzęcie sieciowym otrzymujemy zawsze 'produkty z egzemplarzami' w magazynie.

###### Podsumowanie

Celem operacji synchronizacji OS z MAG jest wprowadzenie urządzeń sieciowych do magazynu jako produkty. Ten proces tworzy powiązanie pomiędzy produktem w MAG a urządzeniem sieciowym w OS i pozwala ewidencjonować osprzęt sieciowy przy pomocy magazynu.

Operacja synchronizacji nie wpływa w żaden sposób na dotychczasowe działanie OS.

##### Uwagi

- W przypadku kiedy w tabeli _taxes_ istnieje wiele rekordów gdzie pole _value=23.00_ to przed rozpoczęciem synchronizacji należy zwrócić szczególną uwagę na wartości zmiennej konfiguracyjnej _default_sync_taxid_, która jest tworzona w procesie instalacji pluginu. Każdy model osprzętu sieciowego, który będziemy chcieli przenieść do magazynu jako produkt, będzie dla nowego produktu domyślnie ustawiał wartość podatku na podstawie tej zmiennej. Domyślna wartość dla _default_sync_taxid_ jest ustawiana na wartość pola _ID_ z tabeli _taxes_ gdzie pole _value_ jest równe _23.00_. W LMS może istnieć wiele podatków o polu _value=23.00_ i każdy może być aktywny w chwili instalacji pluginu więc instalator pluginu nie może podjąć decyzji, który ma być prawidłowy, dlatego domyślnie wybiera on ostatnio dodany podatek o wartości _23_. Należy to ustawienie sprawdzić i ewentualnie ustawić odpowiednie _ID_.
- Jeśli z MAG usuwamy producenta powiązanego z producentem w OS to jest on usuwany wyłącznie z MAG. Producent w OS pozostaje nieruszony. Taka operacja jedynie usuwa powiązanie.
- Jeśli z MAG usuwamy produkt powiązany z modelem w OS to jest on usuwany wyłącznie z MAG. Model w OS pozostaje nieruszony. Taka operacja jedynie usuwa powiązanie.
- Jeśli z MAG usuwamy egzemplarz produktu powiązany z urządzeniem sieciowym w OS to jest on usuwany wyłącznie z MAG. Model w OS pozostaje nieruszony. Taka operacja jedynie usuwa powiązanie.
- Jeśli z OS usuwamy producenta powiązanego z producentem w WH to najpierw musimy usunąć producenta w WH (usunąć powiązanie), a dopiero potem usunąć producenta z OS.
- Jeśli z OS usuwamy model powiązany z produktem w WH to najpierw musimy usunąć produkt w WH (usunąć powiązanie), a dopiero potem usunąć model z OS.
- Jeśli z OS usuwamy urządzenie sieciowe powiązane z egzemplarzem produktu w WH to najpierw musimy usunąć egzemplarz produktów w WH (usunąć powiązanie), a dopiero potem usunąć urządzenie sieciowe z z OS.
- Jeśli producent w WH jest powiązany z OS to zmiana nazwy producenta po stronie WH skutkować będzie zmianami nazwy producenta w OS i na odwrót.
- Jeśli produkt w WH jest powiązany z modelem w OS to zmiana nazwy produktu po stronie WH skutkować będzie zmianami nazwy modelu w OS i na odwrót.
- Jeśli egzemplarz produktu w WH jest powiązany z urządzeniem sieciowym w OS to zmiana nazwy i numeru seryjnego egzemplarza produktu po stronie WH skutkować będzie zmianami nazwy i numeru seryjnego urządzenia sieciowego w OS i na odwrót.
- Unikalność nazwy egzemplarza jest na poziomie produktu tzn. ta sama nazwa egzemplarza nie może być użyta w ramach jednego produktu ale może być użyta dla innego produktu. Zalecane jest jednak utrzymywanie unikalności nazwy egzemplarzy na poziomie całego magazynu.
- Nazwy producentów, produktów i egzemplarzy w WH są niewrażliwe na wielkość liter np. nazwa 'device' , 'DEVICE' i 'Device' są traktowane jako takie same.

