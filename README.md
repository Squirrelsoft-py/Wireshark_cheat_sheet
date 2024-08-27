# Informatik Labortag Netzwerke

# Einleitung

- ## Was ist Wireshark?
  
  - Open-Source-Paket-Analyse-Software
  - Netzwerkanalysewerkzeug
  - Erfasst und analysiert den Datenverkehr in Echtzeit
  - Dient zur Diagnose von Netzwerkproblemen und zur Sicherheitsüberwachung
  - Unterstützt eine Vielzahl von Netzwerkprotokollen
  - Kann den gesamten Datenverkehr oder spezifische Filter anzeigen
  - Kann Netzwerkverkehr Aufzeichnen und speichern

- ## Wozu wird Wireshark genutzt?
  
  - Netzwerkanalyse
    - Identifizierung von Bottlenecks
    - Leistungsproblemen
    - Sowie andere Netzwerk Problemen
  - Sicherheitsüberwachung
    - Erkennung von Angriffen
    - Überwachung von verdächtigem Datenverkehr
  - Protokollierung
    - Aufzeichnen und Analysieren des Datenverkehrs für spätere Überprüfung

- ## Wie ist Wireshark aufgebaut
  
  ![App Screenshot](https://i.imgur.com/115qLsm.png)

- ### 1
  
    Das zentrale Element des Hauptfensters ist das "Packet List"-Fenster. Hier werden alle erfassten Netzwerkpakete in tabellarischer Form angezeigt. Jede Zeile repräsentiert ein einzelnes Paket und enthält Informationen wie die Paketnummer, Zeitstempel, Quell- und Zieladresse, Protokoll, Länge des Pakets und andere relevante Details.

- ### 2
  
    Zusätzlich zu diesem Tabellenformat bietet Wireshark ein "Packet Details"-Fenster. Wenn ein bestimmtes Paket in der Liste ausgewählt wird, zeigt dieses Fenster eine detaillierte Analyse des Pakets an. Hier können Sie die Hierarchie der Protokollebene, die einzelnen Felder des Pakets und deren Werte im Hexadezimal- oder ASCII-Format betrachten.

- ### 3
  
    Das "Packet Bytes"-Fenster stellt den rohen Datenstrom des ausgewählten Pakets dar, was besonders nützlich ist, wenn Sie die genauen Bytes eines Pakets analysieren möchten.

- ### 4
  
    Die Filterleiste oberhalb des "Packet List"-Fensters ermöglicht es, gezielt nach bestimmten Protokollen, Quell- oder Zieladressen oder anderen Kriterien zu filtern, um den Fokus auf relevante Pakete zu legen.

- ## Wie funktionieren die Filter in Wireshark
  
  - ### Displayfilter
    
    - Ermöglichen die Filterung des auf der Benutzeroberfläche von Wireshark    angezeigten Netzwerkverkehrs
    - Können nach Protokollen, IP-Adressen, Ports und anderen Kriterien angewendet werden
    - Beispiel: ip.addr == 192.168.1.1 zeigt nur Pakete an, bei denen die IP-Adresse 192.168.1.1 beteiligt ist
    - Um nach bestimmten Protokollen zu filtern, kann man einfach den Protokollnamen in die Suchleiste eingeben
  
  - ### Logical Operators:
    
    - Ermöglichen die Kombination mehrerer Filterbedingungen
    - Gängige Operatoren sind and, or und not
    - Beispiel: ip.src == 192.168.1.1 and tcp.port == 80 zeigt nur TCP-Pakete an, die von der IP-Adresse 192.168.1.1 stammen und den Port 80 verwenden
    - Logische Operatoren helfen, komplexe Filterausdrücke zu erstellen
