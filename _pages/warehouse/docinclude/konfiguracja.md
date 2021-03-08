##  Konfiguracja wstępna

W procesie instalacji tworzone są wstępnie zdefiniowane zmienne konfiguracyjne związane z pluginem, które można zmienić z poziomu opcji konfiguracyjnych systemu. Należą one do sekcji "warehouse".

Przed rozpoczęciem właściwej pracy z magazynem konieczne jest uzupełnienie słowników danych. Uprawniony do ich uzupełniania jest użytkownik z rolą "(WAREHOUSE) Administracja magazynem" ([Uprawnienia](uprawnienia.md)) lub z rolą "pełny dostęp".

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-1.png)

Podczas instalacji wtyczki część słowników jest od razu uzupełniona minimalną ilością danych. Tuż po instalacji pluginu słowniki należy uzupełnić podstawowymi danymi niezbędnymi do rozpoczęcia pracy.

**Zaleca się wykonanie poniższych czynności w kolejności ich występowania.**

#### Nadanie uprawnień dostępu do modułów.

Proces wstępnej konfiguracji może przeprowadzić jedynie użytkownik z rolą "(WAREHOUSE) Administracja magazynem" ([Uprawnienia](uprawnienia.md)) lub z rolą "pełny dostęp". Przypisanie roli następuje z poziomu formularza edycji użytkownika LMS.

#### Utworzenie domyślnych planów numeracyjnych dokumentów magazynowych

Plugin "Warehouse" umożliwia prowadzenie ewidencji magazynowej z uwzględnieniem firm występujących w LMS. Każda firma w LMS musi posiadać własne plany numeracyjne dla dokumentów magazynowych. Generowanie planów numeracyjnych odbywa się poprzez uruchomienie z głównego LMS (Magazyn-słowniki -> Generuj plany).

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-2.png)

Na formularzu należy wybrać firmę oraz zaznaczyć typy dokumentów, dla których mają zostać wygenerowane plany i uruchomić 'Generuj domyślne plany numeracyjne'.

Uwaga: Wskazane jest wygenerowanie planów dla wszystkich typów dokumentów danej firmy. Jeśli tego nie zrobimy w każdym momencie można uruchomić ten formularz i przy jego pomocy dodać brakujące plany numeracyjne. W trakcie rozwoju systemu mogą pojawiać się nowe typy dokumentów, dla których będzie potrzeba zdefiniowania planu numeracyjnego, wtedy należy użyć tego formularza do wygenerowania planu dla takich dokumentów.

Po wykonaniu czynności generowania formularz wygląda następująco:

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-3.png)

Wygenerowane plany pojawiają się na liście wszystkich planów numeracyjnych w systemie (rysunek poniżej) i podlegają takim samym operacjom (np.edycji) jak każdy plan numeracyjny.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-4.png)

Należy pamiętać, że każda firma musi mieć swoje plany numeracyjne, dlatego domyślny plan numeracyjny dla dokumentu magazynowego używa w szablonie skróconej nazwy firmy jako wyróżnika.

#### Utworzenie magazynów

Aby rozpocząć ewidencję magazynową dla firmy musi być dla niej zdefiniowany magazyn główny ([Magazyny](magazyny.md)).

#### Bilans otwarcia

Uwaga: W kwestii ewidencji już posiadanych produktów firmy przyjmują podejście, w którym rezygnują z ewidencji magazynowej już posiadanego towaru i rozpoczynają ewidencję tylko produktów nabytych po rozpoczęciu używania pluginu. W takim przypadku bilansu otwarcia można nie wykonywać.

Niezależnie od tego czy bilans otwarcia będzie robiony czy nie, zaleca się wykonanie czynności synchronizacji ([Synchronizacja masowa](synchronizacja_masowa.md)).

[Tworzenie bilansu otwarcia magazynu](bilans_otwarcia.md)

#### Nadanie uprawnień

Dla każdego użytkownika, który będzie zaangażowany w pracę magazynu należy nadać odpowiednie uprawnienia ([Uprawnienia](uprawnienia.md)).

#### Podsumowanie

Po wykonaniu powyższych czynności magazyn jest gotowy do używania przez pozostałych użytkowników systemu i ewidencjonowania bieżących operacji magazynowych.

## Zmienne konfiguracyjne

### warehouse.allow_sale_below_purchase_price

**Typ:** Wartość całkowita.

**Wartość domyślna:** _0_

**Opis:** Określa czy pozwalać (wartość _1_) na sprzedaż produktów magazynowych w cenach poniżej ceny zakupu, czy nie (wartość _0_).

**Dostępność:** po 1.9.1
