## FIFO

###### FIFO - first in - first out
1. Metoda wyceny zużycia materiałów oparta na założeniu, że wydanie materiałów do produkcji rozliczane jest według cen zakupu materiałów, które chronologicznie były przyjmowane do magazynu.
2. Zasada, zgodnie z którą towary najdłużej składowane w magazynie wydawane są w pierwszej kolejności.

Poniższa instrukcja ma na celu zobrazowanie działania tej metody wyceny w pluginie. W przykładach przyjmowane są małe ilości zakupionego towaru w celu lepszego zobrazowania procesu.

#### Produkty bez egzemplarzy

Załóżmy, że kupiliśmy produkt o nazwie "Router AAA" w trzech dostawach:
- pierwsza dostawa towaru była w ilości 1 szt. po 120 zł za sztukę i otrzymaliśmy od dostawcy fakturę "FV/101/2020",
- druga dostawa towaru była w ilości 1 szt. po 130 zł za sztukę i otrzymaliśmy od dostawcy fakturę "FV/102/2020".
- trzecia dostawa towaru była w ilości 1 szt. po 140 zł za sztukę i otrzymaliśmy od dostawcy fakturę "FV/103/2020".

Żeby wprowadzić towar na magazyn utworzymy produkt bez egzemplarzy o nazwie "Router AAA" i udokumentujemy dostawę tworząc 3 dokumenty PZ (poniżej).

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-216.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-217.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-219.png)

Na stanie magazynowym mamy 3 szt. Teraz wystawimy WZ na jedną sztukę.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-218.png)

Widzimy, że najpierw została rozchodowana sztuka, która jako pierwsza weszła na stan magazynowy dokumentem "TESTOWA1/PZ/4/2020" i rozchód nastąpił w cenie z tego przyjęcia czyli 120 zł netto.

Teraz z kolei wystawmy jedno WZ na dwie kolejne sztuki.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-220.png)

Interpretacja jest następująca. Najpierw została rozchodowana jedna sztuka, która weszła na stan magazynowy dokumentem "TESTOWA1/PZ/5/2020" i rozchód nastąpił w cenie z tego przyjęcia czyli 130 zł netto. Ponieważ ilość sztuk z tej PZ została wyczerpana kolejna sztuka została rozchodowana z kolejnego przyjęcia towaru dokonanego dokumentem "TESTOWA1/PZ/6/2020" i rozchód nastąpił w cenie z tego przyjęcia czyli 140 zł netto.

#### Produkty z egzemplarzami

Załóżmy, że kupiliśmy produkt o nazwie "Router BBB" w trzech dostawach:
- pierwsza dostawa towaru była w ilości 2 szt. po 120 zł za sztukę i otrzymaliśmy od dostawcy fakturę "FV/104/2020",
- druga dostawa towaru była w ilości 2 szt. po 130 zł za sztukę i otrzymaliśmy od dostawcy fakturę "FV/105/2020".
- trzecia dostawa towaru była w ilości 2 szt. po 140 zł za sztukę i otrzymaliśmy od dostawcy fakturę "FV/105/2020".

Żeby wprowadzić towar na magazyn utworzymy produkt z egzemplarzami o nazwie "Router BBB" i udokumentujemy dostawę tworząc 3 dokumenty PZ (poniżej).

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-221.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-222.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-223.png)

Na stanie magazynowym mamy 6 szt. identycznych urządzeń w różnych cenach zakupu.

Teraz wystawimy WZ na jedną sztukę.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-224.png)

Zatwierdzony dokument wygląda jak poniżej.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-225.png)

W przykładzie wybraliśmy urządzenie "ROUTER-RBE6" przyjęte w ostatniej dostawie, jednak rozchód nastąpił w cenie pierwszej dostawy czyli 120 zł netto. Jest to jak najbardziej prawidłowe zachowanie systemu dlatego, że wycenie nie podlegają egzemplarze, ale produkt. Czyli daje nam to możliwość rozchodowania dowolnego egzemplarza i jednocześnie prawidłowej wyceny rozchodu produktu. Należy zaznaczyć, że zawsze rozchodujemy produkt jako taki, a to jaki egzemplarz jest rozchodowany, jest tylko dodatkową informacją, którą możemy potraktować jako cechę produktu.

Teraz z kolei wystawmy jedno WZ na dwie kolejne sztuki.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-226.png)

Interpretacja jest następująca. Najpierw została rozchodowana jedna sztuka, która weszła na stan magazynowy dokumentem "TESTOWA1/PZ/7/2020" i rozchód nastąpił w cenie z tego przyjęcia czyli 120 zł netto. Ponieważ ilość sztuk z tej PZ została wyczerpana kolejna sztuka została rozchodowana z kolejnego przyjęcia towaru dokonanego dokumentem "TESTOWA1/PZ/8/2020" i rozchód nastąpił w cenie z tego przyjęcia czyli 130 zł netto.




