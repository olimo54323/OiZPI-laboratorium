# OiZPI-laboratorium

## Pizzeria – diagramy analizy strukturalnej (draw.io)

Notacja: diagramy kontekstowy i przepływu danych w notacji Yourdon/DeMarco (proces – koło,
terminator – prostokąt, magazyn danych – dwie poziome linie); przepływ sterowania jako schemat blokowy
(start/koniec – elipsa, krok – prostokąt, decyzja – romb).

| Plik | Zawartość |
|---|---|
| `diagramy/01_kontekstowy/kontekst_pizzeria.drawio` | diagram kontekstowy całego systemu |
| `diagramy/02_przeplyw_danych/dfd_0_pizzeria.drawio` | DFD poziom 0 – podział na 5 podsystemów |
| `diagramy/02_przeplyw_danych/dfd_1_zamowienia.drawio` | DFD poziom 1 – obsługa zamówień |
| `diagramy/02_przeplyw_danych/dfd_2_rezerwacje.drawio` | DFD poziom 1 – obsługa stolików (rezerwacji) |
| `diagramy/02_przeplyw_danych/dfd_3_hr.drawio` | DFD poziom 1 – obsługa HR |
| `diagramy/02_przeplyw_danych/dfd_4_magazyn.drawio` | DFD poziom 1 – obsługa stanów magazynowych |
| `diagramy/02_przeplyw_danych/dfd_5_dowoz.drawio` | DFD poziom 1 – system dowozu |
| `diagramy/03_przeplyw_sterowania/cfd_1_zamowienia.drawio` | przepływ sterowania – obsługa zamówień |
| `diagramy/03_przeplyw_sterowania/cfd_2_rezerwacje.drawio` | przepływ sterowania – obsługa stolików (rezerwacji) |
| `diagramy/03_przeplyw_sterowania/cfd_3_hr.drawio` | przepływ sterowania – obsługa HR |
| `diagramy/03_przeplyw_sterowania/cfd_4_magazyn.drawio` | przepływ sterowania – obsługa stanów magazynowych |
| `diagramy/03_przeplyw_sterowania/cfd_5_dowoz.drawio` | przepływ sterowania – system dowozu |

### Moduły

System jest modułowy – każdy proces DFD poziomu 0 to osobny moduł, który można sprzedawać oddzielnie:
obsługa zamówień, obsługa rezerwacji stolików, obsługa HR, obsługa stanów magazynowych, obsługa dowozu.
Moduły zamówień i dowozu łączą się wyłącznie przez magazyn danych „Zamówienia” (dowóz jest dodatkiem
do zamówień); moduły rezerwacji, HR i magazynu działają samodzielnie.

### Założenia

- Płatność przy składaniu zamówienia – potwierdzona płatność uruchamia przygotowanie w kuchni.
- Rezerwacje przyjmuje kelner (telefon, sala) albo klient sam przez internet.
- Kucharz zgłasza zużycie składników i gotowość zamówienia; menedżer akceptuje zamówienie towaru.
- Gotowe zamówienie wydaje kelner (na miejscu, na wynos) albo kurier (dowóz).

### Słownik

Terminatory: Klient, Kelner, Kucharz, Kurier, Menedżer, Pracownik, Dostawca.

Magazyny danych: Zamówienia, Rezerwacje, Pracownicy i grafik, Stany magazynowe.

Przepływy danych (ta sama nazwa na każdym poziomie):

| Obszar | Przepływy |
|---|---|
| Zamówienia | zamówienie, potwierdzenie zamówienia, płatność, rachunek, status zamówienia, zlecenie przygotowania, zgłoszenie gotowości, powiadomienie o gotowym zamówieniu |
| Rezerwacje | zapytanie o termin, wolne stoliki, rezerwacja, potwierdzenie rezerwacji, anulowanie rezerwacji |
| Magazyn | raport zużycia, stan magazynowy, zamówienie towaru do akceptacji, akceptacja zamówienia towaru, zamówienie towaru, dostawa |
| HR | dane pracownika, grafik, czas pracy, raport czasu pracy |
| Dowóz | gotowość kuriera, zlecenie dostawy, potwierdzenie doręczenia |
