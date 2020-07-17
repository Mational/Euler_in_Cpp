#include <iostream>
#include <vector>

using namespace std;

bool pandigital(string si)
{
    int r=si.size();
    for(int j=1;j<r;j++)
    {
        if(si[j]=='0')
            return false;
        for(int k=0;k<j;k++)
            if(si[k]==si[j])
                return false;
    }
    return true;
}

int mnozna(int liczba)
{
    for(int j=2;j*j<=liczba;j++)
        if(liczba%j==0)
            if(liczba/j!=1 && liczba/j!=liczba)
            {
                string mm=to_string(j)+to_string(liczba/j);
                if(pandigital(mm)==true)
                {
                    mm+=to_string(liczba);
                    if(mm.size()==9)
                        if(pandigital(mm)==true)
                            return liczba;
                }
            }
    return 0;
}

int main()
{
    int suma=0;
    vector<int>pand;

    for(int i=1234;i<=9876;i++)
        if(pandigital(to_string(i))==true)
            pand.push_back(i);

   for(int i=0;i<pand.size();i++)
        suma+=mnozna(pand[i]);

    cout << "Suma: " << suma << endl;
    return 0;
}
