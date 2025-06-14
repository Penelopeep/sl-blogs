# Seelen interfejs użytkownika: Metody instalacji i kanały aktualizacji

## Opcje instalacji

### Microsoft Store (MSIX)

Pobierz najnowszą wersję z [Microsoft Store](https://www.microsoft.com/store).
To jest najbezpieczniejsza opacja, przyjazna dla użytkownika z automatycznymi
aktualizacjami.

**Zalety:**

- Automatyczne aktualizacje
- Zweryfikowane i zatwierdzone przez Microsoft
- Wysokie bezpieczeństwo i niezawodność
- Mniejsza wielkość plików niż z instalatora .exe (bez symboli debugowania)

**Wady:**

- Aktualizacje mogą zająć 1-3 dni robocze do zatwierdzenia Microsoft
- Trudniejsza do debugowania i zgłaszania problemów

---

### Winget (MSIX)

Zainstaluj najnowszą wersję za pomocą następującego polecenia:

> winget install --id Seelen.SeelenUI

Oferuje takie same korzyści jak wersja sklepu Microsoft z wygodą
instalacji jedną komendą z wiersza poleceń.

---

### Instalator .exe

[//]: # (There's no good translation for "Releases page" in Polish, so I'll change it to "github")
Pobierz instalator setup.exe z
[githuba](https://github.com/eythaann/Seelen-UI/releases) i uruchom go.

**Zalety:**

- Dostępne natychmiastowe aktualizacje
- Otrzymuje powiadomienia o aktualizacji, gdy tylko nowe wersje zostaną wydane
- Lepsza do celów debugowania

**Wady:**

- Antywirus może oznaczyć ją jako niebezpieczeństwo (przez brak podpisu cyfrowego)
- Większy rozmiar pliku (zawiera symbole debugowania)

## Aktualizacja kanałów

> Niezależnie od wybranego kanału aktualizacji, wszystkie wersje odbierają
> automatyczne aktualizacje. Niestabilne kanały otrzymują również aktualizacje z
> bardziej stabilnych kanałów (np. Nightly otrzymuje aktualizacje zarówno z
> Nightly, jak i bety/stabilnego wydania).

### Stabilne wydanie (Release)

Najbezpieczniejszy i zalecany kanał dla wszystkich użytkowników.

**Cechy:**

- Dokładnie przetestowane bez krytycznych błędów
- Idealny do produkcji i codziennego użytku
- Dostępne w Microsoft Store, Winget (.msix) i jako instalator .exe

### Beta

Dla użytkowników, którzy chcą wczesnego dostępu do nowych funkcji przed
oficjalną wersją.

**Cechy:**

- Zawiera nadchodzące funkcje w testowaniu
- Może zawierać drobne błędy
- Częstsze aktualizacje niż stabilne
- Dostępny tylko jako instalator .exe

### Nightly

Dla zaawansowanych użytkowników i programistów chcą najnowszych zmian.

**Cechy:**

- Zawiera najnowsze, niesprawdzone zmiany
- Może obejmować błędy lub niekompletne funkcje
- Zaktualizowane codziennie lub z każdą znaczącą zmianą kodu
- Dostępny tylko jako instalator .exe

Dowiedz się więcej o kanale Nightly w naszej dokumentacji:
[Seelen UI Nightly](https://seelen.io/blog/nightly).

## Mechanizm aktualizacji: Setup.exe vs MSIX

- **MSIX:** Aktualizacje zarządzane automatycznie przez Microsoft Store
- **Setup.exe:** Zawiera wbudowany aktualizator, który powiadamia, gdy są
  dostępne aktualizacje

![Seelen UI update notification](https://github.com/Seelen-Inc/slu-blog/blob/master/blog/seelen-ui-distribution-channels/image.png?raw=true)

Gdy aktualizacja jest dostępna:

1. Kliknij powiadomienie
2. Aktualizator pobranie i zainstaluje aktualizację
3. Aplikacja ponownie uruchomi się automatycznie
