#include <iostream>
#include <windows.h>
#include <vector>

using namespace std;

int porownaj(vector<int>&r,int kon)
{
    for(int j=1;j<kon;j++)
    {
        if(r[j]==r[kon])
            return  kon-j;
    }
    return 0;
}

string dziel(int d,int&maks,int&v)
{
    string w="";
    string liczba="1";
    int dl;
    int w1,l;
    vector<int>reszta;
    while(l!=0)
    {
        l=stoi(liczba);
        reszta.push_back(l%d);
        if(reszta.size()>1)
        {
            dl=porownaj(reszta,reszta.size()-1);
            if(dl!=0)
            {
                int ww=w[1]-48;
                if(ww!=l/d)
                   w+=to_string(l/d);
                w.insert(w.size()-dl,"(",1);
                w.insert(w.size(),")",1);
                if(dl>maks)
                {
                    maks=dl;
                    v=d;
                }
                return w;
            }
        }
        w1=l/d;
        w+=to_string(w1);
        l-=d*w1;
        liczba=to_string(l);
        liczba+="0";
    }
    return w;
}

int main()
{
    string wynik;
    int maks=0,v;
    for(int i=2;i<=1000;i++)
    {
        wynik=dziel(i,maks,v);
        wynik.insert(1,".",1);
    }
    cout << "Wartosc posiadajaca maksymalny okres: " << v << endl;
    return 0;
}
