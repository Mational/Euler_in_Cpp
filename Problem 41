#include <iostream>
#include <cmath>

using namespace std;

bool is_pandigit(string dane)
{
    int r=dane.size();
    int tab[8]={1,0,0,0,0,0,0,0};
    for(int p=0;p<r;p++)
    {
        int c=dane[p]-48;
        if(c>r)
            return false;
        if(tab[c]==1)
            return false;
        tab[c]=1;
    }
    return true;
}

bool is_prime(int dane)
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
    int wynik;
/*  ****************************************************
    *                                                  *
    *  I start with 7654321 because:                   *
    *  Sum of 1 to 9 is 45 which is divisible by 3     *
    *  Sum of 1 to 8 is 36 which is divisible by 3     *
    *  Sum of 1 to 7 is 28 which isn't divisible by 3  *
    *                                                  *
    ****************************************************
*/
    for(int l=7654321;l>=0;l--)
    {
        if(is_pandigit(to_string(l))==false)
            continue;
        if(is_prime(l)==true)
        {
            wynik=l;
            break;
        }
    }
    cout << "Wynik: " << wynik << endl;
    return 0;
}
