## Sprzedaż produktów z magazynu - faktura pro forma

Mechanizm objęty jest przez plugin walidacją więc w przypadku jakichkolwiek problemów użytkownik będzie o nich informowany.

Należy pamiętać o nadaniu odpowiednich uprawnień dla użytkownika do dokumentów WZ i magazynu sprzedaży ([Uprawnienia](uprawnienia.md)).

Na potrzeby instrukcji zakładamy, że na fakturę pro forma wprowadzimy produkt 'H665'.

#### Tworzenie faktury pro forma

Tworzenie faktury rozpoczynamy od uruchomienia, standardowo dostępnymi w LMS metodami, formularza tworzenia faktury pro forma.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-175.png)

Wybieramy klienta i zapisujemy nagłówek faktury poprzez kliknięcie 'zapisz' w części "Informacje główne".

Uwaga: Jeśli nie zapiszemy nagłówka nie będzie można wybierać pozycji magazynowych. Dlaczego tak jest? Otóż, klient jest przypisany do konkretnej firmy, więc w momencie jego wybrania, system podejmuje decyzję o zasileniu listy produktów pozycjami z magazynu sprzedaży przynależnego do tej samej firmy, do której jest przypisany klient.

Następnie przechodzimy do wybrania produktu z magazynu.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-176.png)

Wprowadzamy ilość i cenę produktu. Ilość może być dowolna nawet wykraczająca poza obecny stan magazynowy i zapisujemy.

#### Przekształcenie faktury pro forma do faktury

Tworzenie faktury rozpoczynamy od uruchomienia, standardowo dostępnymi w LMS metodami, formularza tworzenia faktury z faktury pro forma.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-177.png)

Zapisujemy fakturę.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-178.png)

Nastąpiła walidacja dokumentu i dostaliśmy komunikaty błędów, które trzeba usunąć, aby zapisać fakturę.

Opis błędów:

- 'Zasoby uległy zmianie podczas edycji tego dokumentu i nie mogą zostać dodane do tego dokumentu.' - ten komunikat oznacza, że próbujemy sprzedać ilość większą niż mamy na magazynie w momencie tworzenia faktury. Jeśli tak jest możemy anulować tworzenie faktury, uzupełnić stany magazynowe, a następnie ponownie przejść do tworzenia faktury.
- 'Zła cena sprzedaży netto dla produktu: H665' - oznacza, że próbujemy sprzedać produkt poniżej ceny jego zakupu.

Podpowiedzi rozwiązania (treść mówi sama za siebie):

- "Usuń produkt: H665 z faktury, dodaj ponownie i ustaw ilość."
- "Musisz wybrać egzemplarze dla produktu: H665. Usuń ten produkt i dodaj ponownie!"

Postępujemy zgodnie z podpowiedziami i usuwamy pozycję z produktem i dodajemy go jeszcze raz.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-179.png)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-180.png)

Teraz możemy zapisać fakturę. W momencie zapisu zostanie do niej utworzony zatwierdzony dokument WZ co od razu wywoła skutek magazynowy.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-181.png)
