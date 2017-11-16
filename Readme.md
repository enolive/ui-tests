# UI-Tests
## Symptome
* schlechte Wartbarkeit
* UI Test sind langsam
* Instabil
    * anfällig gegenüber Layoutänderungen

## Ursachen
* misachtung der Testpyramide
* Vernachlässigung von Test-Code
* sehr lange Durchlaufzeiten

# Nutzen von Tests
* Sicherstellung der Änderbarkeit des Codes
# Arten von Test
## Unit
Kleine Tests einzelner Einheiten

## Integration
Test einer kompletten Anwendung unter Umgehung der UI
Lassen sich mit den technischen Mitteln eines UnitTest realisieren.  

Abgrenzung von fremden Schichten durch künstlichen Schnittstellenzielen

## UI-Tests als UI-UnitTests
* Model und Controller werden durch Mocks ersetzt.
* Zustand eines mocked Controller resultiert in Zustand von UI.
* UI wirft ausschließlich Events, diese können auch per UnitTests ausgelöst werden. 

## UI-Test als elektronischer Anwender
* Möglichkeit über Testübergreifende Snapshots des UI-Aufbaus. Es können Änderungen überprüft werden, welche andernfalls nicht überprüfbar sind.
* Können also Akzeptanztest misbraucht werden um prinzipielles Funktionieren der Anwendung zu testen.
* Fehlerursache ist bei Fehlschlag eventuell nur sehr schwer zu erkennen.
* Menge der Abhängigkeiten tendenziell sehr groß
* Fehleranfällig durch äußere Einflüsse (Fehler durch Windows-Popup)

## Testbarkeit von UI
* wenn möglich Oberflächenzustände- und Logig unabhängig von Oberflächentechnologie gestalten.
* Auslagerung von UI-Events in Services