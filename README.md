نحنا شغالين علي مسابقه teknofest قسم الdoner kanat دايرين نعمل الريبورت المطلوب تسليمه (ارفقت الtemplete انا ) 
انا شغال في قسم الsoftware حاليا اخترنا الحاجات دي :
النظام PX4 ,المحطه الارضيه Qground station ,نموذج الذكاء الاصطناعي للكاميرا YOLO , ح نشتغل بي ROS و MAVLink غالبا 
وحاليا مهمتي اني اعمل محاكاه ناجحه للدرون ثبتت Ubuntu 22.04.5 LTS (Jammy Jellyfish) ومعاه gazebo harmonic  

Gazebo simülasyon
fiziksel montajdan önce gazebo üzerinden SITL (Software In The Loop) simülasyonu yapıyoruz; burada ağırlık, ağırlık merkezi, atalet ve diğer mekanik özelliklerin yanı sıra motor özellikleri ve diğer detaylar gibi elektriksel özellikleri de içeren tüm dron verilerini giriyoruz. Simülatör üzerinden fiziksel dünya ayarlarının doğru olduğunu doğruluyoruz; ayrıca rüzgar, nem ve diğer faktörleri ekleyerek dronun performansını gözlemliyor ve buna göre gerekli düzenlemeleri yapıyoruz. Ayrıca, gelecek planlarımızdan biri de İstanbul gibi belirli bir konumun verilerini Google Haritalar'dan çıkarıp simülatöre aktararak gerçekle %100 uyumlu bir simülasyon elde etmektir.


Arama Algoritması: Paralel Tarama
Paralel tarama algoritmasına dayanacağız. Arama alanı, yarışma şartlarına göre 100×30 boyutlarında bir dikdörtgen olarak belirlenecektir. Drone, köşeden başlayarak uzun kenar boyunca ilerleyecektir. Karşı kenara ulaştığında 180 derece dönerek aramaya devam edecek ve tekrar ilk kenara ulaşana kadar bu şekilde ilerleyecektir. Drone’un şekli kaçırmaması için görüntü alanında yaklaşık %10–20 örtüşme olacaktır. Eğer drone şekli görürse, arama durdurma komutu gönderilecek ve bırakma algoritmasına geçilecektir.
