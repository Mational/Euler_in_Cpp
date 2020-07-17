#include <iostream>

using namespace std;

int main()
{
    int maks=0;
    int mp=0;
    for(int p=6;p<=1000;p++)
    {
        int i=0;
        for(int a=2;a<p/3;a++)
            while(a+(a+1)+(a+2)<=p)
            {
                int b=(p-a)/2;
                int c=p-a-b;
                while( (a*a)+(b*b)>(c*c) && b>a )
                {
                    b-=1;
                    c+=1;
                }
                if( (a*a)+(b*b)==(c*c) )
                    i++;
                break;
            }
        if(i>maks)
        {
            maks=i;
            mp=p;
        }
    }
    //cout << "Maks ilosc: " << maks << endl;
    cout << "Dla p: " << mp << endl;
    return 0;
}
