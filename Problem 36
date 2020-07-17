#include <iostream>

using namespace std;

bool is_palindromic(string t)
{
    int r=t.size()-1;
    string t2="";
    for(int i=r;i>=0;i--)
        t2+=t[i];

    if(t2==t)
        return true;
    return false;
}

string tbin(int a)
{
    string koniec="";
    while(a>0)
    {
        int b=a%2;
        string ss;
        if( b == 0 )
            koniec="0"+koniec;
        else
            ss = to_string(b);
        koniec=ss+koniec;
        a/=2;
    }
    return koniec;
}

int main()
{
    int s=0;
    int pal;
    string bin;
    for(int n=1;n<1000000;n++)
    {
        if( is_palindromic(to_string(n))==false )
            continue;
        bin=tbin(n);
        if( is_palindromic(bin)==true)
            s+=n;
    }
    cout << s << endl;
    return 0;
}
