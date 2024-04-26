# Reading-from-file-into-array
// مها محمد حمدى

#include <iostream>
#include <fstream>
#include<string>
using namespace std;

ifstream file("mydata.txt");


void read_from_file(string name,int storage[],int size);
void show(int enteries, int arr[]);
int main()
{
   
    // Check if the file is successfully opened
    if (!file.is_open()) {
        cout << "Error opening the file!" << endl;
        return 1;
    }
    int storage[100];
    int size = 10;
    read_from_file("mydata.txt",storage,size );

    show(size,storage);
    

   // file.close();
	return 0;
}
void read_from_file(string name ,int storage[],int size) {
    for (int i = 0;i < size;i++) {
        file >> storage[i];

    }
}
void show(int enteries, int arr[]) {
    for (int i = 0;i < enteries;i++) {
        cout << arr[i] << endl;
    }
}


