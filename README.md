# Dimas-Dwiki
Tugas mata kuliah Artificial Intelligence and Apllication pada minggu ke-10
**MODUL 4
TEKNIK PENCARIAN BLIND SEARCH**
4.1 Tujuan Praktikum
	Mahasiswa mampu memahami konsep blind search dan dapat mengimplementasikan program salah satu algoritma blind search pada kasus tree. Program ini dibuat dengan menggunakan bahasa pemrograman Java.
4.2 Tugas
1. Tentukan bagaimana algoritma BFS di atas dapat menentukan node ke 8, 6, dan 7.
Pembahasan :
	Dalam menentukan node ke 8, 6, dan 7 pada algoritma BFS pada modul. Piluh node awal yang dipilih yaitu naode 3. Pada node tersebut terdapat node tetangga pada node 4 dan 2 serta menambahkan ke dalam antran (queue) untuk diproses selanjutnya. Kemudian, algoritma mengambil node 4 yaitu pada node 3, 5, dan 6. Lalu dilanjutkan node 5 dan 6 dalam antrian.
	Algoritma terus berjalan sesuai antrian. Node 5 dan 6 diambil secara berutuan. Node 5 memiliki tetangga 4 dan 6 akan tetapi 4 telah dikunjungi sebelumnya. Maka, node 6 ditambahkan pada antrian selanjutnya. Pada node 1 merupakan tetangga dari node 6 yang diambil selanjutnya ke dalam antrian. Serta node 7 dan 8 ialah tetangga dari node 6. Sampai seterusnya algoritma terus mengambil node-node dari antrian dan memeriksa tangga mereka.
	Maka karena itu, algoritma BFS menentukan node 8,6,dan 7 dengan mengunjungi dan memeriksa node-node secara berutuan sesuai dengan jarak relatif mereka dari node awal (node 3). Berikut merupakan hasil grapfik dari blind search sebagai berikut.
 

2. Ubahlah method static void main sehingga bentuk tree seperti Gambar 4.4 dapat dibentuk. Kemudian tentukan bagaimana algoritma BFS dapat menemukan node 5.
Pembahasan :
Setelah melakukan praktikum menggunakan software Netbeans dan melakukan uji coba pada Modul 4 (nomor 2) ditemukan hasil sebagai berikut.
(0,d=0) (1,d=1) (2,d=1) (3,d=2) (4,d=2) (5,d=2) (6,d=2) BUILD SUCCESSFUL (total time: 0 seconds)
Untuk mengubah metode main agar menciptakan pohon seperti yang diinginkan dalam Gambar 4.5, kita harus mengubah program pada metode main seperti di atas. Dalam perubahan ini, simpul-simpul dan tepi-tepi yang ditambahkan sesuai dengan Gambar 4.5. Simpul 0 memiliki dua anak, yaitu 1 dan 2. Simpul 1 memiliki dua anak, yaitu 3 dan 4. Simpul 2 memiliki dua anak, yaitu 5 dan 6.
Untuk menjelaskan bagaimana algoritma BFS menemukan node 5, berikut adalah langkah-langkahnya:
•	*Node 0 (d=0):* BFS dimulai dari simpul n0 dengan jarak 0.
•	*Node 1 (d=1):* n0 memiliki dua anak, n1 dan n2. BFS melanjutkan ke n1 dengan jarak 1.
•	*Node 3 (d=2):* n1 memiliki dua anak, n3 dan n4. BFS melanjutkan ke n3 dengan jarak 2.
•	*Node 4 (d=2):* n1 juga memiliki anak n4, tetapi n4 sudah diwarnai GRAY (dalam proses BFS), jadi BFS tidak melanjutkan ke n4.
•	*Node 2 (d=1):* Setelah menyelesaikan anak-anak n1, BFS kembali ke n0 dan melanjutkan ke n2 dengan jarak 1.
•	*Node 5 (d=2):* n2 memiliki anak n5. BFS melanjutkan ke n5 dengan jarak 2.
Dengan demikian, algoritma BFS pada graf di atas menemukan node 5 dengan jarak 2 dari node awal (n0).

3. Ubahlah method static void main sehingga bentuk tree seperti gambar 4.5 dapat dibentuk. Kemudian tentukan bagaimana algoritma BFS dapat menemukan node 9.
Pembahasan :
Berikut merupakan Tree 1 pada gambar 4.5 yang terdapat pada modul.
 
Ini adalah hasil dari BFS yang dimulai dari node `n1` dan menandai setiap node dengan jaraknya dari node awal `n1`.
Untuk menemukan node 9 dalam graf tersebut menggunakan algoritma BFS, Anda dapat melihat pada jarak (`distance`) dari setiap node dari node awal. Dalam hasil BFS di atas, node 9 memiliki jarak (`distance`) 3 dari node awal `n1`. Jadi, Anda dapat mengatakan bahwa node 9 ditemukan dalam 3 langkah dari node `n1` dalam BFS. Anda juga dapat melihat bahwa node 9 dicapai melalui node 5 (dalam jarak 2) dan kemudian dari node 5 ke node 9 (dalam jarak 3).
Ini adalah cara algoritma BFS bekerja untuk menemukan node tertentu dalam graf dengan memberikan jarak dari node awal ke node yang dicari. Dalam kasus ini, node 9 ditemukan dalam 3 langkah dari node awal `n1`.
Hasil Program:
 

4. Ubahlah kode program di atas sehingga bentuk tree seperti Gambar 6 dapat dibentuk. Kemudian tentukan bagaimana algoritma BFS dapat menemukan node C.
Pembahasan :
•	BFS dimulai dari node awal, yaitu node 6 (dalam representasi graf Anda).
•	Node 6 dicatat dengan jarak 0 (d=0), dan status warna node diubah menjadi GRAY (menunjukkan bahwa node tersebut sedang diproses).
•	Node 6 memiliki dua tetangga: node 2 dan node 7. Kedua node ini ditambahkan ke antrian BFS.
•	BFS kemudian memeriksa node 2 dari antrian. Node 2 diberi label dengan jarak 1 (d=1) dan status warna GRAY, dan tetangganya (node 1, 4, dan 6) ditambahkan ke antrian.
•	Node 1 yang ada di antrian selanjutnya diberi label dengan jarak 2 (d=2), dan status warna GRAY. Kemudian, tetangganya (node 2) tidak ditambahkan ke antrian karena telah diproses sebelumnya.
•	Node 4 yang ada di antrian selanjutnya diberi label dengan jarak 2 (d=2), dan status warna GRAY. Tetangganya (node 3, 5) ditambahkan ke antrian.
•	Node 3 yang ada di antrian selanjutnya diberi label dengan jarak 3 (d=3), dan status warna GRAY.
•	Setelah semua node di antrian diproses, BFS selesai, dan hasilnya adalah sebagai berikut: (6,d=0) (2,d=1) (7,d=1) (1,d=2) (4,d=2) (9,d=2) (3,d=3) (5,d=3) (8,d=3)
Jadi, algoritma BFS menemukan node 3 dengan mengikuti lintasan dari node 6 ke node 2, dari node 2 ke node 1, dan dari node 2 ke node 4, lalu dari node 4 ke node 3. Node 3 diberi label dengan jarak 3 dari node awal (6).


**MODUL 5
TEKNIK HEURISTIC SEARCH**
5.1 Tujuan
Memperlihatkan kepada mahasiswa bagaimana menyelesaikan permasalahan pada game 8-puzzle dengan menggunakan algoritma heuristic search. Mahasiswa diharapkan mampu mengimplementasikan algoritma heuristic dengan menggunakan Java.
5.2 Tugas
1.	Pelajari class EightPuzzleSearch, EightPuzzleSpace, dan Node.
a.	EightPuzzleSearch
Merupakan kelas yang mewakili algoritma pencarian (seperti A* atau BFS) yang digunakan untuk menyelesaikan masalah teka-teki delapan angka (Eight-Puzzle). Kelas ini mengimplementasikan logika untuk menjalankan pencarian, memantau keadaan ruang masalah, dan menghasilkan solusi.
b.	EightPuzzleSpace
Merupakan kelas yang menggambarkan ruang masalah teka-teki delapan angka. Ruang masalah ini mencakup keadaan awal, tujuan, serta operator-operasi yang diperbolehkan (seperti menggeser angka-angka). Kelas ini berisi metode-metode untuk menghasilkan penerjemahan antara keadaan dan representasinya dalam ruang masalah.
c.	Node
Node adalah entitas dalam struktur data yang digunakan dalam pencarian. Dalam konteks ini, Node mewakili keadaan dalam ruang masalah teka-teki delapan angka. Node ini memiliki informasi tentang keadaan saat ini, g(n) (biaya sejauh ini untuk mencapai node ini), h(n) (fungsi heuristik yang memperkirakan biaya dari node ini ke tujuan), serta referensi ke node yang merupakan pendahulunya. Node digunakan untuk melacak jalur solusi dan melakukan perhitungan dalam algoritma pencarian, seperti A*.

2.	Ubahlah initial dan goal state dari program di atas sehingga bentuk initial dan goal state-nya Gambar 8. Kemudian tentukan langkah-langkah mana saja sehingga puzzlenya mencapai goal state. Analisa dan bedakan dengan solusi pada point 1.

Jawab:
Setelah mengubah initial dan goat state dari program yang diberikan dengan initial = 3 1 2 4 7 5 6 8 0  dan goat state = 1 2 3 4 0 8 5 6 7 , ditemukan hasil penyelesaian sebagai berikut:

 1 2 3 4 5 6 7 8 0 
 1 2 3 4 5 6 7 0 8
 1 2 3 4 0 6 7 5 8
 1 2 3 4 6 0 7 5 8
 1 2 0 4 6 3 7 5 8
 1 0 2 4 6 3 7 5 8
 0 1 2 4 6 3 7 5 8
 4 1 2 0 6 3 7 5 8
 4 1 2 6 0 3 7 5 8
 4 1 2 6 5 3 7 0 8
 4 1 2 6 5 3 0 7 8
 4 1 2 0 5 3 6 7 8
 0 1 2 4 5 3 6 7 8
 1 0 2 4 5 3 6 7 8
 1 2 0 4 5 3 6 7 8
 1 2 3 4 5 0 6 7 8
 1 2 3 4 0 8 5 6 7 

3.	Ubahlah initial dan goal state dari program di atas sehingga bentuk initial dan goal state-nya Gambar 5.9. Kemudian tentukan langkah-langkah mana saja sehingga puzzlenya mencapai goal state. Analisa dan bedakan dengan solusi pada point 1 dan 2.

Jawab:
Setelah mengubah initial dan goat state dari program yang diberikan dengan initial = 1 5 3 4 6 8 2 7 0  dan goat state = 7 6 5 8 0 4 1 2 3, ditemukan hasil penyelesaian sebagai berikut:
1 5 3 4 6 8 2 7 0
1 5 3 4 6 0 2 7 8
1 5 0 4 6 3 2 7 8
1 0 5 4 6 3 2 7 8
1 6 5 4 0 3 2 7 8
1 6 5 4 7 3 2 0 8
1 6 5 4 7 3 2 8 0
1 6 5 4 7 0 2 8 3
1 6 0 4 7 5 2 8 3
1 0 6 4 7 5 2 8 3
1 7 6 4 0 5 2 8 3
1 7 6 0 4 5 2 8 3
0 7 6 1 4 5 2 8 3
7 0 6 1 4 5 2 8 3
7 6 0 1 4 5 2 8 3
7 6 5 1 4 0 2 8 3
7 6 5 1 4 0 2 8 3
7 6 5 1 0 4 2 8 3
7 6 5 1 8 4 2 0 3
7 6 5 1 8 4 0 2 3
7 6 5 0 8 4 1 2 3
7 6 5 8 0 4 1 2 3

4.	Ubahlah initial dan goal state dari program di atas sehingga bentuk initial dan goal state-nya Gambar 5.10. Kemudian tentukan langkah-langkah mana saja sehingga puzzlenya mencapai goal state. Analisa dan bedakan dengan solusi pada point 1, 2, dan 3.

Jawab:
Setelah mengubah initial dan goat state dari program yang diberikan dengan initial = 1 2 3 4 5 6 7 8 0  dan goat state = 1 2 3 4 0 5 6 7 8, ditemukan hasil penyelesaian sebagai berikut:
 1 2 3 4 5 6 7 8 0 
 1 2 3 4 5 6 7 0 8
 1 2 3 4 0 6 7 5 8
 1 2 3 4 6 0 7 5 8
 1 2 0 4 6 3 7 5 8
 1 0 2 4 6 3 7 5 8
 0 1 2 4 6 3 7 5 8
 4 1 2 0 6 3 7 5 8
 4 1 2 6 0 3 7 5 8
 4 1 2 6 5 3 7 0 8
 4 1 2 6 5 3 0 7 8
 4 1 2 0 5 3 6 7 8
 0 1 2 4 5 3 6 7 8
 1 0 2 4 5 3 6 7 8
 1 2 0 4 5 3 6 7 8
 1 2 3 4 5 0 6 7 8
 1 2 3 4 0 5 6 7 8

5.	Ubahlah initial dan goal state dari program dan class-class di atas sehingga bentuk initial dan goal state-nya Gambar 5.11. Kemudian tentukan langkah-langkah mana saja sehingga puzzlenya mencapai goal state.

Jawab:
Setelah mengubah initial dan goat state dari program yang diberikan dengan initial = D B E A F G H C 0  dan goat state = A H G B 0 F C D E. Kita lakukan permisalan seperti berikut:
A = 1
B = 2
C = 3
D = 4
E = 5
F = 6
G = 7
H = 8
Kosong = 0

ditemukan hasil penyelesaian sebagai berikut:
4 2 5 1 0 7 8 3 6
4 2 5 0 1 7 8 3 6
4 2 5 1 0 7 8 6 3
4 2 5 1 4 7 8 6 3
4 2 5 1 7 0 8 6 3
4 2 5 1 7 8 0 6 3
4 2 5 1 0 8 7 6 3
4 2 5 0 1 8 7 6 3
4 2 5 6 0 8 7 1 3
4 2 5 6 8 0 7 1 3
4 2 5 6 8 1 7 0 3
4 2 5 6 8 1 0 7 3
4 2 5 6 8 1 3 7 0
4 2 5 6 8 1 3 0 7
4 2 5 6 1 8 3 0 7
4 2 5 6 1 3 8 0 7
4 2 5 6 1 3 8 7 0

