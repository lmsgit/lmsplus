## Zakup usług ZU

Zakup usług ZU jest wirtualnym dokumentem magazynowym przeznaczonym do ewidencjonowania usług zakupowanych przez przedsiębiorstwo. Może on operować wyłącznie na wirtualnych magazynach.

W swojej działalności przedsiębiorstwo prowadzi różnego rodzaju inwestycje. Z pomocą pluginu firma może odpowiednio ewidencjonować materiały jakie kupuje i jakie zużywa na potrzeby tych inwestycji. Najczęściej rozwiązywane jest to poprzez utworzenie oddzielnego magazynu dla każdej inwestycji i przepuszczanie towaru powiązanego z inwestycją tylko przez magazyn do inwestycji. Daje to możliwość łatwego i przejrzystego kontrolowania zużycia materiałów na inwestycję i ich kosztów. Kosztami inwestycji są również różnego rodzaju usługi świadczone przez podmioty zewnętrzne np. roboty budowlane, dzierżawa działek, przygotowanie map, projekty, transport itp. Właśnie te koszty usług możemy przy pomocy dokumentu ZU ewidencjonować w magazynie. Dzięki temu w jednym miejscu mamy zebrane i uporządkowane informacje o przebiegu i kosztach inwestycji.

Dokument ZU jest dokumentem wirtualnym ponieważ nie generuje on żadnych obrotów magazynowych. Jest to jedynie ewidencja pomocnicza, która nie musi być raportowana w żaden sposób. Mechanizm ten służy jedynie pomocy przedsiębiorcy i jego używanie nie jest obowiązkowe.

Niniejsza instrukcja ma na celu zobrazowanie zastosowania ewidencji zakupionych usług.

Na potrzeby tej instrukcji przyjmiemy założenie, że rozpoczęliśmy inwestycję budowy przyłącza o nazwie kodowej 'WW-123' i w związku z tym musieliśmy kupić następujące materiały, na które dostaliśmy właśnie faktury zakupu od dostawcy "ARBUCKLE":
- studnia o nazwie "Studnia SKR" w ilości 3 szt. i cenie 200zł netto za sztukę
- mikrokabel o nazwie "Mikrokabel FO BKT" w ilości 3 km. i cenie 800zł netto za kilometr
- mikrorurka o nazwie "Mikrorurka DB 12x2" w ilości 3 km. i cenie 700zł netto za kilometr

oraz dostaliśmy faktury od podmiotów zewnętrznych z tytułu świadczenia następujących usług:
- transport w wysokości 120 zł netto od kontrahenta "ARBUCKLE"
- opracowanie projektu budowy przyłącza w wysokości 1500 zł netto od kontrahenta "CHATFIELD"

##### Utworzenie usług

Wymienionych towarów nie mamy jeszcze wprowadzonych do katalogu produktów ([Katalog produktów](produkt_wyjasnienie.md)) więc musimy je dodać. Wszystkie wymienione powyżej towary będziemy ewidencjonować jako produkty bez egzemplarzy ([Tworzenie produktu bez egzemplarzy](produkt_bez_egz.md)).

Wymienionych usług nie mamy jeszcze wprowadzonych do katalogu usług ([Katalog usług](katalog_uslug.md)) więc musimy je dodać ([Tworzenie usługi](usluga.md)).

##### Utworzenie magazynów

Chcemy wydzielić ewidencję produktów i usług powiązanych z naszą fikcyjną inwestycją 'WW-123' od ewidencji pozostałego asortymentu magazynowego. W tym celu będziemy musieli stworzyć dwa magazyny ([Magazyny](magazyny.md)):

- magazyn o nazwie "Inwestycja WW-123" i symbolu "WW-123", który będzie typem "Magazyn zwykły". Przeznaczymy go do ewidencji materiałów zużywanych na potrzeby inwestycji.
- magazyn o nazwie "Inwestycja-ZU WW-123" i symbolu "WW-123-ZU", który będzie typem "Magazyn do ewidencji operacji wirtualnych". Przeznaczymy go do ewidencji zakupu usług na potrzeby inwestycji.

Poniżej lista utworzonych magazynów.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-189.png)

##### Nadanie uprawnień

Aby zrealizować proces użytkownik będzie potrzebował odpowiednich uprawnień do dokumentów PZ, RW i ZU oraz uprawnień do magazynów przeznaczonych na inwestycję ([Uprawnienia](uprawnienia.md)).

##### Przyjęcie produktów na magazyn "Inwestycja WW-123"

Przyjęcia na magazyn "Inwestycja WW-123" dokonujemy dokumentem PZ. Instrukcja tworzenia PZ tutaj: [Przyjęcie zewnętrzne (PZ)](dokument_pz.md)

Poniżej widok zatwierdzonego dokumentu PZ oraz stan magazynowy wprowadzonych produktów.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-190.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-191.png)

##### Wprowadzenie usług na magazyn "Inwestycja-ZU WW-123"

Przyjęcia usług na magazyn "Inwestycja-ZU WW-123" dokonujemy dokumentem ZU. Odbywa się to analogicznie jak wystawianie dokumentu PZ, z tą różnicą, że dodajemy do dokumentu usługi a nie produkty. Ponieważ mamy dwóch różnych dostawców usług będziemy musieli zrobić 2 dokumenty ZU.

- Z menu głównego wybierz "Magazyn-dokumenty->ZU".
- Uruchom przycisk "Dodaj dokument".

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-192.png)

- Uzupełnij wymagane informacje i zapisz.
- Uzupełnij dokument o odpowiednie pozycje i zatwierdź dokument.

Poniżej widok zatwierdzonego dokumentów ZU.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-193.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-194.png)

Dokumenty ZU nie generują stanów magazynowych, o których mówimy w przypadku produktów. Możemy jedynie śledzić ilość i wartość zakupionych usług.

Należy przejść do menu głównego i uruchomić "Magazyn->Zakup usług". Zestawienie funkcjonuje analogicznie jak kartoteka "Stany magazynowe" dla produktów.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-195.png)

##### Wydanie produktów do realizacji inwestycji

Chcemy teraz wydać wszystkie produkty z magazynu "Inwestycja-ZU WW-123" na potrzeby realizacji inwestycji. Żeby taki rozchód zaewidencjonować w magazynie musimy wystawić dokument rozchodowy i do tego celu użyjemy dokumentu RW. Pomocna będzie w tym ta instrukcja: [Rozchód wewnętrzny i korekta rozchodu (RW) (RWk)](dokument_rw.md).

Poniżej widok utworzonego dokumentu RW oraz stanów magazynowych po tej operacji.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-196.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-197.png)

Uwaga: Nie musimy tworzyć od razu jednego RW na wszystko. Możemy materiały na realizację inwestycji wydawać z magazynu partiami i do każdej partii tworzyć RW z magazynu inwestycji.

##### Podsumowanie

W dowolnej chwili możemy teraz śledzić koszt inwestycji i rozchód materiałów. Ze slajdów poniżej możemy od razu wywnioskować, że jak na razie na inwestycje wydaliśmy 5100zł+1620zł=6720zł netto. Nasz księgowy też będzie zadowolony kiedy będziemy wszystkie dokumenty związane z inwestycją przekazywać spójnie powiązane.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-198.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-199.png)
