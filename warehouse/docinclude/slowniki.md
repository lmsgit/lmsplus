Słowniki danych:

- Producenci - słownik służy do definiowania producentów produktów w magazynie i ewentualną ich synchronizację z producentami z OS. Z tego słownika czerpane są informacje o producencie podczas tworzenia nowego produktu.
   - Podczas dodawania producenta do MAG istnieje możliwość jednoczesnego dodania producenta do OS o ile nazwa nie jest zarezerwowana w OS.
   - Istnieje możliwość dodania producenta z MAG do producentów w OS, ale tylko pod warunkiem, że nazwa nie jest już zajęta.
   - Edycja producenta w MAG, który jest powiązany z OS powoduje zmiany również w OS.
   - Usuwanie producenta z MAG powiązanego z producentem z OS powoduje usunięcie tylko z WH (usunięcie powiązania).
   - Usunięcie producenta z MAG jest możliwe tylko jeśli nie jest przypisany do żadnego produktu.
- Grupy produktów - słownik służy do definiowania grup asortymentu. Każdy produkt może mieć przypisaną jedną grupę.
- Jednostki miar - słownik służy do definiowania jednostek miar jakie używane będą w magazynie. Każdy produkt/usługa musi mieć przypisaną jednostkę miary.
- Rodzaje cen - słownik służy do definiowania rodzajów cen jakie używane będą w magazynie. Każdy produkt może mieć przypisanych klika rodzajów cen dzięki czemu możliwe jest zdefiniowanie polityki cenowej sprzedaży.
   - Produkt może posiadać różnego rodzaju ceny sprzedaży, ale nie musi.
   - Jeśli są jakieś ceny sprzedaży to tylko jedna z nich może być ceną domyślną.
   - Cena domyślna jest podpowiadana podczas wystawiana dokumentu sprzedaży.
   - Usunięcie ceny domyślnej nie jest możliwe bezpośrednio (chyba, że jest to jedyna cena). Należy najpierw ustalić nową cenę domyślną a następnie ewentualnie usunąć starą cenę.
   - Modyfikacja ceny obejmuje zmianę jej wartości netto i brutto. Jeśli potrzebna jest zmiana typu ceny należy usunąć stary typ ceny i dodać nowy typ.
- Prefiksy - słownik pozwala definiować nazwy prefiksów stosowanych podczas tworzenia egzemplarzy produktu.
- Dostawcy - wyświetla listę dostawców zdefiniowanych w systemie. Jest to uproszczona lista klientów, którzy zostali zdefiniowani jako dostawcy. W celu zdefiniowania klienta jako dostawcy należy przy pomocy formularza edycji klienta oznaczyć go jako dostawcę. Generalnie zarządzanie dostawcami następuje poprzez formularze przeznaczone do zarządzania klientami.