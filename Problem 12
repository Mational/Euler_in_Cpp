#include <iostream>

using namespace std;

int dzielniki(int ii)
{
    int dziel=0;
    for(int j=1;j*j<=ii;j++)
    {
        if(ii%j==0)
        {
            dziel++;
            if(ii/j!=j && ii/j!=1)
                dziel++;
        }
    }
    return dziel;
}

int main()
{
    long long suma=0;
    int max_dziel=0;
    int i=1;
    while(max_dziel<500)
    {
        suma+=i;
        int l_dzielnikow=dzielniki(suma);
        if(l_dzielnikow>max_dziel)
            max_dziel=l_dzielnikow;
        i++;
    }
    cout << suma << endl;
    return 0;
}
