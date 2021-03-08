## Inwentaryzacja IW

Funkcja Inwentaryzacji pozwala na uzgodnienie stanów magazynowych w programie ze stanem rzeczywistym magazynu.

Należy pamiętać o nadaniu odpowiednich uprawnień dla użytkownika do dokumentów IW i magazynu podlegającemu inwentaryzacji ([Uprawnienia](uprawnienia.md)).

UWAGI:

- Inwentaryzację należy przeprowadzić oddzielne dla każdego magazynu.
- Przed rozpoczęciem inwentaryzacji wszystkie dokumenty w magazynie muszą być zatwierdzone (dopilnowanie tego warunku należy do użytkownika).
- Od momentu utworzenia arkusza inwentaryzacji do momentu jego zatwierdzenia nie można wystawiać żadnych dokumentów powiązanych z magazynem na którym jest prowadzona inwentaryzacja.
- Inwentaryzacja rozpoczyna sie w momencie utworzenia arkusza inwentaryzacji i kończy w momencie jego zatwierdzenia.
- Inwentaryzacji podlegają tylko produkty, które znalazły się na arkuszu inwentaryzacji.

Inwentaryzację można przeprowadzać w dowolnym momencie o ile spełnione są powyższe uwagi.

Inwentaryzacja składa się z trzech etapów:
- Etap 1 – przygotowanie arkuszy inwentaryzacyjnych.
- Etap 2 – uzupełnienie stanów rzeczywistych towarów w magazynie.
- Etap 3 – zatwierdzeni arkusza (utworzenie dokumentów korygujących stany: IPW, IRW).

##### Tworzenie dokumentu arkusza inwentaryzacji (IW).

Uruchom z menu głównego 'Magazyn-dokumenty->IW'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-182.png)

Uruchom przycisk 'Dodaj dokument'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-183.png)

Uzupełnij kolejno:
- firmę,
- magazyn,
- plan numeracyjny.

Dodatkowo można wybrać opcje, które mają wpływ na wygląd i sposób wypełniania formularza arkusza inwentaryzacji.

###### Brak wybranych opcji

Jeśli nie zaznaczymy żadnej opcji utworzony zostanie arkusz spisowy w następującej postaci:

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-184.png)

Na takim arkuszu pojawiają się wszystkie produkty z magazynu, który podlega inwentaryzacji. Wśród nich mogą się też znaleźć produkty, które na magazynie mają zerowy stan (jeśli opcja "Bez stanów zerowych" nie jest zaznaczona). Na formularzu nie ma informacji o bieżącym stanie magazynowym więc uzupełnianie arkusza możemy przeprowadzić jedynie w oparciu o spis z natury.

Jest to najbardziej zbliżony do "podręcznikowego" sposób prowadzenia inwentaryzacji. Osoba wprowadzająca dane ze spisu z natury nie może się sugerować istniejącymi danymi magazynowymi, może jedynie wprowadzić stan rzeczywisty.

###### Opcja "Wypełnij arkusz"

Jeśli nie zaznaczymy żadnej opcji utworzony zostanie arkusz spisowy w następującej postaci:

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-185.png)

Na takim arkuszu pojawiają się wszystkie produkty z magazynu, który podlega inwentaryzacji. Wśród nich mogą się też znaleźć produkty, które na magazynie mają zerowy stan (jeśli opcja "Bez stanów zerowych" nie jest zaznaczona). Formularz jest wstępnie wypełniony informacjami o bieżącym stanie magazynowym. Uzupełnianie arkusza przeprowadzamy zawsze w oparciu o spis z natury jednakże wiedza o bieżącym stanie magazynowym może pomóc w wykryciu ewentualnych błędów w spisie z natury.

Bieżące stany magazynowe również pojawią się na wydruku arkusza przeznaczonego do spisu z natury.

Niedogodnością takiego arkusza jest fakt, że osoba wprowadzająca dane ze spisu z natury może się sugerować istniejącymi danymi magazynowymi, przez co może próbować fabrykować spis z natury. Zaletą z kolei jest to, że musimy zmienić tylko wartości w tych produktach, w których wystąpiły różnice pomiędzy stanem magazynowym a spisem z natury (jest to szczególnie przydatne w przypadku produktów z egzemplarzami).


###### Opcja "Bez stanów zerowych"

Powoduje, że dla każdej z opcji do arkusza spisowego nie trafią produkty, których stan magazynowy jest równy "0".

##### Uzupełnianie arkusza

Na potrzeby instrukcji wybierzemy stan z obrazka poniżej.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-183.png)

Po zapisaniu otrzymujemy następujący arkusz.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-186.png)

Wypełnianie formularza musimy przeprowadzić na podstawie spisu z natury. Aby taki arkusz wydrukować należy uruchomić "Drukuj"

Edycja ilości produktu możliwa jest po uruchomieniu ikonki "Edytuj" znajdującej się w wierszu z produktem.

Na liście pozycji na arkuszu widoczne są następujące kolumny:
- Ilość na arkuszu – stan, jaki wynika ze spisu produktu w rzeczywistości (wprowadzany przez użytkownika). W nowo utworzonym arkuszu należy uzupełnić to pole dla każdego produktu.
- Bieżąca ilość – stan produktu w magazynie w programie na chwilę utworzenia arkusza spisowego.

Jedynym polem jakie mamy do uzupełnienia jest pole "Ilość na arkuszu". W przypadku produktu z egzemplarzami ilość jest uzupełniana automatycznie w zależności od wartości pola "Ilość na arkuszu" dla każdego egzemplarza.

Koniecznie należy uruchomić akcję 'Zapisz' dostępną na końcu wiersza produktu. Jeśli tego nie zrobimy zmiany wprowadzone na pozycji znikną i trzeba będzie edycję produktu wykonać od początku.

Usuwanie produktów z arkusza jest niemożliwe.

##### Usuwanie IW

Usunąć można jedynie niezatwierdzony dokument IW. Przerywa to proces inwentaryzacji.

##### Zatwierdzanie arkusza inwentaryzacji.

Zatwierdzenie arkusza kończy proces inwentaryzacji i skutkuje utworzeniem odpowiednich dokumentów przychodu i rozchodu produktów. Dla nadwyżek tworzony jest dokument IPW zwiększający ilość w magazynie, a tam gdzie stwierdzono niedobór tworzony jest dokument IRW, zmniejszający ilość w magazynie. Jeśli nie ma nadwyżek, to dokument IPW się nie utworzy. Jeśli nie ma niedoborów, to dokument IRW się nie utworzy. Jeśli stan magazynowy wszystkich produktów w magazynie idealnie pokrywa się z rzeczywistością, to dokumenty IRW oraz IPW nie zostaną utworzone.

Dokument IPW powoduje przyjęcie produktu na magazyn w ostatniej cenie zakupu, natomiast dokument IRW powoduje rozchód produktu z magazynu według metody FIFO.

Zatwierdzenie arkusza powoduje automatyczne zatwierdzenia dokumentów IW, IPW i IRW i nie ma możliwości korygowania żadnego z tych dokumentów. Dlatego przed zatwierdzeniem arkusza należy się upewnić czy jest on prawidłowo uzupełniony. Jeśli zostaną wykryte błędy już po zatwierdzeniu arkusza to jedynym sposobem ich naprostowania jest wykonanie kolejnej inwentaryzacji (pomocne może być przy tym użycie opcji arkusza wypełnionego).

