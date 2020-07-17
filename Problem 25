#include <iostream>

using namespace std;

string dodaj(string b1,string a1)
{
    int pb=b1.size()-1;
    int pa=a1.size()-1;
    string cyf,w="";
    int p=0;
    while(pb>=0 || pa>=0)
    {
        int ca,cb,w_s;
        if(pa>=0) ca=a1[pa]-48; else ca=0;
        if(pb>=0) cb=b1[pb]-48; else cb=0;
        w_s=ca+cb+p;
        cyf=to_string(w_s%10);
        w.insert(0,cyf,0,1);
        p=w_s/10;
        pa--;pb--;
    }
    if(p)   w="1"+w;
    return w;
}

string odejmij(string b1,string a1)
{
    int pa=b1.size()-1;
    int pb=a1.size()-1;
    string cyf,w="";
    while(pa>=0 || pb>=0)
    {
        string w_s="";
        int ca,cb,cc;
        if(pa>=0) ca=a1[pa]-48; else ca=0;
        if(pb>=0) cb=b1[pb]-48; else cb=0;
        if(cb-ca<0)
        {
            cb+=10;
            cc=b1[pb-1]-48;
            cc--;
            w_s=to_string(cc);
            b1.erase(pb-1,1);
            b1.insert(pb-1,w_s,0,1);
        }
        cyf=to_string(cb-ca);
        w.insert(0,cyf,0,1);
        pa--;pb--;
    }
    return w;
}

int main()
{
    string a="0";
    string b="1";
    string c;
    int i=1;
    while(b.size()<1000)
    {
        c=dodaj(b,a);
        a=b;
        b=c;
        i++;
    }
    //cout << "Wartosc wyrazu ciagu:\n\n" << b << endl;
    cout << "Numer wyrazu ciagu: " << i << endl;
    return 0;
}
