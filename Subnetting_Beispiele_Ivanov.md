# Übung Subnetting

## Übung 1

Bilde aus dem Netz 192.168.0.0 /24 4 Subnetze. Netze mit Mindestzahl an nutzbaren Host aber nicht darunter wählen: Netz a mit 20, Netz b mit 15, Netz c mit 30, und das Netz d mit den Rest Anteil der Netzwerkadressen.

Netz a mit 20,
Netz b mit 15,
Netz c mit 30, und das
Netz d mit den Rest Anteil der Netzwerkadresse

a) 0-31     --> 192.168.0.0 /27
c) 32 - 63  --> 192.168.0.32/27
b) 64 - 95  --> 192.168.0.64/27
d)          --> 192.168.0.128/25

Zusammen um unterricht gemacht

## Übung 2

Teile das Netz 193.170.20.0 /24 in 8 gleich große Netze! Erstelle eine Tabelle mit folgenden Angaben:

| Netzwerkadresse | Nutzbare Hosts | Broadcastadresse |  Subnetzmaske   |
|-----------------|----------------|------------------|-----------------|
| 193.170.20.0    | 1-126          | 127              | 255.255.255.224 |
| 193.170.20.128  | 128-253        | 254              | 255.255.255.224 |
| 193.170.21.0    | 1-126          | 127              | 255.255.255.224 |
| 193.170.21.128  | 128-253        | 254              | 255.255.255.224 |
| 193.170.22.0    | 1-126          | 127              | 255.255.255.224 |
| 193.170.22.128  | 128-253        | 254              | 255.255.255.224 |
| 193.170.23.0    | 1-126          | 127              | 255.255.255.224 |
| 193.170.23.128  | 128-253        | 254              | 255.255.255.224 |

193.170.20.0 /24
193.170.00010100.00000000 /27
              00.1		/27	In dezimal umgerechnet ergibt die Netzadresse
              01.0		/27
              01.1		/27
              10.0		/27
              10.1		/27
              11.0		/27
              11.1		/27

Selbst gelöst
Aufgabenstellung falsch interpretiert, jedoch das Grundprinzip des Subnettings verstanden.
Ich belasse die Aufgabe so wie ist jetzt, da das Ausbessern nach dem selben Prinzip gehen würde, nur eben in dem letzten oktet und nicht wie ich, schon im vorletzten.

## Übung 3

172.28.40.0 /26 Teile wie folgt auf: 2 Netze!
Erstelle eine Tabelle mit folgenden Angaben:
Netzwerkadresse,               nutzbare Hosts,                    Broadcastadresse,              Subnetzmaske.

172.28.40.0                    1-14                               172.28.40.15                    255.255.255.224  /27 32 IPs
172.28.40.16                   17-30                              172.28.40.31                    255.255.255.224  /27 32 IPs

Selbst gelöst

## Übung 4

Wie lautet die Subnetzmaske bei der Netzadresse: 17.0.0.0 mit 10 verwendbaren Subnetzen, sowie mit mindestens 12 Hosts je Subnetz?
Antwort in Sätzen, wie sie zu dieser Lösung kommen; und erstelle eine Tabelle:

Um die Subnetzmaske zu bestimmen, müssen wir zunächst die Anzahl der benötigten Subnetze und Hosts berücksichtigen. Für 10 Subnetze benötigen wir mindestens 4 Bits (2^4 = 16 Subnetze). Für mindestens 12 Hosts pro Subnetz benötigen wir 4 Bits (2^4 - 2 = 14 Hosts). Daher benötigen wir insgesamt 8 Bits für Subnetze und Hosts. Die Subnetzmaske ergibt sich somit aus der Addition dieser Bits zur Standard-Netzmaske der Klasse A (255.0.0.0).

Die Subnetzmaske lautet daher: 255.255.255.240 /28

| Subnetzadresse | Nutzbare Hosts | Broadcastadresse |  Subnetzmaske   |
|----------------|----------------|------------------|-----------------|
| 17.0.0.0       | 1-14           | 17.0.0.15        | 255.255.255.240 |
| 17.0.0.16      | 17-30          | 17.0.0.31        | 255.255.255.240 |
| 17.0.0.32      | 33-46          | 17.0.0.47        | 255.255.255.240 |
| 17.0.0.48      | 49-62          | 17.0.0.63        | 255.255.255.240 |
| 17.0.0.64      | 65-78          | 17.0.0.79        | 255.255.255.240 |
| 17.0.0.80      | 81-94          | 17.0.0.95        | 255.255.255.240 |
| 17.0.0.96      | 97-110         | 17.0.0.111       | 255.255.255.240 |
| 17.0.0.112     | 113-126        | 17.0.0.127       | 255.255.255.240 |
| 17.0.0.128     | 129-142        | 17.0.0.143       | 255.255.255.240 |
| 17.0.0.144     | 145-158        | 17.0.0.159       | 255.255.255.240 |

Gelöst mit Github Copilot

## Übung 5

Bestimmen Sie die Subnetmaske mit folgenden Angaben:

Netzadresse: 210.52.190.0
Subnetze: Anzahl 5
Mindestanzahl von Hosts je Subnetz: 10

Subnetmaske: 255.255.255.240
Abgelesen von: https://www.aelius.com/njh/subnet_sheet.html 

## Übung 6

Teile  ein /30 Netz auf!    Wozu werden diese /30 Netze am häufigsten verwendet?
Antwort: z.B. Eine Einzelverbindung zwischen Routern (Peer to Peer)

Improvisierte Angabe: 192.168.10.0 /24

192.168.10.0-3 Adressraum Usable ip --> 1-2 || NetAdd: .0 || BcAdd: .3 || NetMask: 255.255.255.252 /30

Selbst gelöst

## Übung 7

Nennen Sie den jeweiligen Netz- und Hostanteil der Klassen A, B und C

| Klasse | Netzanteil | Hostanteil |
|--------|------------|------------|
| A      | 8 Bits     | 24 Bits    |
| B      | 16 Bits    | 16 Bits    |
| C      | 24 Bits    | 8 Bits     |

Gelöst mit GitHub Copilot