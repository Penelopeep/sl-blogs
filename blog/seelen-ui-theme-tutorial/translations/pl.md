# Seelen UI: Samouczek podstaw - Dostosuj swój pulpit jak profesjonalista!

![A beautifully customized desktop using Seelen UI themes](https://raw.githubusercontent.com/Seelen-Inc/sl-blogs/refs/heads/master/blog/seelen-ui-theme-tutorial/image.png)

Chcesz nadać swojemu komputerowi systemu Windows nowy nowy wygląd? Seelen UI
ułatwia to dzięki jego potężnemu systemu motywów. Ten przewodnik poprowadzi Cię przez
podstawy, jak działają motywy - brak znajomości kodowania!

## Specjalna wersja debugowania dla twórców motywów

Zanim zaczniemy, twórcy motywów powinni wiedzieć o naszej specjalnej **debugowalnej wersji** Seelen UI! Ta wersja pozwala ci:

- Sprawdź elementy, podobnie jak przeglądarka internetowa (CTRL+Shift+I Otwiera narzędzia deweloperskie)
- Zobacz zmiany HTML/CSS na żywo
- Testuj natychmiastowe modyfikacje motywu
- Łatwo debuguj problemy z stylowaniem

Pobierz wersję debugowania z naszego kanału [nightly](https://seelen.io/apps/seelen-ui/releases/nightly)
(Poszukaj plików kończących się `-debug.exe`, tak jak
`Seelen.UI_2.2.8+20250410073056_x64-setup-debug.exe`).

### Chcesz dowiedzieć się więcej o kompilacjach Nightly?

Sprawdź nasz artykuł odnośnie [kompilacji nightly](https://seelen.io/blog/seelen-ui-nightly)!

## Zrozumienie plików motywów

Pomyśl o motywach UI Seelen, takich jak warstwy farby. Możesz zastosować wiele
motywów naraz i tak jak z farbą, kolejność ma znaczenie! Motywy
mogą wszystko zmienić od kolorów po style okien.

Istnieją trzy sposoby, w jakie można pakować tematy:

1. **Motyw pojedynczego pliku** (plik .yml)
2. **Folder motywu** (zawiera wiele plików)
3. **Motyw skompresowany** (Plik .slu - specjalny format Seelen UI)

### Gdzie umieścić swoje motywy

Wszystkie motywy umieść w tym folder na komputerze:

```text
C:\Users\{YOUR_USERNAME}\AppData\Roaming\com.seelen.seelen-ui\themes
```

### Struktura folderu motywu

Oto, jak wygląda folder motywu w środku:

```text
C:\Users\{USER}\AppData\Roaming\com.seelen.seelen-ui\themes
├── YourThemeFolder             # the name of the folder doesn't matter
│   ├── theme.yml               # Theme metadata file
│   └── seelen                  # creator's username of widgets inside
│       ├── fancy-toolbar.css   # resource's name + css extension
│       └── window-manager.scss # supports SCSS too!
├── CompactTheme.yml            # Theme metadata file with styles inside
└── CompressedTheme.slu         # Special file format used on Seelen UI
```

## Inspiracja: przykładowe motywy

Nie wiesz, od czego i jak zacząć? Seelen UI ma kilka wbudowanych motywów, które możesz użyć jako inspiracji! 
Sprawdź [domyślną kolekcję motywów](https://github.com/eythaann/Seelen-UI/tree/master/static/themes),
aby zobaczyć, jak są stworzone.

## Praca z kolorami - jest to łatwiejsze niż myślisz!

Seelen UI automatycznie pobiera kolor akcentu Windows i tworzy paletę kolorów podobnych do niego do twojej dyspozycji.

### Twój główny kolor akcentu

Te zmienne używają koloru ustawionego w ustawieniach systemu Windows:

- `--config-accent-color`: Czysty kolor (jak #ffbbaa)
- `--config-accent-color-rgb`: Ten sam kolor w formacie RGB (255, 187, 170)

### Kompletna rodzina kolorów

Seelen UI tworzy całą paletę z twojego koloru akcentu:

![Visual guide to Seelen UI's color palette](https://raw.githubusercontent.com/Seelen-Inc/sl-blogs/refs/heads/master/blog/seelen-ui-theme-tutorial/colors.png)

Oto pełna lista dostępnych kolorów:

- Najciemniejsza wersja: `--config-accent-darkest-color`
- Ciemniejsza wersja: `--config-accent-darker-color`
- Ciemna wersja: `--config-accent-dark-color`
- Wersja zwykła: `--config-accent-color`
- Wersja lekka: `--config-accent-light-color`
- Lżejsza wersja: `--config-accent-lighter-color`
- Najlżejsza wersja: `--config-accent-lightest-color`

Każdy kolor ma również wersję RGB (z -rgb na końcu). To jest przydatne do tworzenia gradientów i innych efektów kolorów.

Jako przykładowe ustawienia kolor tła z przeźroczystością:

```css
background-color: rbga(var(--config-accent-darkest-color-rgb), 0.5);
```

### Jeszcze więcej opcji kolorów

Potrzebujesz większy wybór kolorów? Seelen UI dostarcza dziesiątki dodatkowych kolorów
systemu. Sprawdź [przydatną notkę odnośnie kolorów](https://gist.github.com/eythaann/cd9a3cda0206ce23a17f5ea00ec2ba06), dla wszystkich dostępnych opcji.

Wskazówka: Gdy zmienia się kolor systemu Windows, aktualizacje motywu Seleen UI są wykonywane
automatycznie!
