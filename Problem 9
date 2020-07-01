#include <iostream>

using namespace std;

int main()
{
    int a,b,c;
    long long wynik=0;
    for( c=3; c<=1000;c++ )
    {
        for( b=2; b<=1000; b++ )
        {
            if(b>=c)
                break;
            else
            {
                for( a=1; a<=1000;a++ )
                {
                    if( a>=b)
                        break;
                    else
                    {
                        if( a+b+c==1000 && (a*a)+(b*b)==(c*c) )
                        {
                            cout << "A: " << a << "    B: " << b << "    C: " << c << endl;
                            wynik=a*b*c;
                            cout << "Wynik: " << wynik << endl;
                        }
                    }
                }
            }
        }
    }
    return 0;
}
