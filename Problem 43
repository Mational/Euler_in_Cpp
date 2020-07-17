#include <iostream>
#include <algorithm>

using namespace std;

long long suma=0;

void warunki(int tab[])
{
    string tekst="";
    if(tab[0]!=0)
    {
            // d2 d3 d4 is divisible by 2
            // d4 d5 d6 is divisible by 5
            if( tab[3]%2!=0 || tab[5]%5!=0 )
                return;
            // d3 d4 d5 is divisible by 3
            if( ( tab[2]+tab[3]+tab[4] )%3!=0 )
                return;
            // d5 d6 d7 is divisible by 7
            if( ( 9*tab[4]+3*tab[5]+tab[6] )%7!=0 )
                return;
            // d6 d7 d8 is divisible by 11
            if( ( ( tab[5]+tab[7] )-tab[6] )%11!=0 )
                return;
            // d7 d8 d9 is divisible by 13
            if( ( 100*tab[6]+10*tab[7]+tab[8] )%13!=0 )
                return;
            // d8 d9 d10 is divisible by 17
            if( ( 100*tab[7]+10*tab[8]+tab[9] )%17!=0 )
                return;
            for(int i=0;i<10;i++)
                tekst+=to_string(tab[i]);
            suma+=stoll(tekst);
    }
}

void permute(int tab[], int l, int r)
{
    if(tab[0]==0)
        return;
    // Przypadek podstawowy
    if (l == r)
        warunki(tab);
    else
    {
        // Permutacja
        for (int i = l; i <= r; i++)
        {
            // Zamiana
            swap(tab[l], tab[i]);
            // Wywołanie rekursyjne
            permute(tab, l+1, r);
            //Powrót``
            swap(tab[l], tab[i]);
        }
    }
}

int main()
{
    int rozmiar=10;
    int tab[rozmiar]={1,0,2,3,4,5,6,7,8,9};
    permute(tab,0,rozmiar-1);
    cout << "Suma: " << suma << endl;
    return 0;
}
