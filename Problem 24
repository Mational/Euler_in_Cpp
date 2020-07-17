#include <iostream>
#include <algorithm>

using namespace std;

int main()
{
   /* char ca[]="0123456789";

    for(int i=1;i<1000000;i++)
        next_permutation(ca,ca+10);
    cout << ca << endl;*/
    int it=0;
    for(int a=0;a<=9;a++)
        for(int b=0;b<=9;b++)
            if(b!=a)
            for(int c=0;c<=9;c++)
                if(c!=b && c!=a)
                for(int d=0;d<=9;d++)
                    if(d!=c && d!=b && d!=a)
                    for(int e=0;e<=9;e++)
                        if(e!=d && e!=c && e!=b && e!=a)
                        for(int f=0;f<=9;f++)
                            if(f!=e && f!=d && f!=c && f!=b && f!=a)
                            for(int g=0;g<=9;g++)
                                if(g!=f && g!=e && g!=d && g!=c && g!=b && g!=a)
                                for(int h=0;h<=9;h++)
                                    if(h!=g && h!=f && h!=e && h!=d && h!=c && h!=b && h!=a)
                                    for(int i=0;i<=9;i++)
                                        if(i!=h && i!=g && i!=f && i!=e && i!=d && i!=c && i!=b && i!=a)
                                        for(int j=0;j<=9;j++)
                                        {
                                            if(j!=i && j!=h && j!=g && j!=f && j!=e && j!=d && j!=c && j!=b && j!=a)
                                                it++;
                                            if(it==1000000)
                                            {
                                                cout <<a<<b<<c<<d<<e<<f<<g<<h<<i<<j<<endl;
                                                return 0;
                                            }
                                        }
    return 0;
}
