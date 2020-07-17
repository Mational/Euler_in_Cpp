#include <iostream>
#include <math.h>

using namespace std;

bool prime(int num)
{
    for(int i=2;i*i<=num;i++)
        if(num%i==0)
            return false;
    return true;
}

int main()
{
    int w;
    int maks=0,ma,mb;
    for(int a=-999;a<1000;a++)
    {
        if(prime(abs(a))==false)
            continue;
        for(int b=-1000;b<=1000;b++)
        {
            if(prime(abs(b))==false)
                continue;
            int ile=0;
            for(int n=0;prime(n*n+n*a+b)==true;n++)
            {
                if(n*n+n*a+b<0)
                    break;
                ile++;
            }
            if(ile>maks)
            {
                maks=ile;
                ma=a;
                mb=b;
            }
        }
    }
    //cout << "Maks: " << maks << "  A: " << ma << "  B: " << mb << endl;
    cout << "Iloczyn: " << ma*mb << endl;
    return 0;
}
