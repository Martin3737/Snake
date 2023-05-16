# Snake
## Cíl projektu
Uživatel bude ovládat šipkami hada, který se bude pohybovat ve vyhraničeném poli. Pokud sní blok had se zvětší o 1 blok. Pokud narazí do vyhraničeného pole, hra se restartuje. 
## Zvolené technologie
Visual Studio, náročnost: střední C#


--------------------------------------------------------------
# Projektová dokumentace hry Snake v C#
Aplikace: Jedná se o hru Snake, kde hráč ovládá hada, sbírá jídlo a snaží se co nejdéle přežít.
Použité technologie:
C# (programovací jazyk)
Windows Forms (grafické rozhraní)
GDI+ (grafická knihovna pro kreslení na plátno)
Popis fungování uvnitř: Hra má několik funkcí, které řídí chování hada a interakci s uživatelem.
KeyIsDown a KeyIsUp: Tyto funkce ovládají hada pomocí klávesnice. Pokud uživatel zmáčkne klávesu, která ovládá pohyb hada, nastaví se příslušná boolean proměnná (goLeft, goRight, goDown, goUp) na true. Pokud uživatel klávesu pustí, boolean proměnná se nastaví na false.
StartGame: Tato funkce slouží k inicializaci hry a spuštění nové hry. Funkce vyvolá RestartGame().
TakeSnapShot: Tato funkce slouží k vytvoření snímku obrazovky hry. Kód vytvoří novou bitmapu a nakreslí do ní obsah okna aplikace. Poté se bitmapa uloží do souboru s názvem "Snake Game".
GameTimerEvent: Tato funkce je spuštěna při každém ticku timeru a řídí celou hru. Funkce nejprve zjistí, kterým směrem se had má pohnout a přepíše hodnotu globální proměnné directions. Poté projde všechny části hada a přesune je o jedno políčko dle směru hada. Pokud se hlava hada dostane na stejné místo jako jídlo, volá se funkce EatFood(), která přidá novou část hada. Dále funkce zkontroluje, zda had nenarazil do zdi nebo do sebe sama. Pokud ano, volá se funkce GameOver().
UpdatePictureBoxGraphics: Tato funkce se stará o kreslení herního plátna. Nejprve se smaže starý obsah plátna a nakreslí se nový obsah. Kód projde všechny části hada a nakreslí je do plátna, poté nakreslí jídlo.
EatFood: Tato funkce se stará o přidání nové části hada na správné místo po sežrání jídla. Dále funkce zvýší skóre a upraví hodnotu high score, pokud je skóre větší než high score.
Funkce GameOver() se spouští, když had narazí do zdi nebo do sebe sama. Nejprve se zastaví herní timer a zobrazí se dialogové okno s informací o tom, že hra skončila a s možností spustit novou hru nebo ukončit hru. Pokud uživatel stiskne tlačítko pro novou hru, volá se funkce RestartGame(), která inicializuje novou hru. Pokud uživatel stiskne tlačítko pro ukončení hry, aplikace se ukončí.
Při ukončení hry se dále uloží aktuální skóre do souboru s názvem "SnakeHighScores.txt", pokud je skóre vyšší než aktuální nejlepší skóre. Pokud je skóre nižší, nic se neukládá. Dále se vypíše aktuální skóre a nejlepší skóre do konzole, aby uživatel mohl vidět svůj výkon.

Návod na použití projektu:
Spusťte aplikaci "SnakeGame.exe".
Klepněte na tlačítko "Start".
Použijte šipky na klávesnici k ovládání hada.
Snažte se sbírat jídlo a vyhýbat se střetům s okraji obrazovky nebo samotným hadem.
Pokud zemřete, klikněte na tlačítko "Restart".
Pokud chcete uložit snímek obrazovky, klikněte na tlačítko "Take a snapshot".
Možný rozvoj v budoucnu/popis reálného využití projektu:
Tento projekt lze dále rozvíjet například přidáním více úrovní obtížnosti, implementováním dalších herních prvků, jako jsou bonusové předměty, nebo přidáním více hráčů do hry.
Hra s hadem může být také použita jako zábavná a interaktivní vzdělávací hra pro děti, která pomáhá rozvíjet jejich dovednosti, jako jsou pozornost a reakční časy. Lze ji také využít k rozvoji dovedností programování pro začátečníky, kteří by chtěli vytvořit vlastní hru s použitím C# a Windows Forms.

