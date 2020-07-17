#include <iostream>
#include <cmath>

using namespace std;

string dodawanie(string num1,string num2)
{
    if(num1.size()<num2.size())
        swap(num1,num2);
    string wynik="";
    int p1=num1.size()-1;
    int p2=num2.size()-1;
    int tmp=0;
    int c1,c2;
    int w1,mod;
    int w11=1;
    while(p1>=0)
    {
        if(w11>10)
            break;
        c1=num1[p1]-48;
        if(p2>=0) c2=num2[p2]-48+tmp;
        else      c2=tmp;
        w1=c1+c2;
        mod=w1%10;
        wynik.insert(0,to_string(mod));
        tmp=w1/10;
        p1--;p2--;
        w11++;
    }
    if(tmp>0)
        wynik.insert(0,to_string(tmp));
    return wynik;
}

string mnozenie(string war1,string war2)
{
    string wyn_mnoz="0";
    int r1=war1.size();
    int r2=war2.size();
    for(int p1=r1-1;p1>=0;p1--)
    {
        string wyn="";
        int c1=war1[p1]-48;
        int tmp=0;
        int w10=1;
        for(int p2=r2-1;p2>=0;p2--)
        {
            if(w10>10)
                break;
            int c2=war2[p2]-48;
            int mnoz=c1*c2+tmp;
            wyn.insert(0,to_string(mnoz%10));
            tmp=mnoz/10;
            w10++;
        }
        int prz=r1-(p1+1);
        while(prz>0)
        {
            wyn.insert(wyn.size(),"0");
            prz--;
        }
        if(tmp>0)
            wyn.insert(0,to_string(tmp));
        wyn_mnoz=dodawanie(wyn_mnoz,wyn);
    }
    return wyn_mnoz;
}

string potegowanie(int iliczba)
{
    string swynik="1";
    for(int i=0;i<iliczba;i++)
    {
        swynik=mnozenie(to_string(iliczba),swynik);
    }
    return swynik;
}

int main()
{
    string wynik_pot="0";
    for(int liczba=1;liczba<=1000;liczba++)
    {
        //cout << liczba << endl;
        wynik_pot=dodawanie(wynik_pot,potegowanie(liczba));
    }
    cout << "Wynik: " << wynik_pot << endl;
    return 0;
}
