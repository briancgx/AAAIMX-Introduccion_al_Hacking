# Introduccion al Hacking

## Objetivos
Este curso tiene como objetivo proporcionar los fundamentos esenciales para iniciarse en el mundo del hacking. Además, busca fomentar el aprendizaje continuo y autodidacta en este vasto y dinámico campo.

## Temas
- Comandos básicos de Linux.
- Direcciones IPv4, IPv6 y MAC.
- Modelo OSI.
- TCP y UDP (Protocolos más conocidos).
- OSINT (TheHarvester).
- Google Hacking.
- Ingeniería social (Phishing).
- Reconocimiento con Nmap.
- Descubrimiento de hosts en una red local.
- Fuzzing y Fuerza Bruta.
- Contraseñas Default y Cracking (Jhon The Ripper, SSH y FTP).
- Básicos de BurpSuite y hacking web (XSS - Cross Site Scripting).
- Final: Reconocimiento y explotación de una máquina vulnerable.

## Requisitos fundamentales
- Alguna distribución de linux instalada (Kali linux, Parrot u otra de preferencia enfocada al hacking)
Nota: En el caso de no contar con Kali instalado, se adjunta un video para su instalación.
[Instalación de Kali](https://www.tiktok.com/@br14ncgx/video/7280082143114497285?is_from_webapp=1&sender_device=pc&web_id=7370770948541564422)

## Herramientas usadas en el curso
1. TheHarvester
Herramienta para OSINT, utilizada para recopilar correos electrónicos, subdominios, direcciones IP y más.
**Instalación**
```bash
sudo apt-get install theharvester
```
Uso:
```bash
theharvester -d example.com -b google
```

2. Nmap
Herramienta para escanear redes y descubrir hosts y servicios.
Instalación:
```bash
sudo apt-get install nmap
```
Escaneo básico:
```bash
nmap -sP 192.168.1.0/24
```

3. Gobuster
Herramienta de fuerza bruta para encontrar directorios y archivos ocultos en servidores web.
Instalación:
```bash
sudo apt-get install gobuster
```
Uso:
```bash
gobuster dir -u http://example.com -w /path/to/wordlist
```

4. Hydra
Herramienta para realizar ataques de fuerza bruta en servicios como SSH o FTP.
Instalación:
```bash
sudo apt-get install hydra
```
Uso:
```bash
hydra -l usuario -P /ruta/a/lista_de_contraseñas ftp://192.168.1.100
```

5. John the Ripper
Herramienta de cracking de contraseñas.
Instalación:
```bash
sudo apt-get install john
```
Uso:
```bash
john /ruta/a/archivo_hashes
```

6. SecLists
Una colección de listas de palabras para usar en fuerza bruta, diccionarios de nombres de usuario, contraseñas, directorios, subdominios y más.
```bash
git clone https://github.com/danielmiessler/SecLists
```
Uso: Las listas se almacenarán en /usr/share/seclists/. Puedes usarlas en cualquier ataque de fuerza bruta o reconocimiento:
```bash
gobuster dir -u http://example.com -w /usr/share/seclists/Discovery/Web-Content/common.txt
```

NOTA: Se usarán más herramientas además de las que hay aquí, pero ya vienen instaladas con kali, asi que no hay problema.
