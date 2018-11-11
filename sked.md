## Sked - das Kalender AddOn

<p class="intro">Das AddOn Sked kann als Basis für die Umsetzung aller Arten von Kalender eingesetzt werden. Mehrsprachigkeit ist ebenso bereits vorgesehen wie die Erweiterung um eigene Datenfelder per 1-Zeilen Konfiguration.</p>

Sked ist eines der jüngeren AddOns für REDAXO. Im September 2017 erschien die erste Version. Das Thema beschäftigte viele Entwickler*nnen schon lange. Auf jedem REDAXO-Tag gab es eine oder mehrere Anfragen „gibt es einen Veranstaltungskalender“. Wer sich mit dem Thema Kalender schonmal beschäftigt hat, der weiß wie vielfältig und wie unterschiedlich die Anforderungen an einen Kalender sein können. Das kann von einer einfachen Auflistung eintägiger Termine bis zu einer mehrsprachigen Seminarplanung mit diversen Kategorien gehen. Der eine braucht wiederkehrende Termine, der andere einen Raumbelegungsplan. Da erschien es mir eher unwahrscheinlich, dass es dafür ein passendes AddOn geben könnte.

Wir werfen aber einfach mal einen Blick unter die Haube. Die Anzeigemaschine von Sked im Backend basiert auf dem Fullcalendar. Damit steht eine solide Basis für die Darstellung zur Verfügung. Sked selbst bringt bei der Installation Tabellen und Verwaltungsmöglichkeiten für Termine, Orte und Kategorien mit. Es lassen sich Anfangs- und Enddatum und Uhrzeit für jeden Termin pflegen. Auch wöchentlich, monatlich oder jährlich wiederkehrende Termine in einstellbaren Intervallen sind vorgesehen.

Für eine einfache Terminliste mag uns das AddOn auf den ersten Blick zu komplex vorkommen. Da mag vielleicht eine einfache yform Tabelle einfacher erscheinen. Für einen anderen Fall stehen möglicherweise nicht genügend Eingabefelder zur Verfügung. So könnte es beispielsweise wünschenswert sein für die Orte noch ein Geofeld für eine Kartenanzeige zur Verfügung zu haben.

### Sked Backend - Kalenderdarstellung

Kalenderdarstellung im Backend von Sked. Ein Klick auf einen Termin zeigt den Eintrag in der Detailansicht. Kategorien können nach eigenen Vorstellungen angelegt und angepasst werden.

### Modifiziertes Backend in Sked

Beispiel eines modifizierten Backends. "Orte" werden in diesem Falle nicht gebraucht. Auch mehrtägige Termine werden nicht benötigt. Veranstaltungskategorien werden in diesem Beispiel als Vorlagen verwendet, da es viele gleichartige Termine gibt, bei denen die Merkmale nicht einzeln verwaltet werden müssen.

Bei den Individualisierungswünschen kommt einem der modulare Aufbau von Sked entgegen. Sked ist nämlich bereits so programmiert, dass eine Individualisierung weitestgehend möglich ist. Hierfür stehen beispielsweise eigene Config Dateien zur Verfügung, die bei einem Sked Update auch erhalten bleiben. In diesen Dateien lassen sich eigene Felder definieren. Die Definition alleine genügt! Sked legt die Felder dann beim nächsten Aufruf in der Tabelle an und stellt sie im Backend zur Verfügung. Manchmal reicht auch dies nicht für die eigenen Bedürfnisse. Dann lassen sich Sked Tabellen auch in yform Tabellen migrieren und entsprechend anpassen und erweitern.

Individualisierungen von Sked kann man aber auch per Javascript und CSS vornehmen. Eine Anregung, wie man dabei vorgehen kann, findet sich in den Tipps: (https://friendsofredaxo.github.io/tricks/addons/sked/config)

### Ausgabe

Wie sollen die Termine nun ausgegeben werden? Sked selbst verfügt über keine Modulausgabe. Das ist der in der Einleitung beschriebenen Tatsache geschuldet, dass der Einsatz von Sked doch sehr vielfältig sein kann. Es gibt verschiedene Möglichkeiten der Ausgabe. Im Doku Plugin von Sked gibt es ein Modulbeispiel. Man kann die Daten einfach per rex_sql aus der Datenbank ziehen oder sich entsprechende yorm Objekte erstellen. Ein Beispiel hierfür findet sich ebenfalls im oben genannten Tricks Artikel. Sked enthält eine API zur Ausgabe und Filterung der Events als JSON.

Das zusätzliche AddOn sked_ics von Alexander Walther erlaubt einen Import von ical Dateien aus einer fremden Quelle in die Datentabelle von Sked per Cronjob. sked_ics enthält außerdem die Ausgabemöglichkeit von ical Daten und die Erstellung von Terminen im JSON-LD Format.

### Beispiele

(https://www.zinzendorfschulen.de/aktuelles/termine.html)

(https://www.hotelamfischmarkt.com/aktuelles/)

(https://www.skiclub-bingen.de/termine/)

[zur AddOn Übersicht](/)
