# Liman-Depo-Eklentisi
# Liman MYS Depo Eklentisi İle Yerel Depo Oluşturma 
## Depo Eklentisi Kurulumu

 Liman MYS üzerinde bulunan Depo eklentisi, uzaktaki depoları yerele çekmeye ve sunucunuzdaki depoları kullanarak uzak sunucu bağımlılığını koparmaya yarar.

 >  Liman MYS kurulumu için -> https://rehber.liman.dev/liman-kurulum/ sayfasına göz atabilirsiniz.
 
 Depo eklentisi kurulumu için ilk olarak Eklenti Mağazası'na gitmelisiniz. Sol alt köşede bulunan Eklenti Mağazası butonuna tıklayarak mağazaya gidebilirsiniz.Mağazada bulunan eklentilerden Depo eklentisini bularak Satın Al diyoruz (Depo eklentisi ücretsiz bir eklentidir :)).
 
![1 1](https://https://github.com/busrakose/Liman-Depo-Eklentisi/blob/main/images/1.1.JPG?raw=true)


Eklenti satın alma işlemi tamamlandıktan sonra Depo eklentisini kuracağımız sunucumuzu sol köşede Suncular başlığı altında bulup tıkladıktan sonra Sunucu Detayları'na tıklıyoruz.
Açılan pencerede Eklentiler tabine tıklayıp + butonuna basıyoruz.

![2 1](https://https://github.com/busrakose/Liman-Depo-Eklentisi/blob/main/images/2.1.JPG)
 
 
Karşımıza Liman MYS üzerinde yüklü olan eklentiler çıkıyor. Biz Depo eklentisine tıklayıp Ekle diyerek sunucumuza eklentimizi ekleme işlemini tamamlıyoruz.

![3 1](https://https://github.com/busrakose/Liman-Depo-Eklentisi/blob/main/images/3.1.JPG)





Sunucumuza tıkladığımızda altında yüklemiş olduğumuz eklentimizi görebiliyoruz. Depo eklentisine tıkladığımızda kurulması gereken paketler olduğunu görüyoruz. Paketleri Yükle diyerek işlemi başlatıyoruz.

![4 1](https://https://github.com/busrakose/Liman-Depo-Eklentisi/blob/main/images/4.1.JPG)

Paket yükleme işlemi tamamlandıktan sonra Depo eklentimizi kullanmaya başlayabiliriz..


## Depo Eklentisi İle Yerel Depo Oluşturma

Depo eklentisi kurulumu tamamlandıktan sonra açılan pencerede Yerel Depo tabine tıklayıp Yerel Depo Ekle diyerek yeni depomuzu oluşturalım.

![5 1](https://https://github.com/busrakose/Liman-Depo-Eklentisi/blob/main/images/5.1.JPG)

Açılan pencerede Yerel Depo özelliklerini doldurmamız gerekiyor.


![6](https://https://github.com/busrakose/Liman-Depo-Eklentisi/blob/main/images/6.JPG)

> Örnek:![6 1](https://https://github.com/busrakose/Liman-Depo-Eklentisi/blob/main/images/6.1.JPG)




Bütün boşlukları doldurduktan sonra Ekle diyerek depomuzu ekliyoruz.

![6 2](https://https://github.com/busrakose/Liman-Depo-Eklentisi/blob/main/images/6.2.JPG)


Eklediğimiz depoyu artık depoların bulunduğu tabloda görebiliyoruz. 
Adres başlığı altında bulunan link bizim yerel depo adresimiz. Linkin üzerine tıklıyoruz.

![7 1](https://https://github.com/busrakose/Liman-Depo-Eklentisi/blob/main/images/7.1.JPG)

Karşımıza depoda bulunan Yerel Paketler penceresi çıkıyor. 
>Source List : Depomuzun debian paketini yüklemek için kullanacağımız uzantı.
>GPG Anahtarı: Depoyu istemciye eklemek için gerekli olan anahtar.

GPG Anahtarını Dışa Aktar diyerek anahtara ulaşabiliriz.
![8 1](https://https://github.com/busrakose/Liman-Depo-Eklentisi/blob/main/images/8.1.JPG)

![9 1](https://https://github.com/busrakose/Liman-Depo-Eklentisi/blob/main/images/9.1.JPG)

Depo Adresi butonuna tıkladığımızda depomuzun içindeki verileri görebiliriz.

![10](https://https://github.com/busrakose/Liman-Depo-Eklentisi/blob/main/images/10.JPG)

Yerel depomuz ve istemciye kurmak için gerekli tüm bilgilerimiz artık hazır.

## Yerel Depoya Filezilla İle Paket Yükleme

Oluşturduğumuz Yerel Depo içerisine Filezilla(ftp/sftp yapan başka uygulama da olur) ile paket yükleyebiliriz.

Filezilla uygulamamızı açıp Sunucu, Kullanıcı adı, Parola, Kapı numarası boşluklarını dolduruyoruz.
>Sunucu sftp://sunucu-ip-adresi
>Kullanıcı adı: Sunucuda kullanılan kullanıcı adı.
>Parola: Sunucuda kullanılan kullanıcı parolası.
>Kapı numarası: Bağlanılacak port numarası.



![11](https://https://github.com/busrakose/Liman-Depo-Eklentisi/blob/main/images/11.JPG)

Bağlantı yapıldıktan sonra aşağıdaki dosyalar kısmından yüklemek istediğimiz paketi seçip yükleme işlemini tamamlıyoruz.
 
>Eğer yükleme yaparken permission denided hatası alırsanız sunucu terminalinden kullanıcı izinlerini düzenlemeniz gerekiyor. Bunun için; 
chmod -R 777 /depodaki-dosya-adi/depodaki-dosya-dizini 
komutunu kullanabilirsiniz (depodaki-dosya-adi ve depodaki-dosya-dizini kısımlarını kendi deponuzdaki dosya adı ve dizinine göre değiştirmeyi unutmayın!!)


## İstemciye Yerel Depoyu Kurma

İlk olarak istemcinizde ssh paketinin kurulu olması gerekiyor.
>Eğer ssh paketi kurulu değilse;
sudo apt install ssh 
diyerek ssh paketini indirmelisiniz.

Yerel depomuzu istemcimize eklemek için Liman MYS üzerinden edindiğimiz Source List ve GPG Anahtarı bilgilerine ihtiyacımız var.

İlk olarak GPG Anahtarını terminale yazıp çalıştırıyoruz.

>Not: İstemci ile sunucunuzun saatleri aynı değilse GPG anahtarı komutunu çalıştırdığınızda böyle bir hatayla karşılaşırsınız.
![deb1](https://https://github.com/busrakose/Liman-Depo-Eklentisi/blob/main/images/deb.JPG)
Eğer istemciniz Pardus bir istemci ise 
sudo nano /etc/adjtime
komutunu çalıştırıp  açılan editör içersindeki UTC ifadesini LOCAL olarak değiştirip reboot diyerek yeniden başlatarak bu sorunu çözebilirsiniz.

Depomuzu istemcimize eklemek için
sudo nano /etc/apt/sources.list 
komutunu çalışarak depoların bulunduğu dizine ulaşıyoruz.
![12](https://https://github.com/busrakose/Liman-Depo-Eklentisi/blob/main/images/12.JPG)

Açılan sayfaya Liman MYS üzerinden aldığımız Source List'i ekleyerek Ctrl+S ve Ctrl+X diyerek pencereyi kapatıyoruz.
![13](https://https://github.com/busrakose/Liman-Depo-Eklentisi/blob/main/images/13.JPG)

Depomuzu istemcimize kurduk. İçerisindeki paketlere erişebilmek için sistemi update ve upgrade etmemiz gerekiyor.
> sudo apt update
 update işlemi tamamlandıktan sonra
> sudo apt upgrade 

işlemlerimizi tamamlıyoruz.
## İstemciye Yerel Depodaki Paketi Kurma

Yerel depo içerisine yüklediğimiz paketi kurmak için 
>sudo apt install paket-adi
(paket-adi kısmına depoya yüklediğiiz paketin adını yazmalısınız!!)

diyerek paket kurulumunu tamamlıyoruz.
