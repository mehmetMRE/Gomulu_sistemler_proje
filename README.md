# Gomulu_sistemler_proje Mehmet Ertan
Kısmi Otomasyonlu Dolum Sistemi
#Click for video
[<img src="https://img.freepik.com/free-vector/youtube-player-icon-with-flat-design_23-2147839964.jpg" width="50%">](https://youtu.be/GNge8DfXvAs "Now in Android: 55")











Projenin girişleri: "button": Buton girişi. Butona basıldığında 1, basılmadığında 0 değeri alır. 

Projenin çıkışları: 
"green_led": Yeşil LED çıkışı. Butona basıldığında aktif hale gelir ve yanar.
"purple_led": Mor LED çıkışı. Butondan elinizi çektiğinizde aktif hale gelir ve yanar.
"pin": Belirlediğiniz pin çıkışı. Butona basıldığında aktif hale gelir, elinizi çektiğinizde ise devre dışı kalır.
Projenin iç yapısı: 
Durumlar:
IDLE: Başlangıç durumu. Bekleme durumu. 
BUTTON_PRESSED: Butonun basıldığı durum. 
BUTTON_RELEASED: Butonun bırakıldığı durum.
Registreler: 
"state": Mevcut durumu tutan 2-bit genişliğinde bir register.
"button_state": Butonun anlık durumunu tutan bir register. Butona basıldığında 1, basılmadığında 0 değeri alır. 
"last_button_state": Önceki buton durumunu tutan bir register. Önceki durum ile karşılaştırma yapmak için kullanılır.
Davranış: 
Kombinasyonel mantık: 
Mevcut duruma ve buton durumuna dayanarak çıkışları belirler.
State geçişleri: 
IDLE durumundayken, butona basılırsa BUTTON_PRESSED durumuna geçer.
BUTTON_PRESSED durumundayken, buton bırakılırsa BUTTON_RELEASED durumuna geçer. BUTTON_RELEASED durumundayken, butona basılırsa BUTTON_PRESSED durumuna geri döner.
Çıkışların belirlenmesi: IDLE durumunda, green_led ve pin çıkışları devre dışıdır. 
BUTTON_PRESSED durumunda, green_led yanar ve pin çıkışı aktif hale gelir. 
BUTTON_RELEASED durumunda, purple_led yanar ve pin çıkışı devre dışıdır.
Bu proje, belirlediğiniz pinin aktif hale gelmesiyle birlikte yeşil LED'in yanacağı ve butondan elinizi çektiğinizde pinin devre dışı kalacağı ve mor LED'in yanacağı bir dolum sistemi davranışı sergiler.
Bu kodu FPGA Tang Nano 1k gibi bir donanım platformunda veya bir simülasyon ortamında çalıştırarak projeyi gerçekleştirebilirsiniz.
