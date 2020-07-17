#include <iostream>
#include <cmath>

using namespace std;

int main()
{
    long long n1=165;
    long long pn=n1*( (3*n1)-1)/2;
    long long n2=285;
    long long tn=n2*(n2+1)/2;
    do
    {
        n1++;
        pn=n1*( (3*n1)-1)/2;
        for(n2=n2-2;tn<=pn;n2+=2)
        {
            tn=n2*(n2+1)/2;
            if( tn==pn)
            {
                cout << "Tn: " << tn << endl;
                //cout << "n: " << n2 << endl;
                return 0;
            }
        }
    }while(pn!=tn);
    //cout << tn << endl;
    return 0;
}
