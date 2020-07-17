#include <iostream>
#include <cmath>

using namespace std;

bool wynik(long long l,long long m)
{
    l+=m;
    int cyfry_l=log10(l)+1;
    int cyfry_m=log10(m)+1;
    if(cyfry_l>cyfry_m)
        return true;
    return false;
}

int main()
{
    long long licznik=1;
    long long  mianownik=2;
    int ile=0;
    if(wynik(licznik,mianownik)==true)
        ile++;
    for(int i=0;i<=1000;i++)
    {
        if(log10(licznik)+1>15 || log10(mianownik)+1>15)
        {
            licznik/=1e10;
            mianownik/=1e10;
        }
        licznik+=mianownik*2;
        swap(licznik,mianownik);
        if(wynik(licznik,mianownik)==true)
            ile++;
    }
    cout << ile << endl;
    return 0;
}
