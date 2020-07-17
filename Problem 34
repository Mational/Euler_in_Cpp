#include <iostream>

using namespace std;

int digit_fac(int liczba)
{
    int frac[10]={1,1,2,6,24,120,720,5040,40320,362880};
    int s=0;
    string t=to_string(liczba);
    for(int i=0;i<t.size();i++)
        s+=frac[t[i]-48];
    return s;
}

int main()
{
    int df;
    int suma=0;
    for(int n=3;n<50000;n++)
        if(digit_fac(n)==n)
            suma+=n;

    cout << "Suma: " << suma << endl;
    return 0;
}
