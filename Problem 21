#include <iostream>

using namespace std;

int const r=10000;

int d(int number)
{
    int suma=1;
    for(int i=2;i*i<=number;i++)
    {
        if(number%i==0)
        {
            suma+=i;
            if(number/i!=i && number/i!=1)
                suma+=number/i;
        }
    }
    return suma;
}

int main()
{
    int s=0;
    for(int n=4;n<r;n++)
    {
        int a=d(n);
        if(d(a)==n && a!=n)
        {
            s+=n;
        }
    }
    cout << "Suma: " << s << endl;
    return 0;
}
