# Parameter und Rückgabewerte

Für die meisten Programme ist es unpraktisch, die berechneten Daten jedes Mal in der Konsole auszugeben (`print`) und anschließend wieder über die Konsole einzulesen. Daher können Methoden Übergabewerte (Parameter) und Rückgabewerte (Return Values) haben.

Nicht mehr sich, wie das funktioniert? Unten findest du Beispiele und Erklärungen oder schaue das Simpleclub [Video zu Methoden mit Parameter](https://youtu.be/oSDtCcDXcTM) und/oder das [Video zu Rückgabewerten](https://youtu.be/qQ79aq7HZ-U)

---
## Aufgabe
[//]: [task][Taschenrechner](AddStruct,SubStruct,MulStruct,DivStruct,AddBehave,SubBehave,MulBehave,DivBehave,ClassStruct)

Die Vorlage enthält bereits eine (noch sinnfrei programmierte) `addieren`-Methode. Im untenstehenden Klassendiagramm findest du 4 weitere Methoden, die zu implementieren sind.

Programmiere den Inhalt aller Methoden anhand ihres jeweiligen Namens. In der main-Methode kannst du die Methoden mit passenden Parametern aufrufen (ein Beispiel für die Addition ist bereits enthalten) und den Rückgabewert z.B. in der Konsole ausgeben.

---

## Klassendiagramm
```
+---------------------------------------------------------+
|                    Taschenrechner                       |
+---------------------------------------------------------+
|                                                         |
+---------------------------------------------------------+
| + static double addieren(double z1, double z2)          |
| + static double subtrahieren(double z1, double z2)      |
| + static double multiplizieren(double z1, double z2)    |
| + static double dividieren(double z1, double z2)        |
| + static double mittelwert(double z1, double z2)        |
+---------------------------------------------------------+
```

---

## Beispiele


### Beispiel 1: Parameter

Die Definition der Parameter erfolgt in den Klammern hinter dem Methodennamen und ähnelt sehr der Variablendefinition. Der Methodenkopf sieht dann beispielsweise so aus:
```java
public static void beispiel1(int ganzzahl, String text)
```

Parameter können innerhalb (also zwischen den geschweiften Klammern) einer Methode genauso wie Variablen verwendet werden – daher auch die Ähnlichkeit:
```java
public static void beispiel1(int ganzzahl, String text)
{
    System.out.println("Die Zahl "+ ganzzahl + " sieht ausgeschrieben so aus: " + text);
}
```

Der erste Wert eines Parameters wird beim Aufruf der entsprechenden Methode jedes Mal gesetzt. In Blockly machen wir das indem wir Werte an den Aufruf-Block hängen.


### Beispiel 2: Rückgabewerte

Natürlich können Werte nicht nur vom Aufrufenden an die Methode übergeben werden, sondern auch umgekehrt. Einen solchen Wert nennt man dann Rückgabewert.

Der Rückgabetyp (also der Typ des Rückgabewerts) wird ebenfalls im Methodenkopf festgelegt und steht immer unmittelbar vor dem Methodennamen. Wenn man keinen Rückgabewert benötigt, gibt man an dieser Stelle den Datentyp `void` an, um es für den Computer deutlich zu machen.

Beispiele für Methodenköpfe:
- `public static` **void** `beispiel1(int ganzzahl, String text)`
- `public static` **String** `beispiel2(int ganzzahl, String text)`

Als **letzter Schritt** der Methode wird der tatsächliche Wert zurückgegeben. Hierzu verwendet man das Schlüsselwort `return`, gefolgt von einem Leerzeichen und dem Wert oder der Variable, deren Wert man zurückgeben möchte. Nach dem Return-Statement endet eine Methode sofort.

```java
public static String beispiel2(int ganzzahl, String text)
{
    return "Die Zahl "+ ganzzahl + " sieht ausgeschrieben so aus: " + text;
}
```

### Beispiel 3: Mit Rückgabewerten arbeiten - Divide and Conquer
Mit dem Rückgabewert kann der Aufrufende (das bist entweder du oder eine andere Methode) natürlich weiterarbeiten. In `beispiel3` wird der Rückgabewert von `beispiel2` in die Variable `ausgabeText` gespeichert und anschließend auf der Konsole ausgegeben.

Diese Strukturierung ermöglicht der Programmiererin, ein großes Problem in mehrere kleinere Probleme zu zerlegen und diese anschließend nacheinander oder im Team zu bearbeiten. Dieses Vorgehen ist Teil des Konzepts **Divide and Conquer** und spiegelt damit einen der wichtigsten Ansätze der Informatik wider!

```java
public static void beispiel3(int ganzzahl, String text)
{
    String ausgabeText = beispiel2(ganzzahl, text);
    System.out.println(ausgabeText);
}
```
