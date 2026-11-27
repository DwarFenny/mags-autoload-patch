# Mags Autoload Patch — raport projektu

## Cel

Mags Autoload Patch to dodatek do S.T.A.L.K.E.R. GAMMA, który rozszerza GAMMA
Mags Reloaded o automatyczne ładowanie magazynków Loadoutu oraz balansowanie
amunicji. Opcjonalnie współpracuje z Animated Magazine Loading (AML), aby
ładowanie i rozładowywanie korzystało z animacji.

## Aktualny stan

- Aktualna wersja: **v0.23**.
- Najnowsza paczka: `Mags_Autoload_Patch - by Fennu - AML v0.23.zip`.
- Użytkownik przetestował ostatnie zmiany i zgłosił, że działanie wydaje się
  prawidłowe.
- Walidacja techniczna obejmowała składnię Lua, XML MCM i zawartość ZIP.
- Zmiany w grze wymagają testów w GAMMA; walidacja statyczna ich nie zastępuje.

## Funkcje

- Klawisz autoloadu skanuje ekwipunek i uzupełnia niepełne magazynki Loadoutu.
- Zwykłe ładowanie korzysta z dominującego typu amunicji już w magazynku;
  oznaczone magazynki korzystają z klasy amunicji przypisanej do oznaczenia.
- Dla konfliktu amunicji w oznaczonym magazynku dostępne są tryby Skip, Mix
  i Replace.
- Opcjonalne balansowanie rozdziela amunicję między magazynki Loadoutu,
  najpierw używając luźnych nabojów, a rozładowując tylko zaplanowaną nadwyżkę.
- Przy włączonym mieszaniu w balansowaniu preferowany jest dominujący typ
  amunicji z magazynka; pozostałe kompatybilne typy są używane po wyczerpaniu
  preferowanego.
- Balansowanie może używać klawisza autoloadu albo osobnego klawisza.
- Opcjonalne rozładowywanie klawiszem C dotyczy magazynków spoza Loadoutu.
- AML zapewnia animacje, jeśli aktywny jest zgodny mostek i wymagane API.
- MCM zawiera wybór języka ENG/PL, ustawienie prędkości, widoczność raportu
  i opcję debugowania.
- Ładowanie można anulować ponownym naciśnięciem klawisza, kliknięciem X na
  spinnerze albo zamknięciem ekwipunku.
- Przy aktywnym AML kolejki mogą kontynuować działanie po zamknięciu ekwipunku.
  Sprint ma osobną opcję MCM; wyjęcie broni i inne akcje zajmujące ręce nadal
  przerywają całą kolejkę.

## Zależności i instalacja

- Wymagany: GAMMA Mags Reloaded 1.05.
- Opcjonalny: Animated Magazine Loading oraz zgodny mostek
  `[Working for Animated Magazine Load]`.
- Dla AML mostek musi mieć wyższy priorytet niż GAMMA.Mags.Reloaded-1.05,
  a tryb ładowania Mags Reloaded powinien być ustawiony na `Individual`.
- Mod instaluje się z ZIP-a w MO2. Szczegóły znajdują się w [README.txt](./README.txt).

## Główne pliki

- `gamedata/scripts/mags_autoload_mcm.script` — logika autoloadu, balansu,
  integracji AML, anulowania i raportowania.
- `gamedata/configs/text/eng/ui_mcm_mags_autoload.xml` — angielskie etykiety MCM.
- `gamedata/configs/text/pol/ui_mcm_mags_autoload.xml` — polskie etykiety MCM.
- `README.txt` — instalacja, zależności i opis funkcji.

## Przyszłe usprawnienia — TODO

- Rozszerzyć raport końcowy balansu o listę zmienionych magazynków i typów amunicji.
- Wyświetlać, które magazynki pominięto i z jakiego powodu.

Na obecnym etapie zalecane jest pozostawienie logiki bez dalszych zmian
i dodawanie usprawnień dopiero na podstawie kolejnych testów w grze.
