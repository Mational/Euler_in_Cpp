#include <iostream>
#include <cmath>

using namespace std;

int main()
{
    float wynik=1;
    for(int i=1;i<100;i++)
        wynik*=i;
    int ile=0;
    for(int n=23;n<=100;n++)
    {
        int r=1;
        while(true)
        {
            float licz=1;
            int m1=r;
            int m2=n-r;
            if(m2>m1)
                swap(m1,m2);
            for(int i=m1+1;i<=n;i++)
            {
                if(m2>1)
                    licz/=m2--;
                licz*=i;
            }
            if(licz>1e+6)
            {
                ile+=((n/2)-r)*2+1;
                if(n%2!=0)
                    ile++;
                break;
            }
            r++;
        }
    }
    cout << "Ile: " << ile << endl;
    return 0;
}
