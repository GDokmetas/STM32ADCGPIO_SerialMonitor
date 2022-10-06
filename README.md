# STM32ADCGPIO_SerialMonitor
STM32 ile ADC ve GPIO okumalarını seri port üzerinden izleyin, istediğiniz dil ile analog dünyaya açılın. 

STM32F103C8T6 Bluepill uyumludur. 
Karta yüklemek için STM32CubeProgrammer'den .elf dosyasını yükleyin.
Programı incelemek için main.c dosyasına bakabilirsiniz. 

Komut Listesi 
'1' -> Okuma Talebi (Tüm okumalar)
'A' -> PA10 HIGH
'a' -> PA10 LOW
'B' -> PA9 HIGH
'b' -> PA9 LOW
'C' -> PA8 HIGH
'c' -> PA8 LOW
'D' -> PB15 HIGH
'd' -> PB15 LOW
'E' -> PB14 HIGH
'e' -> PB14 LOW
'F' -> PB13 HIGH
'f' -> PB13 LOW
'G' -> PB12 HIGH
'g' -> PB12 LOW

Gelen veri çerçevesi 

"%04i%04i%04i%04i%04i%04i%04i%04i%04i %i%i%i%i%i%i%i%i %i%i%i%i%i%i%i\n"

A0+A1+A2+A3+A4+A5+A6+A7+A8 -boşluk- PB1+PB2+PB10+PB11+PB7+PB6+PB5+PB4 -boşluk- PA10+PA9+PA8+PB15+PB14+PB13+PB12 + \n

A0-A8 : PA0-PA8 Arası analog okumaları ifade eder, her bir okuma 0000-4096 arası sonuç verir. Her zaman 4 karakterdir.
PB1-PB4 : Dijital Giriş Ayaklarını Gösterir. PB1, PB2, PB10, PB11, PB7, PB6, PB5, PB4 giriş ayaklarıdır. 
PA10-PB12: Dijitaç çıkış ayaklarının durumunu gösterir. PA10, PA9, PA8, PB15, PB14, PB13, PB12 çıkış ayaklarıdır.
Her veri paketinin sonunda \n karakteri gönderilmektedir. 


