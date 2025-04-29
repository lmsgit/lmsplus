## Korzyści uczestnika projektu LMS Plus

Uczestnik uzyskuje dostęp do specjalnej gałęzi stabilnej LMS oraz utrzymywanych na bieżąco dodatków do publicznie dostępnej gałęzi LMS (lista wszystkich obecnie dostępnych dodatków jest dostępna poniżej i aktualizowana na bieżąco).
Wszystkie dodatki przechowywane są w odrębnych gałęziach systemu kontroli wersji git. Dzięki temu możliwe jest
sprawne zarządzanie dodatkami udostępnianymi w ramach projektu poprzez wykonywanie półautomatycznych synchronizacji zachodzących zmian w kodzie. Dokumentację systemu git znajdziemy pod adresem [https://git-scm.com/doc](https://git-scm.com/doc). Uczestnicy projektu są traktowani przez opiekuna projektu LMS Plus priorytetowo i uzyskują odpowiedzi na pytania techniczne w pierwszej kolejności przed resztą społeczności internetowej. Nasze rozwiązania oparte są na kilkunastu latach doświadczeń w programowaniu w środowisku sieciowym (m.in. uczestnictwo w projektach Kadu oraz LMS). Gwarantujemy zadowolenie i najwyższą technicznie
jakość obsługi.

#### Podsumowanie korzyści

1. Dostęp do kodu źródłowego wszystkich rozwiązań dostępnych w projekcie.
1. Utrzymywane są na bieżąco wydania stabilne LMS+ (od kilku lat dwa wydania równolegle - żeby umożliwić łagodne migracje między wersjami) - obecnie są to 27.x, 26.x, 25.x i 24.x. Do wersji stabilnych wchodzą głównie poprawki błędów oraz krytyczne zmiany z wersji rozwojowej.
1. Dostęp do bogatej dokumentacji w postaci wiki.
1. Wsparcie mailowe poprzez:
    - listę mailingową lms-plus@lists.lms.org.pl,
    - system zgłoszeń (ang. issues) projektu w witrynie github.com.

## Warunki uczestnictwa w projekcie LMS Plus

Każdy uczestnik za opłatą miesięczną uzyskuje dostęp do prywatnego repozytorium git bazującego na publicznym repozytorium LMS-a. Przystąpienie do projektu jest możliwe na co najmniej rok. Po roku uczestnik może wycofać się z projektu za miesięcznym wypowiedzeniem.

Opłata miesięczna uzależniona jest od zadeklarowanej przez uczestnika obsługiwanej liczby abonentów zgodnie z poniższym zasadami (warunki obowiązujące od **1 kwietnia 2025 roku**):

- **200 zł** - poniżej **500** abonentów,
- **250 zł** - od **500** abonentów i poniżej **1000** abonentów,
- **300 zł** - od **1000** abonentów.

## Dołączenie do projektu LMS Plus

Zapraszamy do dołączenia do projektu LMS Plus - można to zrobić wysyłając maila na adres [biuro@chilan.com](mailto:biuro@chilan.com?subject=projekt%20LMS%20Plus) o następującej treści:
1. Dane firmy do wystawianych faktur.
1. Adres e-mail, na który będą automatycznie wysyłane faktury.
1. Deklarowana liczba obsługiwanych abonentów (w przypadku braku deklaracji przyjmiemy taryfę w cenie **300 zł**).
1. Adres e-mail do zapisania na listę mailingową LMS Plus.
1. Nazwa konta w systemie github.com (konto trzeba utworzyć samodzielnie).
1. Załączony skan podpisanego i przypieczętowanego regulaminu projektu dostępnego poniżej:

    [Regulamin projektu LMS Plus](/assets/files/lms-plus-regulamin.pdf)

## Dostęp do repozytorium projektu LMS Plus

1. [Przygotować parę kluczy ssh umożliwiających dostęp do repozytorium](https://help.github.com/articles/generating-ssh-keys/). Wygenerowane klucze służą skonfigurowaniu wygodnego dostępu SSH do własnego konta subskrybenta w serwisie **github.com**. Nie należy ich nam przesyłać!
1. Dla wygody warto dopisać informacje o dostępie ssh do github w lokalnym pliku **~/.ssh/config**:

    ```
    Host github.com
        User git
        Hostname github.com
        PreferredAuthentications publickey
        IdentityFile /katalog_domowy_użytkownika/.ssh/nazwa_pliku_z_kluczem_prywatnym
    ```

    Opcją **IdentityFile** należy wskazać ścieżkę do pliku zawierającego klucz prywatny spośród pary wygenerowanych w **punkcie 1** kluczy.
 
1. Wykonać lokalną kopię repozytorium dla gałęzi master w lokalnym katalogu lms:

    ```bash
    git clone git@github.com:chilek/lms-plus.git lms
    ```

## Wymagania LMS Plus

* system operacyjny RHEL 8 lub zgodny z nim binarnie (CentOS, RockyLinux, AlmaLinux),
* baza danych PostgreSQL 10 lub wyższa,
* Serwer WWW Apache w wersji 2.4,
* PHP w wersji 7.2 - preferowana wersja to 7.4.

## Spis gałęzi repozytorium projektu LMS Plus

**Uwaga: linki poniżej są dostępne wyłącznie dla uczestników projektu!**

[gałąź główna (klon publicznie dostępnej gałęzi master)](https://github.com/chilek/lms-plus/tree/master)

[gałąź stabilna](https://github.com/chilek/lms-plus/tree/stable) (ostatnia wersja **27.79**)

[poprzednia gałąź stabilna](https://github.com/chilek/lms-plus/tree/stable-26) (ostatnia wersja **26.112**)

[poprzednia gałąź stabilna](https://github.com/chilek/lms-plus/tree/stable-25) (ostatnia wersja **25.108**)

[poprzednia gałąź stabilna](https://github.com/chilek/lms-plus/tree/stable-24) (ostatnia wersja **24.135**)

[przestarzała gałąź stabilna](https://github.com/chilek/lms-plus/tree/stable-1.11.23) (ostatnia wersja **1.11.23.32**)

[przestarzała gałąź stabilna](https://github.com/chilek/lms-plus/tree/stable-1.11.22) (ostatnia wersja **1.11.22.34**)

[przestarzała gałąź stabilna](https://github.com/chilek/lms-plus/tree/stable-1.11.21) (ostatnia wersja **1.11.21.37**)

[przestarzała gałąź stabilna](https://github.com/chilek/lms-plus/tree/stable-1.11.20) (ostatnia wersja **1.11.20.20**)

[przestarzała gałąź stabilna](https://github.com/chilek/lms-plus/tree/stable-1.11.19) (ostatnia wersja **1.11.19.15**)

[wtyczka: obsługa gpon urządzeń firmy ZTE](https://github.com/chilek/lms-plus/tree/gpon-zte/plugins/LMSGponZtePlugin/doc) - **[zrzuty ekranu](https://github.com/chilek/lms/wiki/GPON-ZTE-zrzuty-ekranu)**

[wtyczka: obsługa gpon urządzeń firmy Dasan](https://github.com/chilek/lms-plus/tree/gpon-dasan/plugins/LMSGponDasanPlugin/doc) - **[zrzuty ekranu](https://github.com/chilek/lms/wiki/GPON-DASAN-zrzuty-ekranu)**

[wtyczka: obsługa platformy VoIP Hiperus C5](https://github.com/chilek/lms-plus/tree/hiperus)

[wtyczka: obsługa platformy VoIP Adescom](https://github.com/chilek/lms-plus/tree/adescom)

[wtyczka: obsługa platformy IPTV Jambox](https://github.com/chilek/lms-plus/tree/jambox) - **[zrzuty ekranu](https://github.com/chilek/lms/wiki/JAMBOX-zrzuty-ekranu)**

[wtyczka: obsługa platformy Nettelekom](https://github.com/chilek/lms-plus/tree/nettelekom)

[wtyczka: obsługa platformy Metroport MVNO](https://github.com/chilek/lms-plus/tree/metroport-mvno)

[zaawansowane szablony dokumentów](https://github.com/chilek/lms-plus/tree/document-templates) - **[zrzuty ekranu](https://github.com/chilek/lms/wiki/CONTRACT-PROMO-zrzuty-ekranu)**:
* [umowy promocyjne i pakietowe](https://github.com/chilek/lms-plus/tree/document-templates/plugins/LMSDocumentTemplatesPlugin/documents/templates/contract-promo),
* [wezwania do zapłaty z automatycznym naliczaniem odsetek](https://github.com/chilek/lms-plus/tree/document-templates/plugins/LMSDocumentTemplatesPlugin/documents/templates/payment-summons),
* [książeczka opłat uwzględniająca harmonogram obciążeń klienta](https://github.com/chilek/lms-plus/tree/document-templates/plugins/LMSDocumentTemplatesPlugin/documents/templates/payment-booklet),
* [biling telefoniczny](https://github.com/chilek/lms-plus/tree/document-templates/plugins/LMSDocumentTemplatesPlugin/documents/templates/billing).

[raporty WWPE do UKE](https://github.com/chilek/lms-plus/tree/uke)

[wtyczka: obsługa magazynu (stara edycja)](https://github.com/chilek/lms-plus/tree/stock) - **[zrzuty ekranu](https://github.com/chilek/lms/wiki/STOCK-zrzuty-ekranu)**

[wtyczka: obsługa magazynu (nowa edycja)](https://github.com/chilek/lms-plus/tree/warehouse)

[wtyczka: integracja z systemem PLICBD2](https://github.com/chilek/lms-plus/tree/plicbd) - **[zrzuty ekranu](https://github.com/chilek/lms/wiki/PLICBD-zrzuty-ekranu)**

[wtyczka: integracja ze speedtest.pl](https://github.com/chilek/lms-plus/tree/speedtest) - **[zrzuty ekranu](https://github.com/chilek/lms/wiki/SPEEDTEST-zrzuty-ekranu)**

[wtyczka: statystyki w oparciu o pakiet narzędziowy RRDTOOL](https://github.com/chilek/lms-plus/tree/rrdstats) - **[zrzuty ekranu](https://github.com/chilek/lms/wiki/RRDSTATS-zrzuty-ekranu)**

[wtyczka: obsługa SMS w oparciu o SerwerSMS.pl/SMS.pl](https://github.com/chilek/lms-plus/tree/serwersms/plugins/LMSSerwerSmsPlugin/doc)

[wtyczka: obsługa SMS w oparciu o SMSAPI.pl](https://github.com/chilek/lms-plus/tree/smsapi/plugins/LMSSmsApiPlugin/doc)

[wtyczka: obsługa SMS w oparciu o SMSCenter.pl](https://github.com/chilek/lms-plus/tree/smscenter/plugins/LMSSmsCenterPlugin/doc)

[wtyczka: obsługa SMS w oparciu o CallAPI.pl](https://github.com/chilek/lms-plus/tree/callapi/plugins/LMSCallApiPlugin/doc)

[wtyczka: obsługa SMS w Mikrotiku](https://github.com/chilek/lms-plus/tree/mikrotik-sms/plugins/LMSMikrotikSmsPlugin/doc)

[wtyczka: obsługa platformy IPTV Evio](https://github.com/chilek/lms-plus/tree/evio) - **[zrzuty ekranu](https://github.com/chilek/lms/wiki/EVIO-zrzuty-ekranu)**

[wtyczka: eksport danych finansowych do formatu XML programu CDN Optima](https://github.com/chilek/lms-plus/tree/optima)

[wtyczka: eksport faktur (i opcjonalnie ich obrazów) do formatu XML programu SoftLab](https://github.com/chilek/lms-plus/tree/softlab)

[wtyczka: eksport danych finansowych do formatu EDI++ firmy InseRT](https://github.com/chilek/lms-plus/tree/edipp)

[wtyczka: eksport danych finansowych do formatu Magik programu WAPRO Fakir](https://github.com/chilek/lms-plus/tree/fakir)

[wtyczka: eksport danych finansowych do formatu Sage Symfonia FK](https://github.com/chilek/lms-plus/tree/symfonia)

[dodatkowe skrypty integracyjne](https://github.com/chilek/lms-plus/tree/backend-scripts)

[wtyczka: zarządzanie licencjami GData klientów](https://github.com/chilek/lms-plus/tree/gdata)

[wtyczka: obsługa podpisów biometrycznych dokumentów w oparciu o usługę Signatus firmy Infinite](https://github.com/chilek/lms-plus/tree/signatus) - **[zrzuty ekranu](https://github.com/chilek/lms/wiki/SIGNATUS-zrzuty-ekranu)**

Uwaga! Dziennik/archiwum transakcji został już zintegrowany z publicznie dostępną gałęzią LMS.
