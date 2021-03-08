## Kategorie podatkowe

Przy pomocy zmiennej konfiguracyjnej [phpui.tax_category_required](https://github.com/chilek/lms-plus/wiki/Zmienne-konfiguracyjne-LMS-Plus-phpui#phpuitax_category_required) możemy wymagać definiowania kategorii podatkowych dla taryf, zobowiązań bez taryf oraz pozycji dokumentów handlowych. W momencie wystawiania dokumentu handlowego na produkty magazynowe będziemy musieli takie kategorie podawać. Dobra wiadomość jest taka, że nie będziemy musieli tego robić każdorazowo przy wystawianiu dokumentu handlowego. Zła wiadomość jest taka, że mimo wszystko dla każdego produktu, który wymaga kategorii, będziemy musieli ją określić.

**Kategorię podatkową przypisujemy tylko dla produktu w magazynie. Nie musimy jej przypisywać dla każdego egzemplarza produktu.**

- Wyszukaj produkt w "Katalogu produktów" i uruchom jego edycję

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-36.png)

- Wybierz odpowiednią kategorię podatkową i zapisz zmiany

W tym momencie podczas tworzenia dokumentu handlowego podczas wyboru produktu z magazynu kategoria podatkowa będzie się automatycznie podpowiadać.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-156.png)

Jeśli na dokumencie handlowym znajdzie się pozycja magazynowa to kategorii podatkowej nie da się zmienić z poziomu dokumentu handlowego. Dlatego, w razie konieczności, należy najpierw zmienić kategorię podatkową dla produktu, a dopiero potem dodawać produkt do dokumentu handlowego.

