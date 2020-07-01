#include <iostream>

using namespace std;

bool czy_pierwsza( int dane )
{
    for(int j=2;j*j<=dane;j++)
    {
        if(dane%j==0)
            return false;
    }
    return true;
}

int main()
{
    long long suma=0;
    for( int i=2; i<2000000; i++ )
    {
        if( czy_pierwsza(i)==true )
        {
            suma+=i;
        }
    }
    cout << suma << endl;
    return 0;
}
