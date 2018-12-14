# Praktikum8

# Praktikum8
##latihan1.cpp : Buatlah algoritma untuk menentukan nilai maksimum dan nilai minimum dari n bilangan bulat dengan menggunakan array.

Alur algoritma

Mendeklarasikan variabel 'int nilai[3],a,min,maks;' sebagai variable input.
Membaca input dari keyboard 'else if(nilai[a] > maks)'
Membandingkan nilai variable //output minimum dan maksimum
![Flowchart](https://raw.githubusercontent.com/MutiaAdindaUtami/Praktikum8.1/master/Flowchart1.png)

![Screenshoot](https://raw.githubusercontent.com/MutiaAdindaUtami/Praktikum8.1/master/poto1.png)

code program lengkap '''c++ //*Program mancari nilai minimum dan maksimum*/
#include <iostream>
#include <conio.h>
using namespace std;
main()
{
   //deklarasi
    int nilai[3],a,min,maks;

   //input-output array
    for(a=1;a<=5;a++){
   cout<<"Masukkan nilai ke-"<<a<<":";
   cin>>nilai[a];
    }

   //proses looping array
   min = nilai[1];
   maks = nilai[1];
   for(a=1;a<=5;a++){
   if(nilai[a] < min){
   min = nilai[a];
   } else if(nilai[a] > maks){
   maks = nilai[a];
   }
   }

   //output minimum dan maksimum
   cout<<"nilai minimum adalah : "<<min<<endl;
   cout<<"nilai maksimum adalah : "<<maks<<endl;

getch();
return 0;
}

###latihan2.cpp : Tentukan modus dari n buah bilangan bulat, dimana besar datanya antara 1 sampai dengan 10.

Alur algoritma

Mendeklarasikan variabel 'class HitungStatistik' sebagai variable input.
Membaca input dari keyboard 'for (int i=0; i<20; i++) f[i] = 0;'
Membandingkan nilai variable HitungStatistik run;
![FlowcharT](https://raw.githubusercontent.com/MutiaAdindaUtami/Praktikum8.1/master/Flowchart2.png)

![Screnshoot](https://raw.githubusercontent.com/MutiaAdindaUtami/Praktikum8.1/master/poto2.png)

code program lengkap '''c++ 
#include <iostream>
#include <math.h>

using namespace std;

class HitungStatistik {
friend ostream& operator<<(ostream&, HitungStatistik&);
friend istream& operator>>(istream&, HitungStatistik&);
public:
HitungStatistik();
void hitung_modus();
private:
void maksimum();
void frekuensi();
int maks, item;
int n;
int A[20];
int f[11];
};

HitungStatistik::HitungStatistik()
{ for (int i=0; i<20; i++) f[i] = 0; }

istream& operator>>(istream& in, HitungStatistik& a) {
cout << "Banyaknya data : ";
cin >> a.n;
for (int i = 0; i < a.n; i++) {
cout << "Data ke- : " << i+1 << " > ";
cin >> a.A[i];
}
return in;
}

void HitungStatistik::maksimum()
{
maks = f[0];
item = 1;
for (int i=0; i<n; i++)
if (f[i] > maks) {
maks = f[i];
item = i;
}
cout << "Modus = " << item;
}

void HitungStatistik::frekuensi()
{
for (int i=1; i<n; i++) ++f[A[i]];
}

void HitungStatistik::hitung_modus() {
cout << "Frekuensi running\n";
frekuensi();
maksimum();
}

ostream& operator<<(ostream& out, HitungStatistik& a) {
cout << "Mulai ...\n";
a.hitung_modus();
cout << "Nilai modus : " << a.item;
return out;
}

main() {
HitungStatistik run;
cin >> run;
cout << run;
return 0;
}

###latihan3.cpp : Buatlah algoritma dan program untuk mengalikan dua buah matriks.

Alur algoritma

Mendeklarasikan variabel '//input matrik pertama void matrik_1(){' sebagai variable input.

Membaca input dari keyboard '//output matrik pertama cout<<"Matrik Pertama :"<<endl;'

Membandingkan nilai variable main (){ matrik_1(); matrik_2();

 			hasil();
 			getch();
 			return 0;
 			}
![Flowchart](https://raw.githubusercontent.com/MutiaAdindaUtami/Praktikum8.1/master/Flowchart3.png)

![Screenshoot](https://raw.githubusercontent.com/MutiaAdindaUtami/Praktikum8.1/master/poto3.png)

code program lengkap '''c++ 
#include <iostream>
#include <conio.h>
using namespace std;

int matrik1[2][2];
int matrik2[2][2];
int matrik3[2][2];
int temp;

//input matrik pertama
void matrik_1(){

int matrik1[2][2];
int matrik2[2][2];
int matrik3[2][2];
int temp;

for (int x = 0;x<2;x++){
for (int y =0;y<2;y++){
cout <<"masukan nilai matrik pertama baris ke-"<<(x+1)<<" kolom ke-"<<(y+1)<<" : ";
cin>>matrik1[x][y];
}# Praktikum8.1
