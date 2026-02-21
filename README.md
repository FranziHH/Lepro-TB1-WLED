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

Um zum Original zurückkehren zu können, habe ich mit dem ESP-Tool die [originale Firmware](./docs/firmware/ESP32-S3-Mini-1_Lepro-TB1.bin) gesichert.


### Firmware/Flashen

Ich bin dabei, die Beschreibung weiter zu Verbessern.
Images Full und Update compiliere ich nach verfügbaren WLED Updates neu.

Die Images können hier heruntergeladen werden: [Firmware](/docs/firmware)

Um das Flashen zu erleichtern habe ich einen Firmware Flasher bereitgestellt:   
[WLED Flash Tool - für Lepro TB1](https://franzihh.github.io/Lepro-TB1-WLED/)


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
