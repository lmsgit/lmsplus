## Dokumenty magazynowe

Każdy niezatwierdzony dokument trafia do bufora. Dokument niezatwierdzony nie ma wpływu na stany magazynowe, dopiero zatwierdzenie dokumentu powoduje, że wprowadzone w nim stany magazynowe zaczynają obowiązywać. Niezatwierdzony dokument można w każdej chwili edytować lub usunąć.

Każdy niezatwierdzony dokument posiada ten sam numer (0) i pełny numer według planu numeracyjnego. W momencie zatwierdzania dokumentu zostanie on w razie konieczności odpowiednio przenumerowany, aby zapewniona była ciągłość numeracji według planu numeracyjnego o czym użytkownik zostanie powiadomiony.

Możemy utworzyć jednocześnie kilka niezatwierdzonych dokumentów tego samego typu i zatwierdzać je w dowolnej kolejności. W takiej sytuacji podczas zatwierdzania dokumentu prowadzona jest kontrola dostępności produktów.

 Przykład:

Mamy na magazynie 5 sztuk 'Routera A'. 'Użytkownik X' wystawił dokument WZ-1 na 'Router A' w ilości 5 sztuk, ale jeszcze nie zatwierdził dokumentu. W tym samym czasie 'Użytkownik B' również wystawia dokument WZ-2 na 'Router A' w ilości 5 sztuk (są one dostępne bo 'Użytkownik A' nie zatwierdził dokumentu WZ-1) i zatwierdza dokument. Teraz 'Użytkownik A' próbując zatwierdzić dokument WZ-1 dostanie komunikat błędu mówiący o tym, że produktu, który oczekiwał już nie ma na magazynie (został w międzyczasie zdjęty przez 'Użytkownika B' dokumentem WZ-2).

 Podobne zabezpieczenia zaimplementowane są na poziomie egzemplarzy produktu.

 Przykład:

Mamy na magazynie egzemplarz 'SN123' produktu 'Router A'. 'Użytkownik X' wystawił dokument WZ-1 na egzemplarz 'SN123', ale jeszcze nie zatwierdził dokumentu. W tym samym czasie 'Użytkownik B' również wystawia dokument WZ-2 na egzemplarz 'SN123' (jest one dostępny bo 'Użytkownik A' nie zatwierdził dokumentu WZ-1) i zatwierdza dokument. Teraz 'Użytkownik A' próbując zatwierdzić dokument WZ-1 dostanie komunikat błędu mówiący o tym, że egzemplarza 'SN123', którego oczekiwał, już nie ma na magazynie (został w międzyczasie zdjęty przez 'Użytkownika B' dokumentem WZ-2).

Powyższy mechanizm blokad zapewnia nam możliwość bezpiecznej pracy dużej ilości użytkowników bez obawy o spójność stanów magazynowych.
