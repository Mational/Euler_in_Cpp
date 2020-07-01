#include <iostream>
#include <vector>

using namespace std;

void dziel( long long liczba, vector <long long> & d )
{
    for( long long i=2; i*i<=liczba; i++ )
    {
        if( liczba%i==0 )
        {
            d.push_back(i);
            if( liczba/i != i && liczba/i != 1 )
                d.push_back(liczba/i);
        }
    }
    return;
}

bool czy_pierwsza(long long liczba )
{
    for( int i=2; i*i<=liczba; i++ )
    {
        if( liczba%i==0 )
        {
            return false;
            if( liczba/i != i && liczba/i != 1 )
                return false;
        }
    }
    return true;
}

void naj_dziel( vector <long long> & d )
{
    long long maks=0;
    for( int i=0; i<d.size(); i++ )
    {
        //cout << d[i] << endl;
        if( czy_pierwsza(d[i])==true )
            if( maks<d[i] )
                maks=d[i];
    }
    cout << "Wynik: " << maks << endl;
    return;
}

int main()
{
    long long a=600851475143;
    vector <long long> dzielniki;
    dziel(a, dzielniki);
    naj_dziel(dzielniki);
    return 0;
}
