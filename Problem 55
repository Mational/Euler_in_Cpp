#include <iostream>

using namespace std;

unsigned long long rewers(string t1)
{
    string t2;
    unsigned long long wynik;
    for(int i=t1.size()-1;i>=0;i--)
        t2.insert(t2.end(),t1[i]);
    wynik=stoull(t2);
    return wynik;
}

bool is_palindrom(unsigned long long w1)
{
    unsigned long long w2=rewers(to_string(w1));
    if(w2==w1)
        return true;
    return false;
}

bool is_lychrel(int in)
{
    unsigned long long num1=in;
    for(int k=0;k<50;k++)
    {
        if(num1>10e17)
            break;
        unsigned long long num2=rewers(to_string(num1));
        num1+=num2;
        if(is_palindrom(num1)==true)
            return false;
    }
    return true;
}

int main()
{
    int ile=0;
    for(int n=0;n<=10000;n++)
        if(is_lychrel(n)==true)
        {
            //cout << n << endl;
            ile++;
        }
    cout << "Ile: " << ile << endl;
    return 0;
}
