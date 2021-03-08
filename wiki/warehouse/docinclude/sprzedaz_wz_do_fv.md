## Sprzedaż produktów z magazynu - WZ do faktury

Do prowadzenia ewidencji urządzeń, które zostały sprzedane używamy dokumentu WZ (wydanie zewnętrzne). Należy pamiętać o nadaniu odpowiednich uprawnień dla użytkownika do dokumentów WZ i magazynu sprzedaży ([Uprawnienia](uprawnienia.md)).

Mechanizm objęty jest przez plugin walidacją więc w przypadku jakichkolwiek problemów użytkownik będzie o nich informowany.

Na potrzeby instrukcji zakładamy, że mamy w magazynie sprzedaży produkt 'H665'.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-154.png)

Przychodzi do nas klient naszej sieci i jest zdecydowany od nas kupić takie urządzenie. Wystawiamy zatem fakturę.

### Tworzenie faktury

Tworzenie faktury rozpoczynamy od uruchomienia, standardowo dostępnymi w LMS metodami, formularza tworzenia faktury.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-155.png)

Wybieramy klienta i zapisujemy nagłówek faktury poprzez kliknięcie 'zapisz' w części "Informacje główne".

Uwaga: Jeśli nie zapiszemy nagłówka nie będzie można wybierać pozycji magazynowych. Dlaczego tak jest? Otóż, klient jest przypisany do konkretnej firmy, więc w momencie jego wybrania, system podejmuje decyzję o zasileniu listy produktów pozycjami z magazynu sprzedaży przynależnego do tej samej firmy, do której jest przypisany klient.

Następnie przechodzimy do wybrania produktu z magazynu. Ponieważ jest to produkt z egzemplarzami nie podajemy ilości. Ilość zmienia się w zależności od ilości wybranych egzemplarzy.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-156.png)

Podajemy cenę i zapisujemy pozycję. W nawiasach mamy podpowiadana cenę netto zakupu urządzenia.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-157.png)

Uruchom "Zapisz".

W momencie zapisu tworzony jest dokument WZ, który zdejmuje z magazynu sprzedaży urządzenie. Takie WZ jest już zatwierdzone.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-158.png)

Stan magazynowy urządzeni po sprzedaży jest pokazany poniżej (dla urządzenia stan wynosi "0").

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-159.png)

##### Uwagi

- Sprzedaż produktu magazynowego poniżej ceny netto jego zakupu jest blokowana, ale jednocześnie podczas wystawiania faktury cena zakupu netto jest podpowiadana.
- Zapisanie faktury powoduje, że edycja ilości pozycji magazynowej takiej faktury nie będzie możliwa, ale możliwa będzie zmiana ceny. Zmiany ilości  w pozycjach magazynowych można dokonać jedynie przez korektę faktury.
- Anulowanie zapisanej faktury nie powoduje żadnych akcji po stronie magazynu. Dokument WZ nadal będzie istniał i będzie zmniejszał stany magazynowe.
- Na fakturze nie możemy usuwać pozycji magazynowych.
- Jeśli faktura jest powiązana z dokumentem WZ operacja usuwania faktury się nie powiedzie.

##### Extra czynności

Czasami może okazać się potrzebne wykonanie kolejnych czynności. Żeby to zobrazować poczynimy na potrzeby instrukcji kolejne założenia. W pierwszej części instrukcji nasz klient dostał fakturę na urządzenie (rysunek poniżej). Zakładamy, że po 2 tygodniach urządzenie uległo awarii i klient chce wymienić urządzenie na sprawne.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-157.png)

W takim wypadku należy wystawić korektę faktury. Uruchom standardową dla LMS akcję tworzenia korekty faktury.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-160.png)

Edytujemy produkt z egzemplarzami dlatego ilość jest uzupełniana automatycznie w zależności od tego ile egzemplarzy mamy na dostępnej liście. Egzemplarz usuwamy z listy co spowoduje, że powróci na listę wyboru dostępnych egzemplarzy i zmieni się ilość produktu na '0'.

Możemy jednocześnie zmienić cenę (w tym przypadku nic to nie zmieni bo i tak wyzerowaliśmy pozycję).

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-161.png)

Uruchom "Zapisz".

W momencie zapisu tworzony jest dokument WZk, który wprowadza na magazyn sprzedaży niesprawne urządzenie klienta. Takie WZk jest już zatwierdzone.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-162.png)

Urządzenie wróciło na ten sam magazyn, z którego było rozchodowane czyli na magazyn sprzedaży. Stan magazynowy został zwiększony (rysunek poniżej)

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-163.png)

##### Uwagi

Jeśli wystawiamy korektę faktury z pozycjami magazynowymi to:
  - Korygowanie pozycji magazynowych można wykonać tylko raz (tylko przy pierwszej korekcie faktury będzie generowany dokument WZk).
  - Zapisanie korekty faktury powoduje, że automatycznie tworzona jest zatwierdzona korekta dokumentu WZk dla tej faktury, który zawiera tylko pozycje magazynowe.
  - Zapisanie korekty faktury powoduje, że edycja takiej korekty faktury będzie możliwa dla pozycji magazynowych jedynie w zakresie cen.
  - Zapisanie korekty faktury powoduje, że usunięcie korekty faktury będzie niemożliwe.
  - Anulowanie korekty faktury nie powoduje żadnych akcji po stronie magazynu. Dokument WZk nadal będzie istniał i będzie zmieniał stany magazynowe.
- Jeśli korekta faktury jest powiązana z dokumentem WZk operacja usuwania korekty faktury się nie powiedzie.

###### Utylizacja urządzenia

Ponieważ zepsute urządzenie poprzez WZk zostało przyjęte na magazyn sprzedaży musimy się go z tego magazynu pozbyć, ponieważ inny pracownik mógłby je wystawić do sprzedaży dla kolejnego klienta, a tego nie chcemy. W tej instrukcji  [Utylizacja urządzeń](utylizacja_urzadzen.md) zostało opisane jak tego dokonać.

