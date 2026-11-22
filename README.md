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

Diagramy są uproszczone: najwyżej 4 kroki na diagram (wyjątek: DFD poziom 0 z 5 podsystemami).

Terminatory: Klient, Pracownik, Menedżer, Dostawca, Kurier.

Magazyny danych: Zamówienia, Rezerwacje, Pracownicy i grafik, Stany magazynowe.
