# Wycena roboczogodzin – System obsługi pizzerii

Wycena dla każdego modułu (diagramu przepływu danych poziomu 1). Moduły są niezależne i mogą być sprzedawane
osobno; moduł dowozu wymaga modułu zamówień.

## 1. Obsługa zamówień

| Aktor | Zadania | Rezultat | Podstawa estymacji | Czas |
|---|---|---|---|---|
| analityk | statusy zamówienia, reguły dostępności składników i płatności | dokumentacja | 5 statusów, 4 reguły | 8h |
| programista | model zamówienia i pozycji zamówienia | tabele, ORM, migracja | 2 tabele, 1 API, testy, skrypty, dokumentacja | 12h |
| programista | przyjęcie zamówienia, kontrola dostępności składników | funkcjonalność | 2 procesy, 3 testy, logika | 16h |
| programista | przyjęcie płatności, wystawienie rachunku | funkcjonalność | 1 integracja płatności, 2 testy, logika | 24h |
| programista | zlecenie przygotowania, rejestracja gotowości, powiadomienie kelnera | funkcjonalność | 2 procesy, 1 powiadomienie, 2 testy | 16h |
| programista | UI powyższej logiki (zamówienie, płatność, widok kuchni) | Figma | 4 ekrany | 24h |
| tester | testy e2e, QA | wyniki testu | 4 scenariusze | 12h |
| **Suma** | | | | **112h** |

## 2. Obsługa rezerwacji stolików

| Aktor | Zadania | Rezultat | Podstawa estymacji | Czas |
|---|---|---|---|---|
| analityk | statusy rezerwacji, reguły (czas trwania, liczba osób, anulowanie) | dokumentacja | 3 statusy, 4 reguły | 8h |
| programista | model rezerwacji i stolików | tabele, ORM, migracja | 2 tabele, 1 API, testy, skrypty, dokumentacja | 8h |
| programista | sprawdzanie dostępności, zapis i anulowanie, kontrola nakładania się rezerwacji | funkcjonalność | 2 procesy, 3 testy, logika | 16h |
| programista | UI powyższej logiki (kalendarz stolików dla kelnera, formularz online dla klienta) | Figma | 2 ekrany, 1 powiadomienie | 16h |
| tester | testy e2e, QA obu kanałów (kelner, internet) | wyniki testu | 2 kanały × 2 scenariusze | 8h |
| **Suma** | | | | **56h** |

## 3. Obsługa HR

| Aktor | Zadania | Rezultat | Podstawa estymacji | Czas |
|---|---|---|---|---|
| analityk | dane kadrowe, zasady grafiku i ewidencji czasu pracy, wymagania RODO | dokumentacja | 3 reguły, RODO | 8h |
| programista | model pracownika, grafiku i ewidencji czasu | tabele, ORM, migracja | 3 tabele, 1 API, testy, skrypty, dokumentacja | 12h |
| programista | zapis grafiku, ewidencja wejść i wyjść, zgodność z grafikiem | funkcjonalność | 2 procesy, 3 testy, logika | 16h |
| programista | raport czasu pracy | raport | 1 raport, eksport PDF/CSV | 8h |
| programista | UI powyższej logiki (kartoteka, grafik, rejestracja czasu) | Figma | 3 ekrany | 16h |
| tester | testy e2e, QA | wyniki testu | 3 scenariusze | 8h |
| **Suma** | | | | **68h** |

## 4. Obsługa stanów magazynowych

| Aktor | Zadania | Rezultat | Podstawa estymacji | Czas |
|---|---|---|---|---|
| analityk | jednostki, stany minimalne, zasady akceptacji zamówień towaru | dokumentacja | 3 reguły | 8h |
| programista | model składnika, stanu magazynowego i zamówienia towaru | tabele, ORM, migracja | 3 tabele, 1 API, testy, skrypty, dokumentacja | 12h |
| programista | rejestracja zużycia, aktualizacja stanów, kontrola stanu minimalnego | funkcjonalność | 2 procesy, 3 testy, logika | 16h |
| programista | zamówienie towaru (akceptacja menedżera, wysyłka do dostawcy), przyjęcie dostawy | funkcjonalność | 2 procesy, 1 wiadomość do dostawcy, 2 testy | 16h |
| programista | UI powyższej logiki (raport zużycia, stany, akceptacja zamówień) | Figma | 3 ekrany | 16h |
| tester | testy e2e, QA | wyniki testu | 3 scenariusze | 8h |
| **Suma** | | | | **76h** |

## 5. Obsługa dowozu

| Aktor | Zadania | Rezultat | Podstawa estymacji | Czas |
|---|---|---|---|---|
| analityk | statusy dostawy, zasady przydziału kuriera, strefy dostaw | dokumentacja | 3 statusy, 3 reguły | 8h |
| programista | model kursu i kuriera, odczyt zamówień z modułu zamówień | tabele, ORM, migracja | 2 tabele, 1 API, testy, skrypty, dokumentacja | 8h |
| programista | przydział kuriera, rejestracja doręczenia, aktualizacja statusu zamówienia | funkcjonalność | 2 procesy, 3 testy, logika | 16h |
| programista | UI powyższej logiki (lista zleceń i potwierdzenie doręczenia dla kuriera) | Figma | 2 ekrany | 16h |
| tester | testy e2e, QA (razem z modułem zamówień) | wyniki testu | 3 scenariusze | 8h |
| **Suma** | | | | **56h** |

## Podsumowanie

| Moduł | Czas |
|---|---|
| Obsługa zamówień | 112h |
| Obsługa rezerwacji stolików | 56h |
| Obsługa HR | 68h |
| Obsługa stanów magazynowych | 76h |
| Obsługa dowozu | 56h |
| **Razem** | **368h** |
