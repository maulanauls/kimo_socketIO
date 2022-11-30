Repo KIMO Module Rusak Dijalan 
•	Untuk Repo source KIMO API hanya tinggal di update aja dari bitbucket
•	Websocket Server bisa clone dari link github  - https://github.com/maulanauls/kimo_socketIO
•	Installasi websocket server
•	Install NodeJS di server terlebih dahulu cara installasi bisa menggunakan laragon atau self dependencies dari link NodeJS tergantung dari OS yang dipakai.
•	Installasi node selesai arahkan ke directory repo kimo_socketIO example : cd /path/kimo_socketIO 
•	Lalu jalankan perintah npm install setelah selesai jalan kan perintah utk running

•	npm run start:dev -> utk mode development 
    - npm run start:prod -> utk productio 
    - npm run debug:dev -> utk debug di development

    -- pastikan package forever dari npm dan nodemon sudah diinstall di PC 
      -- klo belum jalan kan perintah ini 
      npm install forever -g
      npm install -g nodemon

* pre-release 
   siapkan domain self run utk socketio contoh iis gunakan reverse proxy arahkan ke port 3000 applikasi dari socketio server

* installasi di iis management open utk fitur websocket
  * di setting iis allow websocket 
  * utk webconfig samakan yang sudah ada di vps 
  * ikuti config vps

---- flutter app

arahkan sockeio client URL di initstate --> 
di pages/operasional/pelaporan/rusak_dijalan/chat_rdj.dart

socket = await io('https://kimosocketio-dev.kamanggala.web.id/', --> ganti url production
        OptionBuilder()
            .setTransports(['websocket']) // for Flutter or Dart VM
            .disableAutoConnect()  // disable auto-connection
            .build()
    );

