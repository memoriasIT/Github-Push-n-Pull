#include <iostream>
#include <stdio.h>
using namespace std;

void title();
int menu();
int upload();
int download();

int main(){
title();
menu();

return 0;
}

void title(){
string Title = "$$$$$$\\ $$$$$$$$\\ $$$$$$$\\            $$\\ $$\\                     \r\n"
"\\_$$  _|\\__$$  __|$$  __$$\\           $$ |$$ |                    \r\n"
"  $$ |     $$ |   $$ |  $$ |$$\\   $$\\ $$ |$$ | $$$$$$\\   $$$$$$\\  \r\n"
"  $$ |     $$ |   $$$$$$$  |$$ |  $$ |$$ |$$ |$$  __$$\\ $$  __$$\\ \r\n"
"  $$ |     $$ |   $$  ____/ $$ |  $$ |$$ |$$ |$$$$$$$$ |$$ |  \\__|\r\n"
"  $$ |     $$ |   $$ |      $$ |  $$ |$$ |$$ |$$   ____|$$ |      \r\n"
"$$$$$$\\    $$ |   $$ |      \\$$$$$$  |$$ |$$ |\\$$$$$$$\\ $$ |      \r\n"
"\\______|   \\__|   \\__|       \\______/ \\__|\\__| \\_______|\\__|      \r\n"
"\n--------{---(@\r\n"
"PUSH AND PULL TO GITHUB REPOSITORY SCRIPT\r\n"
"\n\nSelect your option\r\n"
"   1) Upload new content\r\n"
"   2) Clone repository (download)\r\n\n\n";

cout << Title;
}

int menu(){
char option;
cin >> option;
while (option != '1' && option != '2'){
            cout << "That's not a valid input, try again: ";
            cin >> option;
}

switch (option){
    case '1':
        upload();
        break;
    case '2':
        download();
        break;
}
}

int upload(){
char option;
string comment, url;

system("cls");
cout << "This file should be in the directory you want to upload. This is the current directory:  " << endl; system("cd"); cout << "\nDo you want to continue? (Y/N)";
cin >> option;
if (option == 'Y' || option == 'y'|| option == '1'){
    cout << "Inizialiting github...  " << endl;
    system("git init");
    system("git add .");
    cout << "Introduce comment for your initial commit: ";
    cin >> comment;
    system(("git commit -m "+comment).c_str());
    cout << "Introduce Github URL to push: \n";
    cin >> url;
    system(("git remote add origin "+url).c_str());
    system("git remote -v");
    system("git push origin master");
    cout << "\n\nProcess Completed!\n\n\n";
} else {
    return 0;
}
}

int download(){
char option;
string username,repo, url;
cout << "This file should be in the directory you want to be the repository to be downloaded. This is the current directory:  " << endl; system("cd"); cout << "\nDo you want to continue? (Y/N)";
cin >> option;
if (option == 'Y' || option == 'y'|| option == '1'){
    cout << "Introduce your username: ";
    cin >> username;
    cout << "Introduce Repository name: ";
    cin >> repo;
    url = "https://github.com/" + username + '/' + repo;
    system(("git clone "+url).c_str());
    cout << "\n\nProcess Completed!\n\n\n";
} else {
    return 0;
}

}
