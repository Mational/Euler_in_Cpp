#include <iostream>

using namespace std;

bool pierwsza( int i )
{
    for( int j=2; j*j<=i; j++ )
    {
        if( i%j==0 )
            return false;
    }
    return true;
}

int main()
{
    int liczba=1;
    int l_pierwsze=0;
    while( l_pierwsze!=10001 )
    {
        liczba++;
        if( pierwsza(liczba)==true )
            l_pierwsze++;
    }
    cout << liczba << endl;
}
