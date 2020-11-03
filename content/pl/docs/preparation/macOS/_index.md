---
title: MacOS
linkTitle: MacOS
weight: 1
description: >
    Opis przygotowania nośnika instalacyjnego z MacOS.
---


# Pobieranie instalatora z gibMacOS

* ####  *Narzędzie to pozwoli Ci pobrać kopię MacOS w wersji od 10.13.x do najnowszej* 

Jeżeli jesteś na maszynie spełniającej wymagania systemu który chcesz pobrać, możesz użyć App store do pobrania instalatora.

Pobierz narzędzie [gibMacOS](https://github.com/corpnewt/gibMacOS), następnie rozpakuj, przejdź do folderu i odpal `gibMacOS.command`:

![alt](gibmacos.png)

Pojawią się wersje MacOS z katalogu publicznego, jeśli chcesz pobrać wersję Beta zmień katalog : `C.Change Catalog`

* Kopia instalatora bedzie pobrana do katalogu `gibMacOS-master/macOS Downloads`
* Aby przekonwertować pobrane pliki do `.app` i przenieść instalator do folderu /Applications uruchom `InstallESDDmg.pkg`

# Tworzenie nośnika instalacyjnego

### Wymagania 

Do stworzenia nośnika instalacyjnego z systemem MacOS Catalina i wyżej potrzebny jest pendrive lub dysk zewnętrzny o pojemności min. 16GB 

### Formatowanie Dysku

Uruchom `Narzędzia Dyskowe` 

* Kliknij Widok>Pokaż wszyskie urządzenia.
* Wybierz swój dysk docelowy i sformatuj go z następującymi ustawieniami:
![alt](diskutility.png)

### Kopiowanie instalatora
*Metoda przy użyciu narzędzia `createinstallmedia`*
 
 * Uruchom `Terminal` i wpisz poniższe polecenia w zależności od systemu który instalujesz :
 
### Catalina
`sudo /Applications/Install\ macOS\ Catalina.app/Contents/Resources/createinstallmedia --volume /Volumes/USB`

### Mojave 
`sudo /Applications/Install\ macOS\ Mojave.app/Contents/Resources/createinstallmedia --volume /Volumes/USB`

### High Sierra
`sudo /Applications/Install\ macOS\ High\ Sierra.app/Contents/Resources/createinstallmedia --volume /Volumes/USB`

Gratulacje, udało Ci się utworzyć nośnik instalacyjny, możesz przejść dalej do [Konfiguracja Bootloadera](/hackintoshpolska-docs/content/pl/docs/bootloader/_index.md)
