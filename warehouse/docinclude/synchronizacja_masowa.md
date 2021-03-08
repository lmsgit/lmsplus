## Synchronizacja masowa

[Czym jest synchronizacja?](synchronizacja_wyjasnienie.md)

- Uruchom (Magazyn->Synchronizacja) w menu głównym LMS.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-8.png)

- Do formularza zostaną załadowane informacje o wszystkich urządzeniach sieciowych oraz o producentach i modelach (tylko pochodzących ze słownika 'Producenci i modele'). Każda pozycja listy może przyjąć jeden z następujących statusów:
  - "Gotowy" - oznacza, że pozycja może zostać przeniesiona do magazynu, wtedy na końcu wiersza pojawia się checkbox, który pozwala oznaczyć ją do przeniesienia.
  - "W magazynie" - oznacza, że pozycja już została przeniesiona do magazynu i nie będzie można jej przesłać ponownie.
  - "Nie gotowy" - oznacza, że pozycja nie może zostać przeniesiona do magazynu, wtedy w kolumnach _komentarze_ i _wskazówki_ zostaną wyświetlone podpowiedzi co należy wykonać, żeby pozycja przeszła w stan "Gotowy".
- Zaznacz pozycje, które chcesz przenieść do magazynu. (Zalecane jest przeniesienie wszystkich producentów, gdyż to spowoduje zasilenie słownika 'Producenci' w magazynie)
- Uruchom "Dodaj do magazynu wszystkie zaznaczone pozycje".

###### Błędy podczas synchronizacji i kontynuacja synchronizacji

Gdy synchronizacja jest niemożliwa dla pewnych danych, to dla tych danych zostaną wyświetlone komunikaty błędów i komentarze podpowiadające rozwiązanie.

###### Czy synchronizować wszystko?

Nie ma takiej konieczności. Wybór należy do administratora magazynu.

Jeśli synchronizacji poddamy wszystko z osprzętu sieciowego to będziemy mieli gwarancję, że w przyszłości (kiedy będziemy dodawać produkty w magazynie, które będziemy wiązać z urządzeniami w osprzęcie sieciowym) nie będziemy mieli konfliktów nazw z już istniejącym osprzętem sieciowym. Poza tym jeśli np. przeniesiemy wszystkich producentów z OS do WH to w magazynie od razu uzupełnił się słownik "Producenci".

Jeśli dokonamy synchronizacji tylko wybranych elementów, które na pewno będą potrzebne w magazynie nie będziemy mieli nadmiarowej ilości danych w magazynie. Przykładowo jeśli będziemy przeszukiwali katalog produktów wyszukiwanie będzie szybsze bo będzie wykonywane na mniejszej ilości elementów.

Można też zastosować metodę stanowiącą rozsądny kompromis, w której synchronizujemy wszystkich producentów (żeby uzupełnił się słownik "Producenci" w magazynie) i wszystkie modele (żeby uniknąć konfliktów nazw w przyszłości), a urządzenia sieciowe synchronizujemy selektywnie (wybieramy tylko te które będą funkcjonowały w magazynie).

###### Przykład

Mamy w osprzęcie sieciowym urządzenia sieciowe należące do producenta 'DASAN' i reprezentujące ten sam model urządzeń 'H660G'. Urządzenia te będziemy chcieli przenieść do magazynu.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-10.png)

Z powyższego rysunku wynika, że nie możemy dodać urządzeń do magazynu ponieważ model nie jest powiązany z magazynem. Natomiast model też nie może zostać dodany do magazynu ponieważ powiązany z nim producent nie jest powiązany z magazynem. W związku z powyższym najpierw należy dodać producenta do magazynu. W tym celu zaznaczamy producenta i wykonujemy "Dodaj do magazynu wszystkie zaznaczone pozycje". W efekcie mamy sytuację z poniższego rysunku.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-11.png)

Z powyższego rysunku widzimy, że producent został dodany do magazynu i teraz możemy do magazynu dodać model. W tym celu zaznaczamy model i wykonujemy "Dodaj do magazynu wszystkie zaznaczone pozycje".

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-12.png)

Z powyższego rysunku widzimy, że producent i model są dodane do magazynu. Teraz możemy do magazynu dodać dowolną ilość urządzeń sieciowych. W tym celu zaznaczamy urządzenia sieciowe i wykonujemy "Dodaj do magazynu wszystkie zaznaczone pozycje".

na rysunku poniżej widzimy, że wszystkie urządzenia zostały dodane do magazynu.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-13.png)

Na poniższych rysunkach możemy zobaczyć efekt synchronizacji. W jej wyniku otrzymaliśmy:
- produkt 'H660G' powiązany z modelem 'H660G' w OS.
- producenta 'DASAN' powiązanego z producentem 'DASAN' w OS
- egzemplarze produktu, z których każdy jest powiązany z urządzeniem sieciowym w OS.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-14.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-15.png)

Dodatkowo po synchronizacji producenta uzupełniony został też słownik 'Producenci'

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-16.png)

###### Uwagi

Formularz (Magazyn->Synchronizacja) może być używany na każdym etapie pracy magazynu jako centrum zarządzania synchronizacją.
