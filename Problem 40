#include <iostream>
#include <cmath>

using namespace std;

int main()
{
    int wynik=1;
    int d=0;
    int liczba=1;
    for(int n=1;n<=1000000;n*=10)
    {
        while(true)
        {
            int r=log10(liczba)+1;
            if(d+r>=n)
            {
                int p=n-d;
                string t=to_string(liczba);
                wynik*=t[p-1]-48;
                break;
            }
            d+=r;
            liczba++;
        }
    }
    cout << "Wynik: " << wynik << endl;
    return 0;
}
