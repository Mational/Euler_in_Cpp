#include <iostream>

using namespace std;

bool czy_pierwsza(int iliczba)
{
    for(int j=2;j*j<=iliczba;j++)
        if(iliczba%j==0)
            return false;
    return true;
}

int main()
{
    float pierwsze=0;
    float wszystkie=1;
    int r=0;
    int liczba=1;
    do
    {
        r+=2;
        for(int i=0;i<4;i++)
        {
            liczba+=r;
            wszystkie++;
            if(czy_pierwsza(liczba)==true)
                pierwsze++;
        }
        //cout << pierwsze/wszystkie << endl;
    }while(pierwsze/wszystkie>0.1);
    cout << "Warstwa: " << r+1 << endl;
    return 0;
}
