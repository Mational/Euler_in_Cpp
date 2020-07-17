#include <iostream>

using namespace std;

int nwd_f(int a,int b)
{
    int nwd=a;
    if(b%nwd!=0)
    {
        nwd/=2;
        while(b%nwd!=0 || a%nwd!=0) nwd--;
    }
    return nwd;
}

void skroc(int dzielna,int dzielnik,int&w)
{
    int d=nwd_f(dzielna,dzielnik);
    if(d==1)
        return;
    int da=dzielna/d;
    int dk=dzielnik/d;
    if(da<10 && dk<10);
        if(da==dzielna/10 && dk==dzielnik%10 && dzielna%10==dzielnik/10)
            w*=dk;
}

int main()
{
    int wynik=1;
    for(int i=99;i>10;i--)
        for(int j=i-1;j>=10;j--)
            if(i%10!=0 || j%10!=0)
                skroc(j,i,wynik);
    cout << "Wynik: " << wynik << endl;
}
