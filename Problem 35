#include <iostream>
#include <cmath>

using namespace std;

bool is_prime(int a)
{
    for(int d=2;d*d<=a;d++)
        if(a%d==0)
            return false;
    return true;
}

int circle(string a)
{
    string b=a;
    a[0]=b[b.size()-1];
    int i=1;
    do
    {
        a[i]=b[i-1];
        i++;
    }while(i<a.size());
    return stoi(a);
}

int main()
{
    int ile=0;
    for(int n=2;n<1000000;n++)
    {
        if(is_prime(n)==false)
            continue;
        int r=log10(n)+1;
        int l=n;
        int pr=1;
        for(int p=1;p<r;p++)
        {
           l=circle(to_string(l));
           if(is_prime(l)==false)
                break;
            pr++;
        }
        if(pr==r)
            ile++;
    }
    cout << "Wynik: " << ile << endl;
    return 0;
}
