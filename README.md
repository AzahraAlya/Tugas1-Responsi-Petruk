# Tugas1-Responsi-Petruk
Pemrograman Terstruktur

#include <iostream>
using namespace std;

//pointer fungsi RataRata
void RataRata(float *sum , int *a){
	
	cout << "\n Rata-rata : " << *sum / *a;
	
}

int main (){

cout<<" ============================================ "<<endl;

cout<<"  Program Menghitung Rata-Rata Edisi Lengkap "<<endl;

cout<<" ============================================= "<<endl;
cout<<endl;

int a = 0; //banyaknya elemen data
int i; //untuk iterasi for
float sum = 0, max = 0, min = 0; 

//minta user input banyaknya data
cout << "Banyaknya bilangan yang akan diinput :";
cin >> a;//*

//bikin array dengan panjang a
float data[a];
//minta user input untuk tiap-tiap element
for(int i=0; i<a; i++) {
    cout << "Input bilangan ke ";
    cout << i+1 << " : ";
    cin >> data[i];
}

sum = 0;
float *ptr;
ptr = data; 

cout<<"\n data yang anda masukkan adalah ";
max = min = *ptr;
for (int i=0; i<a ;i++) {
	cout<< *(ptr + i)<<","; //looping untuk menampilkan lagi bilangan yang di input
	sum = sum + *(ptr + i); //untuk menghitung jumlah dari data yang diinput
	if (max < *(ptr + i)){
		max = *(ptr + i); //menentukan angka terbesar
	}
