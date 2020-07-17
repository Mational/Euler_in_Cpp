#include <iostream>
#include <cmath>
#include <vector>

using namespace std;

bool powtarza(string w, vector<string>&l)
{
    for(int i=0;i<l.size();i++)
        if(w==l[i])
            return true;
    return false;
}

int main()
{
    int kombinacje=0;
    string wynik;
    vector<string>lista;
    for(int a=2;a<=100;a++)
    {

        for(int b=2;b<=100;b++)
        {
            wynik=to_string(pow(a,b));
            if(powtarza(wynik,lista)==false)
            {
                kombinacje++;
                lista.push_back(wynik);
            }
        }
    }
    cout << kombinacje << endl;
    return 0;
}
