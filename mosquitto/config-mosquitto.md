# Tutorial Install dan Konfigurasi Mosquitto
## Apa itu Mosquitto
Mosquitto adalah MQTT broker (server pengelola pesan) yang ringan dan digunakan untuk mengirim serta menerima pesan antar perangkat menggunakan protokol MQTT.

## Set Up
- Download aplikasi mosquitto di [website resmi](https://mosquitto.org/download/)
  ![](https://github.com/nailonk/tutorial-dev-setup/blob/main/asset/install-mosq.png)
- Jalankan file mosquitto, klik **Next** pada setiap langkah
- Selesaikan instalasi dan klik **Finish**

## Konfigurasi
- Buka file mosquitto.conf di visual code
- Lokasi file ```C:\Program Files\mosquitto\mosquitto.conf```
  ![](https://github.com/nailonk/tutorial-dev-setup/blob/main/asset/conf-mosq.png)
- Tambahkan script seperti berikut dan **Update now** di kanan bawah
  ![](https://github.com/nailonk/tutorial-dev-setup/blob/main/asset/mosq1.png)
- Cari **Edit the system environment variables**
  ![](https://github.com/nailonk/tutorial-dev-setup/blob/main/asset/mosq4.png)
- Klik environment variabels, kemudian pilih **Path** di **System Variables** dan klik Edit
  ![](https://github.com/nailonk/tutorial-dev-setup/blob/main/asset/mosqt.png)
- Tambahkan folder mosquitto di path dengan memilih di Browse
  ![](https://github.com/nailonk/tutorial-dev-setup/blob/main/asset/mosq6.png)
- Buka Windows PowerShell dengan perintah dibawah untuk restart konfigurasi terbaru
  ```
  net start mosquitto
  ```
  ![](https://github.com/nailonk/tutorial-dev-setup/blob/main/asset/mosq3.png)

- Konfigurasi selesai :tada:  , letsgoo kita Testing MQTT Publish-Subscribe :rocket:
  - Perintah untuk subscriber
    ```
    mosquitto_sub -h localhost -t smk/test
    ```
  - Perintah untuk publisher
    ```
    mosquitto_pub -h localhost -t smk/test -m "uji MQTT"
    ```
  ![](https://github.com/nailonk/tutorial-dev-setup/blob/main/asset/mosq7.png)
  
  
