# Podręcznik użytkownika pluginu "Warehouse"

###### Dokumentacja oparta na pluginie w wersji 1.9.1

Plugin "Warehouse" jest dodatkiem do systemu LMS przeznaczonym do prowadzenia gospodarki magazynowej. Plugin umożliwia prowadzenie ewidencji każdego rodzaju asortymentu.

Plugin dostarcza standardowych rodzajów dokumentów magazynowych stosowanych w prowadzeniu ewidencji magazynowej. Dokumentacja opisuje przykładowe procesy przepływu produktów w przedsiębiorstwie i dokumenty magazynowe z tym powiązane. Do opisu metod dokumentowania procesów magazynowych przyjęty został ogólny model stosowany w gospodarce magazynowej, który ma na celu zobrazowania funkcji systemu. Ostatecznie to przedsiębiorca decyduje o tym jakimi dokumentować będzie operacje magazynowe. Zalecane jest zatem aby każdy przedsiębiorca korzystający z magazynu przed wystawianiem dokumentów magazynowych uzgodnił z księgowością jakimi dokumentami magazynowymi powinien ewidencjonować odpowiednie dla swojego przedsiębiorstwa procesy.

Istotne cechy działania magazynu:
- Ewidencja magazynowa prowadzona jest w cenach netto według metody FIFO.
- Każda firma zdefiniowana w systemie LMSplus może prowadzić własną, odrębną gospodarkę magazynową.

W dokumentacji będą używane następujące akronimy:
- "OS" - Osprzęt Sieciowy,
- "MAG" - Magazyn,
- "KP" - Katalog produktów,
- "KU" - Katalog usług.

### Konfiguracja wstępna

#### [Konfiguracja wstępna](/wiki/warehouse/docinclude/konfiguracja.md)

#### [Bilans otwarcia (BO)](docinclude/bilans_otwarcia.md)

#### [Przyjęcie zewnętrzne (PZ)](docinclude/dokument_pz.md)

### Rozchód wewnętrzny i korekta rozchodu

#### [Rozchód wewnętrzny i korekta rozchodu (RW) (RWk)](docinclude/dokument_rw.md)

#### [Dzierżawa urządzeń i zwrot dzierżawionych urządzeń](docinclude/dokument_rw_rental.md)

### Przesunięcie między magazynami

#### [Przesunięcie między magazynami (MM)](docinclude/dokument_mm.md)

### Sprzedaż produktów magazynowych

Ewidencja sprzedaży w LMS prowadzona jest przy użyciu faktur sprzedaży natomiast w magazynie realizowana jest przy pomocy dokumentów WZ (wydanie zewnętrzne). Te rodzaje dokumentów muszą być ze sobą powiązane dla każdej sprzedaży. Oznacza to, że jeśli wystawimy fakturę na jakiś produkt, to w magazynie musimy wystawić WZ na ten produkt (zmniejszyć stan magazynowy produktu). Z kolei jeśli w magazynie wystawimy WZ na jakiś produkt, to jesteśmy zobligowani prawem aby w odpowiednim czasie wystawić fakturę na podstawie tego WZ.

Sprzedaż możemy prowadzić jedynie z magazynu, który ma przypisany typ 'Magazyn Sprzedaży' ([Magazyny](docinclude/magazyny.md)).

Integracja WZ z modułem finansowym pozwala na:
- wystawienie WZ i utworzenie faktury w dowolnym momencie na podstawie WZ,
- wystawienie WZ, skorygowanie WZ i utworzenie w dowolnym momencie faktury uwzględniającej Wz i WZk,
- wystawienie faktury na pozycje magazynowe i automatyczne utworzenie WZ podczas zapisu faktury,
- automatyczne wystawienie korekty WZ w momencie kiedy zapisywana jest korekta faktury zawierająca pozycje magazynowe,
- wystawienie faktury pro forma na pozycje magazynowe i przekształcenie do normalnej faktury, która dalej podlega powyższym zasadom,
- ustalenie domyślnej ceny sprzedaży dla produktów,
- łączenie pozycji magazynowych i niemagazynowych na jednej fakturze.

####  [Sprzedaż produktów z magazynu - faktura na podstawie WZ](docinclude/sprzedaz_fv_z_wz.md)

#### [Sprzedaż produktów z magazynu - WZ do faktury](docinclude/sprzedaz_wz_do_fv.md)

#### [Sprzedaż produktów z magazynu - faktura pro forma](docinclude/sprzedaz_pro_forma.md)

### Inwentaryzacja

#### [Inwentaryzacja (IW)](docinclude/inwentaryzacja.md)

### Zakup usług

#### [Zakup usług (ZU)](docinclude/zakup_uslug.md)

### Raporty

#### [Dostawcy](docinclude/dostawcy.md)

#### [Stany magazynowe](docinclude/stany_magazynowe.md)

#### [Lista dokumentów](docinclude/lista_dokumentow.md)

#### [Historia dokumentów](docinclude/historia_dokumentow.md)

#### [Raport sprzedaży](docinclude/raport_sprzedazy.md)

#### [Raport zakupu usług](docinclude/raport_uslug.md)

#### [Dzierżawa](docinclude/raport_dzierzawa.md)

#### [JPK_MAG](docinclude/jpk_mag.md)

#### [Eksport do EDI++](docinclude/epp.md)

## Dodatki:

#### [Magazyny](docinclude/magazyny.md)

#### [Czym jest synchronizacja?](docinclude/synchronizacja_wyjasnienie.md)

#### [Synchronizacja masowa](docinclude/synchronizacja_masowa.md)

#### [Synchronizacja selektywna](docinclude/synchronizacja_selektywna.md)

#### [Katalog produktów](docinclude/produkt_wyjasnienie.md)

#### [Tworzenie produktu bez egzemplarzy](docinclude/produkt_bez_egz.md)

#### [Tworzenie produktu z egzemplarzami niepowiązanego z OS](docinclude/produkt_z_egz.md)

#### [Tworzenie produktu powiązanego z OS](docinclude/produkt_z_egz_os.md)

#### [Katalog usług](docinclude/katalog_uslug.md)

#### [Tworzenie usługi](docinclude/usluga.md)

#### [Dokumenty magazynowe](docinclude/dokumenty_magazynowe.md)

#### [Słowniki](docinclude/slowniki.md)

#### [Uprawnienia](docinclude/uprawnienia.md)

#### [Domyślne ceny sprzedaży produktu](docinclude/ceny_sprzedazy.md)

#### [Kategorie podatkowe](docinclude/kategorie_podatkowe.md)

#### [Utylizacja urządzeń](docinclude/utylizacja_urzadzen.md)

#### [FIFO](docinclude/fifo.md)
