#include <iostream>

using namespace std;

bool nwd(int liczba )
{
    for( int j=1; j<=20; j++ )
    {
        if( liczba%j==0 )
            continue;
        return false;
    }
    return true;
}

int main()
{
    int i;
    for( i=20; nwd(i)==false; i+=20 ){}
    cout << i << endl;
    return 0;
}
