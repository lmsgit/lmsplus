#### Uprawnienia dostępu.

System uprawnień w magazynie działa na trzech poziomach:
- uprawnienia do modułów,
- uprawnienia do magazynów,
- uprawnienia do dokumentów.

##### Uprawnienia do modułów

Plugin dostarcza następujące role systemowe:
- (MAGAZYN) Administracja magazynem (dostęp do wszystkich modułów pluginu)
- (MAGAZYN) Obsługa magazynu (dostęp do wybranych modułów pluginu)

Brak wymaganych uprawnień do modułu zgłaszany jest poprzez odpowiednie komunikaty.

Nadawanie tych uprawnień odbywa się z poziomu edycji użytkownika LMS

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-200.png)

Użytkownik z rolą "(MAGAZYN) Administracja magazynem" może:

- uruchamiać wszystkie moduły i funkcje pluginu,
- zarządzać uprawnieniami do dokumentów oraz magazynów
- zarządzać słownikami

Użytkownik z rolą "(MAGAZYN) Obsługa magazynu" może uruchamiać tylko wybrane moduły i funkcje pluginu, które pozwolą mu:
- tworzyć producentów w słowniku,
- pracować na dokumentach magazynowych, do których uzyskają dostęp,
- sprawdzać stany magazynowe,
- uzupełniać katalog produktów i usług
- generować dokumenty handlowe na produkty magazynowe.

##### Uprawnienia do magazynów

Uprawnieniami może zarządzać tylko użytkownik z rolą "(MAGAZYN) Administracja magazynem" lub pełnym dostępem.

Każdy użytkownik, który będzie pracował z konkretnym magazynem musi mieć nadane uprawnienia do tego magazynu (niezależnie od uprawnień do modułów). Jeśli takich uprawnień nie będzie posiadał, nie będzie miał dostępu do danych o produktach powiązanych z tym magazynem. Możliwy będzie jedynie dostęp do katalogu produktów i usług.

Uprawnienia nadaje się poprzez uruchomienie z menu głównego "Magazyn-Słowniki->Prawa dostępu".

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-201.png)

Po kliknięciu w wiersz wybranego magazynu przechodzimy do nadania uprawnień do magazynu.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-202.png)

Uprawnienie do magazynu pozwala użytkownikowi na prowadzenie operacji magazynowych na tym magazynie poprzez dokumenty magazynowe.

Brak uprawnień do magazynu skutkuje tym, że użytkownik nie będzie mógł wystawić żadnego dokumentu powiązanego z tym magazynem i co więcej nawet nie będzie mógł podejrzeć jakichkolwiek operacji związanych z takim magazynem  oraz raportów, przykładowo nie będzie mógł sprawdzić stanów magazynowych na takim magazynie, albo wyświetlić listy dokumentów dotyczących magazynu.

##### Uprawnienia do dokumentów

Uprawnieniami może zarządzać tylko użytkownik z rolą "(MAGAZYN) Administracja magazynem" lub pełnym dostępem.

Uprawnienia nadaje się poprzez uruchomienie z menu głównego "Magazyn-Słowniki->Prawa dostępu". Po kliknięciu w wiersz wybranego dokumentu magazynowego przechodzimy do nadania uprawnień do magazynu.

Każdy użytkownik, który będzie pracował z magazynem musi mieć nadane uprawnienia do dokumentów (niezależnie od uprawnień do modułów). Uprawnienia pozwalają na zdefiniowanie dla każdego typu dokumentu dozwolonych operacji (podgląd(wydruk), tworzenie, edycja, usuwanie, zatwierdzanie). Dodatkowo, aby użytkownik mógł tych operacji używać musi mieć nadane uprawnienia do magazynu, którego dotyczą dokumenty.

![](https://www.chilan.com/lms-plus/screenshots/warehouse/wh-203.png)

Na przykładzie z powyższego slajdu możemy zaobserwować w jaki sposób można dzielić pracę i uprawnienia między pracownikami różnych szczebli. Widzimy, że użytkownik "Operator magazynu", który jest szeregowym pracownikiem, ma uprawnienia do podglądu, tworzenia i edycji dokumentu PZ. Pozwoli mu to na przygotowanie dokumentu do zatwierdzenia. Kiedy to zrobi, dla jego przełożonego, użytkownika "Administrator Magazynu", pozostanie tylko szybka weryfikacja dokumentu i zatwierdzenie. I gotowe. Dostawa przyjęta a menadżer się nie napracował.

Należy też pamiętać o uprawnieniach do magazynu. W powyższym przykładzie użytkownik "Administrator Magazynu" nie będzie mógł nic zrobić z dokumentem jeśli nie będzie miał uprawnień do magazynu, z którym jest powiązany dokument PZ.

##### Uprawnienia dla użytkowników wystawiających dokumenty sprzedażowe.

Aby użytkownik mógł wystawić dokument handlowy z pozycjami magazynowymi  powinien przynajmniej mieć:
- przypisaną rolę '(MAGAZYN) Obsługa magazynu',
- posiadać uprawnienia do magazynu sprzedaży,
- posiadać uprawnienie do podglądu WZ i WZk.

Dzięki tym minimalistycznym uprawnieniom dla użytkownika będzie możliwe:
- wystawienie faktury i powiązanego dokumentu WZ,
- podgląd dokumentu WZ
- wydrukowanie dokumentu WZ,
- wystawienie korekty faktury i korekty dokumentu WZ,
- podgląd dokumentu WZk
- wydrukowanie dokumentu WZk,
- przeglądanie listy dokumentów WZ i WZk,
- sprawdzanie stanów magazynowych na magazynie sprzedaży.

##### Brak uprawnień

Jeśli funkcje systemu nie działają w spodziewany sposób należy przede wszystkim sprawdzić czy użytkownik posiada wystarczające uprawnienia do wykonania działania.
