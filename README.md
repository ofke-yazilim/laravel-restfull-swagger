# Hakkında
 - **Laravel 8** Framework'ü üzerine **Php 7.4** ile kodlanmıştır.
 - Docker için **dockerfile** ve **docker-compose.yaml** dosyaları oluşturulmuştur.
 - İçerisinde Restfull servisleri barındırmaktadır.
 - Kodlanan servislerin dökümantasyonu https://swagger.io/ altyapısına entegre edilmiştir.
# Docker Kurulumu
İlk olarak Framework dizininde bulunan **.env.example** dosyasının adı **.env** olarak değiştirilmelidir.
****
 - Docker image oluşturmak için Dockerfile'ın bulunduğu dizinde aşağıdaki command çalıştırılmalıdır.<br>
`docker build -t image:1.0.1`
 - İmage oluşturulduktan sonra **Docker-compose.yaml** dosyası açılarak dosya içerisine oluşturulan versiyon yazılır.<br>
 - Aşağıdaki command çalıştırılarak. Docker ortamda proje ayağı kaldırılmış olur.<br>
  `docker-compose up -d --build`
> Yukarıdaki işlemlerden sonra 1 kaç dakika beklenmelidir. Mysql veritabanın ve Projenin ayağı kalkması biraz zaman alıyor.

####İşlem local bilgisayarda yapıldıysa projeye ait linkler aşağıdadır.####
**Servisler  ve Kullanımları :** https://localhost/api/documentation (Servsler bu adresten test edilebilir.)<br>
**Phpmyadmin:**   http://localhost:8080/ (**username:** root **password:** Z5AajEapuLZuNuv)  

 - Projenin bulunduğu container içerisine girebilmek için aşağıdaki command çalıştırılmalıdır. <br>
   `docker-compose exec web sh` 
   
 - Yukarıdaki commad ile container terminaline girilmiş olur. Proje
   kodlarının     bulunduğu yere ise`cd data/www` dosya yoluna gidilerek ulaşılır.

StackEdit stores your files in your browser, which means all your files are automatically saved locally and are accessible **offline!**

## Postman

 - Localhost üzerinde servisleri çalıştırmak için postman üzerine import edilecek olan dosya aşağıdadır.<br>
https://github.com/ofke-yazilim/laravel-restfull-swagger/blob/main/local-restfull.postman_collection.json
- okesmez.com üzerinde çalışan projeyi postman üzerinde test etmek için ise aşağıdaki dosya import edilmelidir.<br>
https://github.com/ofke-yazilim/laravel-restfull-swagger/blob/main/okesmez.com-restfull.postman_collection.json


