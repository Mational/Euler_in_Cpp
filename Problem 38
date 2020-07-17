#include <iostream>
#include <cmath>

using namespace std;

bool pandig(string t)
{
    int cyf[10]={1,0,0,0,0,0,0,0,0,0};
    for(int p=0;p<t.size();p++)
    {
        int poz=t[p]-48;
        if(cyf[poz]==1)
            return false;
        cyf[poz]=1;
    }
    return true;
}

int main()
{
    int maks=0;
    for(int n=9;n<10000;n++)
    {
        int i=n;
        string w="";
        while(w.size()<9)
        {
            w+=to_string(i);
            i+=n;
        }
        if(w.size()!=9)
            continue;
        if(pandig(w)==true)
            if(stoi(w)>maks)
                maks=stoi(w);
    }
    cout << "Maks: " << maks;
    return 0;
}
