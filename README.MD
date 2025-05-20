# Tutorial 10 - Timer

## 1.2 Understanding how it works

![alt text](image.png)

Ketika kita menjalankan aplikasinya (cargo run) setelah kita menambahkan print diluar spawner.spawn ternyata yang ke print duluan adalah print yang berada di luar spawner.spawn dibandingkan yang di dalamnya meski print tersebut berada dibawah spawner.spawn. Hal ini terjadi karena print yang ke print duluan tersebut berada di luar async block yang menyebabkan print tersebut akan diprint secara duluan. Setelah print yang berada di luar async block terprint maka print yang berada dalam spawner.spawn akan terprint setelah diproses executor.run().