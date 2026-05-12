## Reflection
Jaysen Lestari - 2406395335

> How much data your publisher program will send to the message broker in one run?
Dalam satu kali eksekusi, program publisher akan mengirim **5 pesan** ke message broker. Hal ini terjadi karena pada kode publisher terdapat 5 pemanggilan fungsi `publish_event`, sehingga setiap pemanggilan tersebut akan mengirim satu event ke RabbitMQ.

> The url of: "**amqp://guest:guest@localhost:5672**" is the same as in the subscriber program, what does it mean?
Kesamaan URL `amqp://guest:guest@localhost:5672` pada publisher dan subscriber berarti kedua program terhubung ke **message broker RabbitMQ yang sama**. Publisher menggunakan koneksi tersebut untuk mengirim pesan, sedangkan subscriber menggunakan koneksi yang sama untuk mendengarkan dan menerima pesan dari queue yang sesuai.