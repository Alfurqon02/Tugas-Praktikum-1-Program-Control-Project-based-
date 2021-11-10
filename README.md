# Tugas-Praktikum-1-Program-Control-Project-based-
Sep 8, 2021

Buatlah sebuah program menggunakan bahasa C, yang menerapkan teori-teori di bawah ini.


- Pemilihan menggunakan Switch ATAU If-Else.
- Perulangan menggunakan For.
- Mengimplementasikan Break pada salah satu/semua perulangan dalam program.



            #include <stdio.h> //header standar
            #include <stdlib.h>//header untuk fungsi rand()
            #include<time.h> //header untuk fungsi time ()

            void main() //fungsi utama untuk menjalankan program
            {
            int p;
            char pw[50]; //deklarasi pw = password (case B)
                printf ("Pilihan : \nA.Gacha Nilai\nB.Login\n"); //menampilkan pilihan
                printf ("\nJawab Menggunakan Huruf Kapital (A/B) : ");
                scanf ("%c", &p);
            switch (p){ //percabangan switch untuk meletakkan perintah A dan B

            case 'A':

                srand(time(NULL)); //fungsi yang mengembalikan nilai yang kemudia dijadikan seed_number

            int x, y;
                printf ("\nMau Gacha Berapa kali? ");
                scanf ("%i", &y);
            for (int i = 1; i<=y;i+1) //mengulang sebanyak dengan yg di inputkan
                {x = rand() % 100 + 1; //scaling
                printf ("\nNilai Ke-%d kamu = %d \n", i++, x); //menampilkan nilai

            }
                getchar (); //fungsi untuk menahan layar sampai ada input
            break; //untuk memutus hubungan case A dan B

            case 'B' :

                printf("\nMasukan password: ");
                scanf("%s", &pw);

                // percabangan if/esle
            if( strcmp//untuk menghasilkan nilai false atau nol (0) jika kedua teks yang dibandingkan sama
                    (pw, "Informatika") == 0 ){//password yg akan di masukkan saat login (Informatika)
                    printf("\nWelcome Programmer!\n"); //menampilkan jika password benar
                break; }else {
                    printf("\nPassword Salah!\n"); //menampilkan jika password salah
                 }
                    printf("\nSilahkan Coba Lagi!\n");
            break;
            default :// jika menginput selain A atau B akan menjalankan perintah ini

                printf ("\nMaaf Format Salah!\n");

                }
            }
