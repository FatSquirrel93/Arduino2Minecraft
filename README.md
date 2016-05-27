Dieses Minecraft Spigot Server Plugin dient als Schnittstelle zwischen der Server Welt und dem Arduino.
Die Kommunikation erfolgt seriell �ber das USB-Kabel. Die Befehle werden als String, welcher mit einem Zeilenumbruch(\n) endet, �bertragen.

Das Dokument minecraftInput.pdf skizziert, wie ein Ereignis beim Arduino zum Server �bertragen werden und dort ein Ereignis ausgel�st wird.
Das Dokument minecraftOutput.pdf zeigt, wie Informationen vom Server zum Arduino �bertragen werden und dort ein Ereignis ausl�sen.

Das Plugin legt unter plugins/Arduino2Minecraft/config.yml eine Konfigurationsdatei an. Diese kann bearbeitet werden.

#Beispiel f�r Arduino -> Minecraft:

Der Arduino sendet einen Befehl mit einem Linebreak.
z.B. k�nnte der Arduino den Wert "knopf1\n"

In der Konfigurationsdatei muss am Ende der Datei die Zeile "arduino_[arduino_wert]: [mein_befehl]" eingef�gt werden.
Wenn der Spieler Player1 gekickt werden soll, wenn der Arduino den Wert "knopf1\n" sendet, muss folgendes eingef�gt werden:
arduino_knopf1: kick Player1

Die Beispieldateien findest du im Ordner beispiel_knopf1
