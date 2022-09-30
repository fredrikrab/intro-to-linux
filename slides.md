---
title: Intro to Linux for Fuel Fighter
date: 2022-09-13
author: Fredrik Randsborg Bølstad
extensions:
    - terminal
    - image_ueberzug
    - render
styles:
  style: monokai
  margin:
    top: 1
    bottom: 0
  padding:
    top: 1
    bottom: 0
---

# Intro til Linux


```bash
 ______________________
< Fuel Fighter FTW! >
 ----------------------
   \
    \
        .--.
       |o_o |
       |:_/ |
      //   \ \
     (|     | )
    /'\_   _/`\
    \___)=(___/

.......................
```

---

# Agenda

## 1. Hva er Linux?

## 2. Filbehandling

## 3. Terminal

## 4. Installasjon

---

# 1. Hva er Linux?
 

 
![15](images/linux_stack_basic.png)

---

# 1. Hva er Linux?
 

 
![20](images/linux_stack.png)
 

![15](images/gnu_linux.jpeg)

---

# 1. Hva er Linux?
 

 
![20](images/linux_stack_relevant.png)
 

![15](images/gnu_linux.jpeg)

---

# 1. Hva er Linux?
## Fri programvare

> “Free software” means software that respects users' freedom and community. Roughly, it means that the users have the freedom to run, copy, distribute, study, change and improve the software.

> Thus, “free software” is a matter of liberty, not price. *To understand the concept, you should think of “free” as in “free speech,” not as in “free beer.”*

\- https://www.gnu.org/philosophy/free-sw.html

## Hvorfor Linux?

- Stabilit
- Høy ytelse
- Mange tilpasningsmuligheter
- Stort og åpent kildekode-miljø
- Innbygd støtte for mange utviklingsverktøy

---

# 1. Hva er Linux?

## Hvem bruker Linux?
 

 
![30](images/iss_linux_switch.png)

International Space Station

---

# 1. Hva er Linux?

## Hvem bruker Linux?
 

 
![30](images/top500_os_family.png)

Alle de 500 raskeste datamaskinene i verden

Kilde: https://top500.org/statistics/list/

---

# 1. Hva er Linux?

## Hvem bruker Linux?
 

 
![30](images/android_stack_480.png)


Kilde: https://source.android.com/

---

# 1. Hva er Linux?

## Hvem bruker Linux?
 

 
![30](images/agl_members.png)

Kilde: https://www.automotivelinux.org/about/members/

---


# 1. Hva er Linux?

## Hvem bruker Linux?
 

 
![30](images/microsoft_host.png)

Kilde: https://sitereport.netcraft.com/?url=http://microsoft.com

---

# 2. Filbehandling

## Mappestruktur
 

 
![30](images/directory_hierarchy.png)

---

# 2. Filbehandling

## Mappestruktur
 

 
![25](images/home-folder.png)

---

# 2. Filbehandling

## Mappestruktur
 

 
![30](images/home-folder-contents.png)

### `tar.gz`
- Komprimerte filer lagres typisk som `arkiv.tar.gz`
- Disse må pakkes ut på samme måte som .zip-filer

---

# 3. Terminal
 

 
![20](images/cmatrix.png)

## Hvorfor Terminal?

1. Kan gjøre "alt"
2. Fleksibelt
3. Krever få ressurser

## Resultat
- Mye foregår i Terminal
- Scripting av vanlige oppgaver
- Lett å følge guider

---

# 3. Terminal

## `sudo` - > 'super user do' 
 

 
![10](images/sudo_sandwhich.png)


Administrator kalles **root** eller **super user**.

---

# 3. Terminal

## `apt` -> 'Advanced Package Tool'

Verktøy for administrasjon av programvare på Debian-baserte distroer (som Ubuntu).

Installasjon, fjerning og oppdatering av det meste.

Programvare hentes fra "repositories".

```shell-session
$ sudo apt install ros-noetic-desktop-full

```

```terminal11
bash -il
```

### Vanlige `apt`-kommandoer
- `apt install`
- `apt remove`
- `apt update`
- `apt upgrade`

Krever `sudo` foran.

### Hva med installasjon fra fil eller kildekode?
- deb
- snap
- AppImage
- install.sh


---

# 3. Terminal

## Navigasjon

| Kommando | Beskrivelse             |       | Annet  |                                  |
| :------- | :---------------------- | :---: | :----: | :------------------------------- |
| `pwd`    | print working directory |  \|   |   .    | refererer til `pwd`              |
| `ls`     | list                    |  \|   |   ..   | refererer til ett nivå opp       |
| `cd`     | change directory        |  \|   |   ~    | refererer til `/home/$(whoami)/` |
| `mv`     | move                    |  \|   | `nano` | teksteditor                      |
| `rm`     | remove                  |  \|   | `cat`  | dump innhold i fil               |

```terminal25
bash -il
```

-> Tips: Søk etter cheatsheets

---

# 3. Terminal

## Diverse nyttig

### Piltast, TAB og `!!`

- Pil opp og ned blar i historikk
- TAB = autocomplete (dobbelklikk for å se muligheter)
- `!!` er forrige kommando (f.eks. `sudo !!`)

### Kjøre scripts
1. Gjør executable: `chmod +x <fil>`
2. Kall script: `/sti/til/script.sh` (ofte bare `./script.sh`)

### `$PATH` 
- Kjørbare filer kan kalles uten sti dersom de ligger i `$PATH`
- `which <kommando>` gir full sti til programmet

### Dokumentasjon
- `<kommando> --help`
- `man <kommando>`

### Tastatursnarveier

| Funksjon            | Snarvei          |
| :------------------ | :--------------- |
| Avbryt/lukk process | Ctrl + C         |
| Kopier              | Ctrl + Shift + C |
| Lim inn             | Ctrl + Shift + V |
| Åpne Terminal       | Ctrl + Alt + T   |
| Lukke Terminal      | Ctrl + D         |

---

# 4. Installasjon

## Dual boot

- Installer Ubuntu ved siden av Windows eller macOS.
- Velg operativsystem ved oppstart.

## Virtualisert maskin

- Installer programvare som lager en virtuell maskin.
- Installer Ubuntu på denne virtuelle maskinen.

--


Dual boot er generelt å foretrekke men ikke alltid mulig.

---

# 4. Installasjon

## Forberedelser

- Backup
- Deaktiver kryptering
- Partisjoner harddisk

## Potensielle problemer

- Maskinvare virker ikke
  - Nettverkskort
  - Grafikkort
- Maskinen starter ikke
  - Korrupte instillinger for oppstart
  - Sannsynligvis er det meste likevel i orden

---

# 4. Installasjon

## Kjapp gjennomgang

### Deaktiver kryptering

  
![30](images/installation/bitlocker-deactivate.png)

---

# 4. Installasjon

## Kjapp gjennomgang

### Deaktiver kryptering

  
![30](images/installation/bitlocker.png)

---

# 4. Installasjon

## Kjapp gjennomgang

### Partisjonering av harddisk

  
![30](images/installation/partisjonering1.png)

---

# 4. Installasjon

## Kjapp gjennomgang

### Partisjonering av harddisk

  
![30](images/installation/partisjonering2.png)

---

# 4. Installasjon

## Kjapp gjennomgang

### Lag bootable USB

  
![30](images/installation/balena-etcher.png)


Link: https://www.balena.io/etcher/

---

# 4. Installasjon

## Kjapp gjennomgang

### Start maskinen fra USB-penn

  
![30](images/installation/usb-boot.png)


---

# 4. Installasjon

## Kjapp gjennomgang

### Prøv Ubuntu

  
![30](images/installation/live-boot-0-welcome.png)

---

# 4. Installasjon

## Kjapp gjennomgang

### Prøv Ubuntu

  
![30](images/installation/live-boot-1.png)

---

# 4. Installasjon

## Kjapp gjennomgang

### Prøv Ubuntu

  
![30](images/installation/live-boot-2-wifi.png)

---

# 4. Installasjon

## Kjapp gjennomgang

### Prøv Ubuntu

  
![30](images/installation/live-boot-3-wifi.png)

---

# 4. Installasjon

## Kjapp gjennomgang

### Installer Ubuntu

  
![30](images/installation/live-boot-4-install.png)

---

# 4. Installasjon

## Kjapp gjennomgang

### Installer Ubuntu

  
![30](images/installation/live-boot-5-install.png)

---

# 4. Installasjon

## Kjapp gjennomgang

### Installer Ubuntu

  
![30](images/installation/live-boot-6-install.png)

---

# 4. Installasjon

## Kjapp gjennomgang

### Installer Ubuntu

  
![30](images/installation/live-boot-7-install.png)

---

# 4. Installasjon

## Kjapp gjennomgang

### Installer Ubuntu

  
![30](images/installation/live-boot-8-install.png)

---

# 4. Installasjon

## Kjapp gjennomgang

### Installer Ubuntu

  
![30](images/installation/live-boot-9-install.png)

---

# 4. Installasjon

## Kjapp gjennomgang

### Installer Ubuntu

  
![30](images/installation/live-boot-10-install.png)

---

# 4. Installasjon

## Kjapp gjennomgang

### Installer Ubuntu

  
![30](images/installation/live-boot-11-install.png)

---

# 4. Installasjon

## Kjapp gjennomgang

### Installer Ubuntu

  
![10](images/installation/live-boot-12-install.png)

---

# 4. Installasjon

## Oppsummering

1. Backup
2. Krymp og partisjoner harddisken
3. Deaktiver kryptering
4. Last ned Ubuntu og lag bootable USB
5. Start maskinen fra USB
6. Prøv Ubuntu - sjekk WiFi
7. Følg installasjonsveiviseren
   - "Install third-party software" 
   - "Install Ubuntu alongside Windows Boot Manager"
8. Restart
   - Bekreft at både Windows/macOS og Ubuntu starter

```
 ___________
< Spørsmål? >
 -----------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
             --------------
```

### Problemer
- Spør meg
- Google / DuckDuckGo
- Hjelp hverandre
- Orakeltjenesten