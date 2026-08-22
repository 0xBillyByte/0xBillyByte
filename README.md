## Hallo, ich bin Billynary

Lernender Informatiker aus der Schweiz. Mich interessiert vor allem die Stelle,
an der Security, Infrastruktur und Automatisierung zusammenlaufen: Systeme
bauen, sie danach selbst auseinandernehmen und daraus lernen, wie man sie beim
nächsten Mal robuster baut.

Am liebsten arbeite ich an Dingen, die ich danach wirklich selbst benutze. Fast
alles hier läuft bei mir zuhause im eigenen Labor produktiv.

## Woran ich gerade arbeite

**[Vulnerability-Scanner](https://github.com/Billynary/Vulnerability-Scanner)**
Selbst gehostetes Schwachstellenmanagement, das Nessus, Nucleus und Aikido durch
ein einziges Werkzeug ersetzt. Vier Scanner (nmap, Ansible-Paketinventar, Trivy
für Abhängigkeiten und Images) schreiben in dieselbe Findings-Tabelle, Befunde
werden über ihre Aliase zusammengeführt und nach CVSS, EPSS, CISA KEV und
Asset-Gewicht priorisiert. Kern ist ein Scope-Guard, der dreifach durchsetzt, was
überhaupt gescannt werden darf. Python, FastAPI, PostgreSQL, React.

**[OSINT](https://github.com/Billynary/OSINT)**
Recherchewerkzeug mit fünf Modulen: Namenssuche über 16 offene Quellen,
Username-Check, Domain- und Infrastrukturrecherche, defensive E-Mail-Analyse und
EXIF-Auswertung. Ausschliesslich offizielle APIs und öffentliche Quellen, kein
Scraping. Die Treffer kommen als Server-Sent Events herein, damit eine langsame
Quelle nicht die ganze Suche aufhält. React und Express.

**[cit](https://github.com/Billynary/cit)**
Ein Git-Werkzeug fürs Terminal, das die Stärken von GitLens (Commit-Graph, Blame,
Diffs) mit der GitHub-Anbindung (Pull Requests, Checks, Reviews) verbindet.
Inklusive eigenem Lane-Algorithmus für den Graphen und einer Konfliktansicht mit
Auflösung pro Hunk. TypeScript und Ink.

**[Scraper](https://github.com/Billynary/Scraper)**
Watcher für Wohnungen, Flüge, Hotels und Tickets. Erkennt Änderungen gegenüber
dem letzten Lauf und meldet sie per Telegram. Offizielle APIs vor HTML-Scraping,
robots.txt wird durchgesetzt statt nur protokolliert, und der gesamte
Netzwerkverkehr läuft durch einen einzigen höflichen HTTP-Client, damit keine
Quelle die Regeln umgehen kann. Python.

**[Monkstore](https://github.com/Billynary/Monkstore)**
Ein absichtlich verwundbarer NFT-Marktplatz als eigenes Security-Labor. Der Kern
ist bewusst sauber gebaut (argon2id, Zod-Validierung, Prisma), damit die
eingebauten Lücken realistisch wirken. Neben den Lehrbuchklassikern stecken die
interessanteren Fehler in der Geschäftslogik: Preismanipulation, eine Race
Condition beim Kauf und ein Webhook ohne Signaturprüfung. Fastify und TypeScript.

**[EatAI](https://github.com/Billynary/EatAI)**
Lebensmittelverwaltung mit Ablaufwarnungen, Einkaufsliste und Rezeptvorschlägen
aus den vorhandenen Zutaten. Bewusst ohne Frontend-Framework. Express und
PostgreSQL.

Dazu kommen ein paar Dinge, die nicht öffentlich liegen: die Infrastructure as
Code für mein Homelab und eine selbst gehostete Plattform, in der ich Ziele,
Noten, Finanzen und Gewohnheiten zusammenführe.

## Mein Homelab

Der eigentliche Lernort. Ein Proxmox-Host, rund 20 Systeme in vier VLANs,
vollständig als Code beschrieben: OpenTofu provisioniert, Ansible konfiguriert,
je Service eine eigene Datei.

Was dort läuft und wobei ich am meisten gelernt habe:

* Eine zweistufige interne PKI mit step-ca, die Traefik per ACME automatisch mit
  Zertifikaten versorgt
* Autoritatives DNS mit BIND9 und Split-DNS, die Zone wird aus dem Ansible-Inventar
  generiert und kann deshalb nicht davon abweichen
* Zitadel als zentraler OIDC-Provider für alle Dienste, die föderieren können
* Ein selbst gehostetes Mesh-VPN mit Headscale statt eines fremden Koordinationsdienstes
* Ein einzelner Kubernetes-Node mit k3s, bewusst als VM statt als Container im Container
* Eine isolierte Datenbank pro Dienst statt einer zentralen Instanz, nachdem mir
  klar wurde, wie gross der geteilte Schadensradius vorher war

## Was mich interessiert

* **Security**: defensive Arbeit, Schwachstellenmanagement, Hardening, dazu
  Web-Exploitation im eigenen Labor
* **Infrastruktur und Automatisierung**: Infrastructure as Code, Ansible,
  Container, Kubernetes, Observability
* **Netzwerke**: VLANs, Routing, Reverse Proxies, DNS und alles, was ich anfassen kann
* **Sauberer Code**: lieber wenige Abhängigkeiten und eine Entscheidung, die
  begründet im Repository steht, als ein Framework, das ich nicht durchschaue

## Tech Stack

**Sprachen**

![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![C](https://img.shields.io/badge/c-%2300599C.svg?style=for-the-badge&logo=c&logoColor=white)
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Bash](https://img.shields.io/badge/bash_script-%23121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white)
![PowerShell](https://img.shields.io/badge/PowerShell-%235391FE.svg?style=for-the-badge&logo=powershell&logoColor=white)
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![Markdown](https://img.shields.io/badge/markdown-%23000000.svg?style=for-the-badge&logo=markdown&logoColor=white)

**Infrastruktur und Betrieb**

![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Proxmox](https://img.shields.io/badge/Proxmox-E57000?style=for-the-badge&logo=proxmox&logoColor=white)
![OpenTofu](https://img.shields.io/badge/OpenTofu-844FBA?style=for-the-badge&logo=opentofu&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-%23EE0000.svg?style=for-the-badge&logo=ansible&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)
![WireGuard](https://img.shields.io/badge/wireguard-%2388171A.svg?style=for-the-badge&logo=wireguard&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=Cloudflare&logoColor=white)

**Web und Daten**

![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![Vite](https://img.shields.io/badge/vite-%23646CFF.svg?style=for-the-badge&logo=vite&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![Nginx](https://img.shields.io/badge/nginx-%23009639.svg?style=for-the-badge&logo=nginx&logoColor=white)
![Traefik](https://img.shields.io/badge/traefik-%2324A1C1.svg?style=for-the-badge&logo=traefikproxy&logoColor=white)

**Werkzeuge**

![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=Prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/grafana-%23F46800.svg?style=for-the-badge&logo=grafana&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![Figma](https://img.shields.io/badge/figma-%23F24E1E.svg?style=for-the-badge&logo=figma&logoColor=white)

**Nebenbei**

![Blender](https://img.shields.io/badge/blender-%23F5792A.svg?style=for-the-badge&logo=blender&logoColor=white)
![Unreal Engine](https://img.shields.io/badge/unrealengine-%23313131.svg?style=for-the-badge&logo=unrealengine&logoColor=white)
![Steam](https://img.shields.io/badge/steam-%23000000.svg?style=for-the-badge&logo=steam&logoColor=white)

## Kontakt

Am einfachsten hier über GitHub, per Issue oder Discussion in einem der Repos.

> Ich zerlege meine eigenen Systeme regelmässig, nur um zu sehen, ob ich sie beim
> zweiten Mal schneller wieder zum Laufen bringe.
