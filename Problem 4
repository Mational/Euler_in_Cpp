#include <iostream>
#include <math.h>
#include <windows.h>

using namespace std;

int palindrom( int idane )
{
    string pal;
    int r=log10(idane)+1;
    for( int z=0; z<r; z++ )
    {
        pal+=to_string(idane%10);
        idane/=10;
    }
    return stoi(pal);
}

bool czy_palindrom( int dane )
{
    int wynik=palindrom(dane);
    if( wynik==dane )
        return true;
    return false;
}

int main()
{
    int liczba;
    int maks=0;
    for( int i=999; i>=100; i-- )
    {
        for( int j=999; j>=100; j-- )
        {
            liczba=i*j;
            if( czy_palindrom(liczba)==true )
            {
                if( liczba>maks)
                    maks=liczba;
            }
        }
    }
    cout << "Wynik: " << maks << endl;
    return 0;
}
