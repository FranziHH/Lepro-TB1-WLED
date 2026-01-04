# Lepro TB1 Umbau auf WLED 

<div style="display: flex; align-items: center;">
  <img src="/images/Lepro_TB1.jpg" alt="Lepro AI Smart Tischlampe TB1" height="92" style="margin-right: 20px;">
  <a href="https://www.lepro.de/ai-smart-tischlampe-tb1-eu.html"  target="_blank">
    Lepro AI Smart Tischlampe TB1
  </a>
</div>

## Beschreibung

Ausgehend von der Idee, diese Lampe mit WLED zu betreiben, habe ich die Lampe demontiert und erforscht.

Es ist recht einfach möglich, den vorhandenen ESP32 S3 Mini-1 neu zu flashen.

Um zum Original zurückkehren zu können, habe ich mit dem ESP-Tool die [originale Firmware](/firmware/ESP32-S3-Mini-1_Lepro-TB1.7z) gesichert.

### Update Firmware/Flashen

Ich habe eine [WLED Firmware Lepro TB1](/firmware/WLED_0.16.0-alpha_ESP32-S3_4M_Mini_Lepro_TB1_full.7z) compiliert, die alle notwendigem Einstellungen voreingestellt hat und die sich einfach flashen lässt:  
- das Archiv entpacken
- [WLED web installer von ESP Home aufrufen](https://web.esphome.io/) im Chrome Browser!
- Install aufrufen
- die entpackte Datei ``WLED_0.16.0-alpha_ESP32-S3_4M_Mini_Lepro_TB1_full.bin`` auswählen und installieren lassen
- Anschließend über den Access Point die WiFi Zugangsdaten angeben


### Das Flashen ist nicht ganz einfach

Der [WLED web installer](https://install.wled.me) funktioniert <b>NICHT!</b>

Auf dem ESP32 S3 muss ein anderer Bootloader installiert werden, dies funktioniert zur Zeit nur mit dem [inoffiziellen Installer](https://wled-install.github.io/)

Hier muss ``ESP32-S3 (4MB Flash, xxx)`` ausgewählt werden.
Damit wurde bei mir der korrekte Bootloader installiert.

Nach dem Flashen muss der ESP32 neu gestartet werden (Spannung abziehen und wieder anstecken). Danach kann man beim Installer auf weiter klicken, um die EInrichtung des WLANs abzuschließen. Man kann natürlich auch den AccessPoint aufrufen und dort die Einstellungen vornehmen.

### Settings

Ich habe mühevoll die notwendigen GPIOs heraus gefunden.
Auf der Platine sind 2 MOSFETs parallel geschaltet für die Spannungsversorgung der LEDs.

die notwendigen Einstellungen
LED Data Pin: 11
LED Count: 196

Button 0 GPIO: 13 Pushbutton

Relay GPIO: 38 Invert x (selected)

Damit sollte die Lampe funktionieren


### Audio Reactive

Pin I2S SD: 39  
Pin I2S WS: 2
Pin I2S SCK: 1

## Bilder

Im Moment ohne Beschreibung 

<img src="/images/IMG_20251215_192620.jpg" height="400px" title=""> 

<img src="/images/IMG_20251215_192632.jpg" height="400px" title=""> 

<img src="/images/IMG_20251223_115256.jpg" height="400px" title=""> 

<img src="/images/IMG_20251223_115316.jpg" height="400px" title=""> 

<img src="/images/IMG_20251225_183959.jpg" height="400px" title=""> 

<img src="/images/IMG_20251226_111450.jpg" height="400px" title=""> 

<img src="/images/IMG_20251226_131925.jpg" height="400px" title=""> 

<img src="/images/IMG_20251226_131925_GPIOs.jpg" height="400px" title=""> 

<img src="/images/IMG_20251226_132002.jpg" height="400px" title=""> 

<img src="/images/IMG_20251226_132807.jpg" height="400px" title=""> 

<img src="/images/IMG_20251226_132834.jpg" height="400px" title=""> 

<img src="/images/IMG_20251226_133017.jpg" height="400px" title=""> 

<img src="/images/IMG_20251226_133222.jpg" height="400px" title=""> 
