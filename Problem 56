#include <iostream>


using namespace std;

int mdigit=0;

string dodawanie(string sa,string sb)
{
    if(sa.size()<sb.size())
        swap(sa,sb);
    int tmp=0;
    int ia,ib;
    int sum=0;
    char d;
    int pa=sa.size()-1;
    int pb=sb.size()-1;
    string wynik="";
    while(pa>=0)
    {
        ia=sa[pa]-48;
        if(pb>=0)
            ib=sb[pb]-48;
        else
            ib=0;
        sum=ia+ib+tmp;
        d=(sum%10)+48;
        wynik=d+wynik;
        tmp=sum/10;
        pb--;
        pa--;
    }
    if(tmp>0)
    {
        d=tmp+48;
        wynik=d+wynik;
    }
    return wynik;
}

string mnozenie(string a,string b)
{
    if(a.size()>b.size())
        swap(a,b);
    string w="0";
    int ia,ib;
    for(int i=a.size()-1;i>=0;i--)
    {
        string wyn1="";
        int tmp=0;
        char d;
        int s=0;
        ia=a[i]-48;
        for(int j=b.size()-1;j>=0;j--)
        {
            ib=b[j]-48;
            s=(ia*ib)+tmp;
            d=(s%10)+48;
            tmp=s/10;
            wyn1=d+wyn1;
        }
        if(tmp>0)
        {
            d=tmp+48;
            wyn1=d+wyn1;
        }
        for(int j=(a.size()-1)-i;j>0;j--)
            wyn1+="0";
        w=dodawanie(w,wyn1);
    }
    return w;
}

int sum_cyfr(string tekst)
{
    int s=0;
    int r=tekst.size();
    for(int i=0;i<r;i++)
        s+=tekst[i]-48;
    return s;
}

string potegowanie(int wykladnik,int potega)
{
    string a=to_string(wykladnik);
    string b=to_string(potega);
    string wynik="1";
    for(int i=stoi(b);i>0;i--)
    {
        wynik=mnozenie(wynik,a);
        int suma_cyfr=sum_cyfr(wynik);
        if(suma_cyfr>mdigit)
            mdigit=suma_cyfr;
    }
    return wynik;
}

int main()
{
    for(int a=1;a<100;a++)
        potegowanie(a,99);
    cout << "MDigit: " << mdigit << endl;
    return 0;
}
