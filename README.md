# Module 10 - Timer

![Image when theres a print outside of the spawn method](./msg_outside_spawn.png)

Dari gambar di atas, dapat dilihat bahwa pesan `Maxwell's Computer: outside spawn` merupakan pesan yang paling pertama di print yang kemudian diikuti oleh pesan `Maxwell's Computer: howdy!` dan setelah 2 detik berlalu, `Maxwell's Computer: done!`. Hal ini disebabkan karena pesan `howdy!` dan `done!` merupakan sebuah `future` yang baru akan dijalankan ketika `executor` berjalan. Karena perintah print untuk message `outside spawn` berada tepat setelah bagian `spawner.spawn(...)` dan sebelum `executor.run()`, perintah print `outside spawn` tersebut akan dijalankan terlebih dahulu sebelum perintah print `howdy!` dan `done!`.
