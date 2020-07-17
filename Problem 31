#include <iostream>

using namespace std;

int monety[8]={1,2,5,10,20,50,100,200};
int ilosc=200;

int komb(int cel, int naj_moneta)
{
    if(naj_moneta<=0)  return 1;
    int odp=0;
    while(cel>=0)
    {
        odp+=komb(cel,naj_moneta-1);
        cel-=monety[naj_moneta];
    }
    return odp;
}

int main()
{
    cout << komb(ilosc,7);
    return 0;
}
