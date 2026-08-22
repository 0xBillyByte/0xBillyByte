## Hallo, ich bin Billynary

Lernender Informatiker aus der Schweiz. Mich interessieren zwei Dinge: eine
Infrastruktur sicher aufbauen und sie danach selbst angreifen.

Der Rest ergibt sich daraus. Ich baue etwas, nehme es auseinander und baue es
beim nächsten Mal robuster.

## Schwerpunkte

**Red Team.** Web-Exploitation, Angriffe auf Geschäftslogik, Privilege
Escalation, Active Directory. Geübt wird im eigenen Labor und auf Plattformen wie
Hack The Box, nicht auf fremden Systemen.

**Sichere Infrastruktur.** Segmentierung, interne PKI, zentrale Authentisierung,
Least Privilege und Hardening. Alles als Code, damit es nachvollziehbar und
wiederherstellbar bleibt.

## Projekte

**[Monkstore](https://github.com/Billynary/Monkstore)**
Absichtlich verwundbarer Marktplatz als eigenes Angriffslabor. Der Kern ist
sauber gebaut, damit die Lücken realistisch sind. Die interessanteren stecken in
der Geschäftslogik: Preismanipulation, eine Race Condition beim Kauf, ein Webhook
ohne Signaturprüfung. Fastify, TypeScript.

**[Vulnerability-Scanner](https://github.com/Billynary/Vulnerability-Scanner)**
Eigenes Schwachstellenmanagement statt Nessus, Nucleus und Aikido. Vier Scanner
schreiben in dieselbe Findings-Tabelle, priorisiert wird nach CVSS, EPSS und CISA
KEV. Python, FastAPI, PostgreSQL, React.

**[OSINT](https://github.com/Billynary/OSINT)**
Fünf Module für die Aufklärungsphase: Namenssuche über 16 offene Quellen,
Username-Check, Domain- und Infrastrukturrecherche, E-Mail-Analyse, EXIF.
Ausschliesslich offizielle APIs, kein Scraping. React, Express.

**[cit](https://github.com/Billynary/cit)**
Git-Werkzeug fürs Terminal, das GitLens-Funktionen mit der GitHub-Anbindung
verbindet. Eigener Lane-Algorithmus für den Commit-Graphen. TypeScript, Ink.

**[Scraper](https://github.com/Billynary/Scraper)**
Watcher für Wohnungen, Flüge und Tickets. Offizielle APIs vor HTML-Scraping,
robots.txt wird durchgesetzt. Python.

**[EatAI](https://github.com/Billynary/EatAI)**
Lebensmittelverwaltung mit Ablaufwarnungen. Bewusst ohne Frontend-Framework.

Nicht öffentlich: die Infrastructure as Code für mein Homelab und eine selbst
gehostete Plattform für Ziele, Noten und Finanzen.

## Homelab

Angriffsfläche und Übungsziel zugleich. Ein Proxmox-Host, rund 20 Systeme in vier
VLANs, vollständig als Code: OpenTofu provisioniert, Ansible konfiguriert.

Zweistufige interne PKI mit step-ca, autoritatives DNS mit BIND9 und Split-DNS,
Zitadel als zentraler OIDC-Provider, ein selbst gehostetes Mesh-VPN mit
Headscale, ein k3s-Node und eine isolierte Datenbank je Dienst statt einer
zentralen Instanz.

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

> Ich zerlege meine eigenen Systeme regelmässig, nur um zu sehen, ob ich sie beim
> zweiten Mal schneller wieder zum Laufen bringe.
