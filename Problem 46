#include <iostream>
#include <cmath>

using namespace std;

bool czy_zlozona_niep(int iliczba)
{
    for(int i=2;i*i<=iliczba;i++)
        if(iliczba%i==0 && iliczba%2!=0)
            return true;
    return false;
}

bool czy_pierwsza(int dane)
{
    for(int j=2;j*j<=dane;j++)
        if(dane%j==0)
            return false;
    return true;
}

bool goldbach(int iliczba)
{
    for(int i=2;i<=iliczba;i++)
        if(czy_pierwsza(i)==true)
            for(int j=1;2*j*j+i<=iliczba;j++)
            {
                int gnumber=2*j*j+i;
                if(gnumber==iliczba)
                    return true;
            }
    return false;
}

int main()
{
    int liczba=8;
    bool gold=false;
    do
    {
        liczba++;
        if(czy_zlozona_niep(liczba)==true)
            gold=goldbach(liczba);
    }while(gold==true);
    cout << liczba << endl;
    return 0;
}
