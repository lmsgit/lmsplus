## Utylizacja urządzeń

Poniższa instrukcja opisuje propozycje przepływu danych w magazynie w związku z utylizacją urządzeń sieciowych.

Do prowadzenia ewidencji urządzeń, które będziemy utylizować używać będziemy dokumentów MM oraz RW. Należy pamiętać o nadaniu odpowiednich uprawnień dla użytkownika do tych dokumentów oraz do niezbędnych magazynów ([Uprawnienia](uprawnienia.md)).

Fizyczna utylizacja urządzenia może nastąpić dopiero po zdjęciu urządzenia z ewidencji magazynowej.

Utylizację urządzeń możemy prowadzić na dwa sposoby:
- na bieżąco (urządzenie utylizujemy od razu w momencie stwierdzenia takiej potrzeby),
- okresowo (urządzenia do utylizacji gromadzimy a następnie masowo poddajemy utylizacji).

##### Utylizacja urządzeń na bieżąco

Dokonujemy jej poprzez wystawienie dokumentu RW na urządzenie podlegające utylizacji. Tworzenie dokumentu RW opisane jest tutaj: [Rozchód wewnętrzny i korekta rozchodu (RW) (RWk)](dokument_rw.md).

Zalety:
- rozchodu możemy dokonać z dowolnego magazynu w dowolnym momencie,
- rozchodu możemy dokonać przy pomocy jednego prostego dokumentu.

Wady:
- dla każdego utylizowanego urządzenia musimy generować oddzielny dokument.

##### Utylizacja urządzeń okresowo

Dokonujemy jej w następujący sposób:
- tworzymy oddzielny magazyn o nazwie np. "Utylizacja" i typie "Magazyn zwykły" ([Magazyny](magazyny.md)),
- każde urządzenie do utylizacji przenosimy dokumentem MM na magazyn "Utylizacja" ([Przesunięcie między magazynami (MM)](dokument_mm.md)),
- w momencie kiedy nazbiera nam się konkretna liczba urządzeń w tym magazynie tworzymy dokument RW z magazynu "Utylizacja", na który wprowadzamy wszystkie pozycje z magazynu ([Rozchód wewnętrzny i korekta rozchodu (RW) (RWk)](dokument_rw.md)).

Zalety:
- rozchodu wielu urządzeń możemy dokonać przy pomocy jednego prostego dokumentu.

Wady:
- dla każdego utylizowanego urządzenia musimy generować oddzielny dokument MM.

##### Podsumowanie

Ostatecznie ilość generowanych dokumentów w obu sposobach utylizacji jest podobna. Dlaczego to takie ważne? Bo dokumenty magazynowe są dowodami księgowymi i każdy dokument magazynowy opisujący operacje magazynowe firma ma obowiązek posiadać w wersji drukowanej do okazania dla organu kontroli. Najlepiej jest zatem przyjąć rozwiązanie wygodniejsze z punktu widzenia organizacyjnego.
