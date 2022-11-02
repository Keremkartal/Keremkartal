#include <iostream>
#include <cmath>
#include <cstdlib>
#include<time.h>
using namespace std;


//*****************************************ATM UYGULAMASI***********************************

void showmenu()
{
    cout << "********ATM SISTEMINE HOSGEDINIZ*******\n";

        cout << "1-Hesap bilgilerini gostermek icin 1'e basiniz\n";
        cout << "2-Para yatirmak icin 2'ye basiniz \n";
        cout << "3-Para cekmek icin 3'e basiniz\n";
        cout << "***************\n";
        cout << "Sseceneginizi seciniz:";

}
int main()
{
    int giris=0;
    int totalbakiye=0, yatirim=0, cekim=0;

    while(1)
    {
        showmenu();
        cin >>giris;

        switch(giris)
        {
            case 1:
                cout<< "Hesabinizdeki toplam para "<<totalbakiye<<"TL'dir\n";
             break;

            case 2:
                cout<< "Yatiriacak tutari giriniz: \n";
                cin >> yatirim;
                totalbakiye+=yatirim;

             break;


            case 3:
                cout<< "Cekilicek miktari giriniz";
                cin >>cekim;
                if(cekim<totalbakiye)
                {
                   totalbakiye-=cekim;
                    cout<< "kalan bakiye"<<totalbakiye;
                }

        }
    }

return 0;
}
