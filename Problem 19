#include <iostream>

using namespace std;

int main()
{
    int mies[13]={0,31,29,31,30,31,30,31,31,30,31,30,31};
    int dni;
    int dzien=0;
    int ile_niedziel=0;
    for(int i=1900;i<=2000;i++)
    {
        int rok=0;
        bool p=false;
        if(i%100==0)
        {
            if(i%400==0)
                p=true;
        }
        else if(i%4==0) p=true;
        for(int j=1;j<=12;j++)
        {
            if(j==2)
            {
                if(p==true) dni=29;
                else        dni=28;
            }
            else    dni=mies[j];
            for(int k=1;k<=dni;k++)
            {
                rok++;
                dzien++;
                if(dzien%7==0 && i>1900 && k==1)
                    ile_niedziel++;
            }
        }
        //cout << rok << endl;
    }
    //cout << dzien << endl;
    cout << ile_niedziel << endl;
    return 0;
}
