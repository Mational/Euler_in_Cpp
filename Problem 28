#include <iostream>

using namespace std;

int main()
{
    int n=1001;
    int koniec=n*n;
    int liczba=1,krok=2;
    int suma=1;
    while(liczba!=koniec)
    {
        for(int i=0;i<4;i++)
        {
            liczba+=krok;
            suma+=liczba;
        }
        krok+=2;
    }
    cout << "Suma: " << suma << endl;
    return 0;
}
