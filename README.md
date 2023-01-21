# Berliner Debatte LaTeX Templates
 Vorlagen für den Satz eines Heftes der Berliner Debatte mit LaTeX

Dokumentation des LaTeX Style für Berliner Debatte Initial.

# Anlegen eines neuen Hefts

## Installation von LaTeX

LaTeXist ein Programm und eine Art der Dokumentauszeichnung.
LaTeXermöglicht, wissenschaftliche Arbeiten zu verfassen ebenso wie
Briefe, Präsentationen und auch Zeitschriften, wie die Berliner Debatte
Initial. Die Idee dahinter ist eine Fokussierung auf die Inhalte zu
ermöglichen und das Setzen des Textes beinahe vollständig zu
automatisieren.

LaTeXverwendet Befehle zum setzen des Textes. Jeder Befehl beginnt mit
einen \\gefolgt von einem Wort, z.B.

        \chapter

für ein neues Kapitel.

Formatierungen für die Inhalte werden von den Inhalten getrennt abgelegt
und durch die entsprechenden Befehle auf die Inhalte angewendet, z.B.

        \newfontfamily{\chapterfont}{WarnockPro-Regular.otf}
        \renewcommand\huge{\@setfontsize\huge{20}{20}}
        \addtokomafont{chapter}{\chapterfont\huge}

um jede Kapitelüberschrift im gesamten Dokument mit der Schriftart
Warnock-Pro Regular in Schriftgröße 20pt und einzeiligem Abstand zu
setzen.

# LaTeXauf deinem Computer installieren

Wichtig ist eine sogenannte LaTeXDistribution herunterzuladen. Unter
Windows empfiehlt sich Miktex[^1], unter MacOS empfiehlt sich MacTex[^2]

Das installieren von LaTeXfunktioniert genauso wie bei jedem anderen
Programm, Pakete herunterladen und anklicken und dann warten bis die
Installation fertig ist.

## LaTeXEditor

Darüber hinaus ist es sinnvoll einen Editor[^3] zu installieren, mit dem
du LaTeXDateien bearbeiten und kompilieren[^4] kannst. Den Editor musst
du herunterladen und auf deinem Computer installieren.

[Grundeinstellungen für ein neues Heft festlegen]{.image .placeholder
original-image-src="texstudio.png" original-image-title="fig:"}

Da LaTeXDateien reine Textdateien sind hilft ein Editor dabei den
Überblick zu behalten. So werden z.B. die Befehle farblich dargestellt
und das Bauen der PDF Datei kann auch aus dem Editor heraus erfolgen.
Ausserdem sieht man auf der linken Seite im Editor alle Dateien, die zum
Projekt gehören.

# Vorlagen herunterladen

Alle Vorlagen sind in einem öffentlich zugänglichen Speicher abgelegt.
Um ein neues Heft zu erstellen gehe bitte auf github.com und lade dir
das dazugehörige Paket herunter. Entpacke die Datei und starte den
LaTeXEditor. Öffne die Dateien, wie du es von Word oder Excel kennst.

# Struktur der Vorlage

Wenn du die Vorlage entpackt hast sind zwei neue Ordner entstanden.

1.  bdi-Style

2.  cover

Im Ordner \"bdi-style\" befinden sie alle Dateien für das Setzen des
Heft Inhalts.

Im Ordner \"cover\" findest du alle Dateien, die notwendig sind um das
Cover eines Hefts zu erstellen.

## Ordner bdi-style

Das Herzstück eines Hefts sind die Dateien bdi.tex und formats.tex.

### formats.tex {#formats.tex .unnumbered}

Diese Datei bitte **nicht** bearbeiten!

### bdi.tex {#bdi.tex .unnumbered}

In dieser Datei bitte in Zeile 9 ff. den Bereich Konfiguration anpassen
und in die geschweifte Klammer die Werte für ein neues Heft eintragen.

[Grundeinstellungen für ein neues Heft festlegen]{.image .placeholder
original-image-src="heftkonfiguration-festlegen.png"
original-image-title="fig:"}

1.  Zeile 10: Jahrgang

2.  Zeile 11: Jahr

3.  Zeile 12: Ausgabe (Heftnummer)

Aus den hier eingetragenen Werten ergibt sich automatisch die Ausgabe
auf dem Buchrücken und in den Kopfzeilen der einzelnen Seiten.

Weiter unten in der gleichen Datei werden die eigentlichen Inhalte des
Hefts eingebunden.

[Einbinden der Inhalte des Hefts]{.image .placeholder
original-image-src="Inhaltseinbindung.png" original-image-title="fig:"}

1.  toc.tex: Daraus wird das Inhaltsverzeichnis automatisch generiert

2.  kap1-x.tex: darin befinden sich die einzelnen Artikel des Hefts

# Inhalte einfügen

Um einen Artikel oder eine Rezension zu einem Heft hinzuzufügen sind
folgende Schritte notwendig.

1.  Vorlage Artikel.tex oder Rezension.tex duplizieren und umbenennen

2.  Einbinden in der Datei bdi.tex

3.  Einfügen der Inhalte in die neu erstellte Datei

## Erstellen eines Artikels

Kopiere die Vorlage Artikel.tex und benenne sie entsprechend um in
\"Name-des-Artikels.tex. Anschließend gehe in die Datei bdi.tex und
binde die Vorlage wie weiter oben beschrieben ein.

In der Vorlage findest du alle notwendigen Informationen um einen
normalen Text ohne Bilder und Tabellen richtig zu setzen.

## Erstellen eines Rezension

Kopiere die Vorlage Rezensionen.tex und benenne sie entsprechend um in
z.B. rezensionen.tex. Anschließend gehe in die Datei bdi.tex und binde
die Vorlage wie weiter oben beschrieben ein.

In der Vorlage findest du alle notwendigen Informationen um einen
normalen Text ohne Bilder und Tabellen richtig zu setzen.

## Überschriften Editorial

        \bdieditorial{Johanna Wischner, Thomas Müller}

**Resultat** ist die gesetzte Überschrift eines Editorials.

::: center
[image]{.image .placeholder original-image-src="editorial-headline.png"
original-image-title=""}
:::

## Überschriften Artikel

        \bdichapter{<AUTOREN>}{<>TITEL}{<FORMATIERTER TITEL>}{<UNTERTITEL>}

**Resultat** ist die gesetzte Überschrift eines Artikels.

::: center
[image]{.image .placeholder
original-image-src="rezensionen-headline.png" original-image-title=""}
:::

## Überschriften Rezensionen

        \bdirezension{Sonia Combe}{Loyal um jeden Preis.\smallskip „Linientreue Dissidenten“ im Sozialismus}{Ulrich Busch}

**Resultat** ist die gesetzte Überschrift einer Rezension.

::: center
[image]{.image .placeholder original-image-src="bdichapter.png"
original-image-title=""}
:::

## Absätze ohne Einrückung

        \noindent Jemand musste Josef K. 
    
        Jemand musste Josef K. 

**Resultat** ist das der Absatz nicht eingerückt wird. Der darauf
folgende Absatz wird normal eingerückt.

::: center
[image]{.image .placeholder original-image-src="noindent.png"
original-image-title=""}
:::

## Fettdruck und Kursivschrift

        Ein \textbf {großer Teil} des \textit{unveröffentlichten 
        Materials}, das in 

**Resultat** ist das die Worte in der Klammer nach dem Befehl Fett oder
Kursiv ausgegeben werden.

::: center
[image]{.image .placeholder original-image-src="fett-kursiv.png"
original-image-title=""}
:::

## Endnoten

        Vom Archiv zur Druckfassung\endnote{Übersetzte und 
        überarbeitete Fassung von „Walter Kempowski’s Das Echolot. 
        Abgesang ’45. From Archive to Print“, erschienen in: German 
        Life and Letters 66 (2013), Heft 4, S. 416-431 (German Life 
        and Letters © John Wiley \& Sons Ltd.). Mit freundlicher 
        Genehmigung des Verlags.}

**Resultat** ist das an der Stelle wo die Endnote im Text eingefügt
wurde ein Nummer erscheint und am Ende des Textes die Endnote ausgegeben
wird.

::: center
[image]{.image .placeholder
original-image-src="nummerierung-endnote.png" original-image-title=""}
:::

::: center
[image]{.image .placeholder original-image-src="endnote.png"
original-image-title=""}
:::

## Bibliografie

        begin{bibdescription}
            \item Franz Kafka, Der Prozess
            \item Eintrag 2
            \item Eintrag 3 
            \item etc. pp.
        \end{bibdescription}

**Resultat** ist eine fortlaufende und unnummerierte Liste der
Literaturangaben.

::: center
[image]{.image .placeholder
original-image-src="literaturverzeichnis.png" original-image-title=""}
:::

## Bilder

        \begin{figure*}
            \centering
            \caption{Stilisierte politische Einstellungen von 
            Gruppen mit hohem Bildungsniveau 
            (nach Kitschelt, Rehm 2022)}
            \includegraphics[scale=0.8]{brie-2.eps} 
        \end{figure*}

**Resultat** ein eingebundenes Bild mit einem Titel. Im Befehl oben
siehst du, dass du die Bildgröße anpassen kannst durch die Angabe scale,
der Wert 0.8 bedeutet: skaliere das Bild auf 80% Größe.

Die Formate der Bilder sollten .png, .jpg oder .eps sein. Die Beste
Qualität für den Ausdruck bietet das .eps Format, da es sich hierbei um
eine skalierbare Vektorgrafik handelt.

::: center
[image]{.image .placeholder original-image-src="bilder.png"
original-image-title=""}
:::

## Tabellen

Tabellen sind ein etwas komplexeres Thema. Tabellen sind in
LaTeXgrundsätzlich so aufgebaut:

        \begin{tabular*}
            \begin{tabular}{l|c|r}
                1 & 2 & 3 \\\hline
                4 & 5 & 6 \\
                7 & 8 & 9 \\
            \end{tabular}
        \end{tabular*}

1.  tabular\*: startet eine Umgebung, die sich an der passenden Stelle
    in den Text einklinkt und aus zwei Spalten eine macht.

2.  tabularl\|c\|r: startet die Tabelle und definiert die Anzahl der
    Spalten. Die Werte l, c, r stehen für die Ausrichtung des Texts
    innerhalb der Spalte.

3.  1 & 2 & 3 \\\\: die Zahlen sind der Inhalt der Tabelle, das & ist
    der Spaltentrenner und \\\\sind der Umbruch in die näcshte
    Tabellenzeile.

4.  \\hline am ende der ersten Zeile setzt eine horizontale Linie unter
    die erste Zeile.

**Resultat** ist eine Tabelle mit 3 Spalten und 3 Zeilen, die erste
Spalte hat eine Linie unten.

  1    2    3

--- --- ---

  4    5    6
  7    8    9

Komplexere Tabellen sollten idealerweise nicht manuell eingegeben
werden, da die Wahrscheinlichkeit einen Fehler zu machen recht hoch ist.
Es existiert ein Onlinetool \"Table Maker\", dort können Tabellen aus
Word oder Excel einfach reinkopiert werden und eine LaTeXÜbersetzung
erstellt werden, die dann von dort einfach ins LaTeXDokument kopiert
wird. (URL: https://www.latex-tables.com/v3/index.html)

::: center
[image]{.image .placeholder original-image-src="bilder.png"
original-image-title=""}
:::

Hier findest du folgende Dateien zum Bearbeiten vor.

1.  formats.tex

2.  bdi.tex

3.  hyphenation.tex

4.  toc.tex

[^1]: https://miktex.org/download/ctan/systems/win32/miktex/setup/windows-x64/basic-miktex-22.10-x64.exe

[^2]: https://www.tug.org/mactex/mactex-download.html

[^3]: https://www.texstudio.org/ Download für Windows oder Mac

[^4]: Aus dem Textdokument das Heft erzeugen, ähnlich dem Übersetzen

    eines Textes von einer Sprache in eine andere Sprache
