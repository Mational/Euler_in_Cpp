#include <iostream>
#include <cmath>

using namespace std;

int cyfry_5(int liczba)
{
    int c,c_5=0;
    string t=to_string(liczba);
    for(int j=0;j<t.size();j++)
    {
        c=t[j]-48;
        c_5+=pow(c,5);
    }
    return c_5;
}

int main()
{
    int s=0;
    for(int i=2;i<200000;i++)
        if(cyfry_5(i)==i)
            s+=i;
    cout << s << endl;
    return 0;
}
