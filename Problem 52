#include <iostream>
#include <vector>
#include <cmath>

using namespace std;

void nowa(int idane,int t[])
{
    int d=log10(idane)+1;
    for(int i=0;i<d;i++)
    {
        t[idane%10]++;
        idane/=10;
    }
    return;
}

int main()
{

    for(int liczba=1;liczba<10e6;liczba++)
    {
        int t1[10]={0};
        int n=liczba;
        int d1=log10(n)+1;
        for(int i=0;i<d1;i++)
        {
            t1[n%10]++;
            n/=10;
        }
        for(int k=2;k<=6;k++)
        {
            int t2[10]={0};
            nowa(k*liczba,t2);
            for(int i=0;i<10;i++)
                if(t1[i]!=t2[i])
                    goto next;
        }
        cout << liczba << endl;
        return 0;
        next:;
    }
    return 0;
}
