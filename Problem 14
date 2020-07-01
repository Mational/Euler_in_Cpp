#include <iostream>

using namespace std;

int collatz(long long liczba,int lancuch)
{
    if(liczba==1)
        return lancuch;
    if(liczba%2==0)
        return collatz(liczba/2,lancuch+1);
    else
        return collatz(liczba*3+1,lancuch+1);
}

int main()
{
    int dl;
    int maks_lancuch=0;
    int max_liczba=0;
    for(int i=2;i<1000000;i++)
    {
        dl=collatz(i,1);
        if(dl>maks_lancuch)
        {
            //cout << "Dlugosc: " << dl << endl;
            // cout << "Liczba: " << i << endl;
            maks_lancuch=dl;
            max_liczba=i;
        }
    }
    cout << "WYNIK: " << max_liczba << endl;
    return 0;
}
