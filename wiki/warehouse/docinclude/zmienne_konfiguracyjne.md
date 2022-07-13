## Zmienne konfiguracyjne

### warehouse.allow_sale_below_purchase_price

**Typ:** Wartość całkowita.

**Wartość domyślna:** _0_

**Opis:** Określa czy pozwalać (wartość _1_) na sprzedaż produktów magazynowych w cenach poniżej ceny zakupu, czy nie (wartość _0_).

**Dostępność:** Od wersji > 1.9.2

### warehouse.csv_separator

**Typ:** Wartość tekstowa.

**Wartość domyślna:** _|_

**Opis:** Określa znak separatora pól w pliku importu '.csv'.

**Dostępność:** Od wersji > 1.9.4 do < 2.1.0

### warehouse.csv_enclosure

**Typ:** Wartość tekstowa.

**Wartość domyślna:** _"_

**Opis:** Określa znak domknięcia pola w pliku importu '.csv'.

**Dostępność:** Od wersji > 1.9.4 do < 2.1.0

### warehouse.default_taxrate

**Typ:** Wartość tekstowa.

**Wartość domyślna:** _23_

**Opis:** Od wersji > 1.9.4 zastępuje _warehouse.default_sync_taxid_.

### warehouse.default_measure

**Typ:** Wartość tekstowa.

**Wartość domyślna:** _szt._

**Opis:** Od wersji > 1.9.4 zastępuje _warehouse.default_sync_measureid_.

### warehouse.modellist_pagelimit

**Opis:** Od wersji > 1.9.4 zastępuje _warehouse.sync_modelslist_pagelimit_.

### warehouse.netdevicelist_pagelimit

**Opis:** Od wersji > 1.9.4 zastępuje _warehouse.sync_netdeviceslist_pagelimit_.

### warehouse.productlist_pagelimit

**Opis:** Od wersji > 1.9.4 zastępuje _warehouse.sync_producerslist_pagelimit_.

### warehouse.linked_item_netdevice_edition

**Typ:** Wartość logiczna.

**Wartość domyślna:** _true_

**Opis:** Określa, czy w przypadku kiedy egzemplarz produktu jest powiązany z urządzeniem sieciowym zmiana nazwy, numeru seryjnego i opisu egzemplarza w magazynie spowoduje automatyczną zmianę tych danych w powiązanym urządzeniu sieciowym i na odwrót. Dodatkowo dla wartości _true_ przy próbie powiązania istniejącego egzemplarza z istniejącym urządzeniem sieciowym wymienione powyżej dane urządzenia sieciowego zostaną nadpisane danymi egzemplarza.

**Dostępność:** Od wersji >= 2.0.0
