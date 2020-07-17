#include <iostream>
#include <cmath>

using namespace std;

bool is_prime(int n)
{
    if(n==1)
        return false;
    for(int d=2;d*d<=n;d++)
        if(n%d==0)
            return false;
    return true;
}

bool ltr(string liczba)
{
    while(liczba.size()>1)
    {
        liczba.erase(0,1);
        int dane=stoi(liczba);
        if(is_prime(dane)==false)
            return false;
    }
    return true;
}

bool rtl(int liczba)
{
    while(log10(liczba)+1>1)
    {
        liczba/=10;
        if(is_prime(liczba)==false)
            return false;
    }
    return true;
}

int main()
{
    int s=0;
    for(int n=11;n<=1000000;n++)
    {
        if(is_prime(n)==false)
            continue;
        if(ltr(to_string(n))==false)
            continue;
        if(rtl(n)==false)
            continue;
            //cout << n << endl;
        s+=n;
    }
    cout << "Suma: " << s << endl;
    return 0;
}
