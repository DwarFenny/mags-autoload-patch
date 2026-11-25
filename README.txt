Mags Autoload Patch v0.23 - AML plug-and-play (GAMMA Mags Reloaded 1.05)

Klawisz (domyslnie B, zmiana w MCM) skanuje ekwipunek i laduje tylko niepelne magazynki
oznaczone jako Loadout w Mags Reloaded. Oznaczone FMJ/AP/HP magazynki uzywaja klasyfikatora
amunicji Mags Reloaded, wiec nazwa naboju nie musi zawierac skrotu klasy; puste oznaczone
magazynki tez moga byc zaladowane. Dla oznaczonych magazynkow ustaw w MCM, co zrobic z juz
zaladowana inna amunicja: pominac magazynek, wymieszac klasy lub zwrocic stare naboje do
ekwipunku i zastapic je oznaczona klasa.

Naboje sa ladowane pojedynczo; interfejs odswieza sie po kazdym naboju.
Drugie nacisniecie klawisza lub klikniecie X na spinnerze przerywa kolejke.
Zamkniecie ekwipunku przerywa ja, chyba ze aktywne AML i opcja kontynuacji w MCM pozwalaja
na prace w terenie. Przy przerwaniu spinner jest czyszczony.
Przy aktywnym AML kolejka moze kontynuowac ladowanie, rozladowanie i balansowanie po zamknieciu
ekwipunku (opcja w MCM, domyslnie wlaczona po wykryciu AML i przy wlaczonym Field Loading).
Wyciagniecie broni, uzycie przedmiotu lub inna akcja zajmujaca rece przerywa cala kolejke.
MCM pozwala wybrac, czy sprint przerywa kolejke; domyslnie sprint ja przerywa.
Gdy AML i jego mostek sa aktywne, ladowanie (oraz rozladowanie przy trybie Replace) uzywa
animacji i dzwiekow AML. Bez aktywnego sterownika AML mod automatycznie wraca do standardowego
autoloadingu Mags Reloaded.
Mnoznik Autoload speed w MCM ma zakres 0.25-5.00: bez AML skaluje load_delay Mags Reloaded.
Przy wlaczonym AML (Animated Magazine Loading) predkosc animacji jest ograniczona do 2.0.
Predkosc bazowa AML ustawisz w MCM Mags Reloaded -> AML Load Animation Speed; wartosci
Autoload speed powyzej 2.00 nie przekrocza limitu AML.
Domyslny jezyk komunikatow to ENG (wybor PL pozostaje w MCM). Raport koncowy jest domyslnie wlaczony,
a debugowanie wylaczone.

Nowe opcje:
- Rownowazenie amunicji jest domyslnie wylaczone. Po wlaczeniu w MCM rozdziela naboje z magazynkow
  Loadoutu i luznych pudelek, aby wyrownac grupy. Przy uruchomieniu skanuje aktualny ekwipunek.
  Najpierw wykorzystuje naboje z pudelek; wyciaga z magazynkow tylko wyliczona nadwyzke, ktorej
  brakuje do rownego podzialu. Nie rozladowuje calego magazynka. Domyslnie dokladne typy amunicji
  sa rozdzielane osobno z uwzglednieniem oznaczen; opcjonalne mieszanie laczy magazynki o tej samej
  zgodnosci amunicji: najpierw uzywa dominujacego typu z magazynka, a inne typy dopiero po jego
  wyczerpaniu. Magazynki bez bezpiecznej grupy sa pomijane, a nadmiar ponad pojemnosc
  zostaje w pudelkach.
- Klawisz rownowazenia moze byc taki sam jak Autoload (domyslnie B) albo osobny (domyslnie N,
  zmieniany w MCM). Przy wspolnym klawiszu wlaczone rownowazenie zastepuje zwykle doladowanie.
- Osobna opcja rozladowuje tylko zaladowane magazynki spoza Loadoutu (nieoznaczone jako Loadout
  w Mags Reloaded); magazynki Loadoutu pozostaja nietkniete. Jest domyslnie wylaczona, a klawisz C
  mozna zmienic w MCM. Z AML rozladowanie korzysta z animacji AML; bez AML jest natychmiastowe.
- Czesciowe rozladowywanie potrzebne do rownowazenia odbywa sie pojedynczymi nabojami przez API
  Mags Reloaded. Przy aktywnym, zgodnym AML rozladowanie i ladowanie uzywaja animacji rak, ktora
  zatrzymuje sie po wykonaniu zaplanowanej liczby naboi. Bez aktywnego AML operacje przebiegaja
  pojedynczymi nabojami ze spinnerem i dzwiekiem Mags Reloaded.

Instalacja w MO2: Install a mod from an archive -> wybierz ten zip.
Wymagania dla AML:
- wlacz "Animated Magazine Loading" i zgodny mostek z moda "[Working for Animated Magazine Load";
- w MO2 ustaw "[Working for Animated Magazine Load]" PONIZEJ "GAMMA.Mags.Reloaded-1.05",
  aby fork z API AML mial wyzszy priorytet;
- w MCM Mags Reloaded ustaw Load behavior na "Individual";
- w MCM AML Compatibility wlacz AML.
Autoload sam wykrywa aktywne API; jesli warunki nie sa spelnione, zachowuje standardowe ladowanie.

Log: wlacz debug w MCM Mags Reloaded, szukaj linii [mags_autoload] w logu gry.
Odinstalowanie: wylacz mod (checkbox) w MO2.
Zmiana klawisza: MCM -> Mags Autoload -> Autoload key (dziala w trakcie gry).
