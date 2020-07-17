#include <iostream>
#include <fstream>
#include <vector>

using namespace std;

void odczyt(vector<string>&v,string sciezka)
{
    fstream plik;
    plik.open(sciezka,ios::in);
    while(!plik.eof())
    {
        string wiersz="";
        plik >> wiersz;
        v.push_back(wiersz);
    }
    return;
}

void sortuj(vector<string>&v)
{
    string im1,im2;
    int l1,l2,r2;
    int r=v.size();
    for(int i=0;i<r;i++)
        for(int j=1;j<r-i;j++)
        {
            im1=v[j-1];
            im2=v[j];
            for(int k=0;k<im1.size();k++)
            {
                l1=im1[k]-64;
                l2=im2[k]-64;
                if(l1>l2)
                    swap(v[j-1],v[j]);
                else if(l1==l2)
                {
                    if(k==im1.size()-1)
                    {
                        if(im1.size()>=im2.size())
                            swap(v[j-1],v[j]);
                        break;
                    }
                    continue;
                }
                break;
            }
        }
}

int main()
{
    vector<string>imiona;
    string name;
    int l,suma=0;
    long long s=0;
    odczyt(imiona,"names.txt");
    sortuj(imiona);
    for(int i=0;i<imiona.size();i++)
    {
        suma=0;
        name=imiona[i];
        for(int j=0;j<name.size();j++)
        {
            l=name[j]-64;
            suma+=l;
        }
        s+=suma*(i+1);
    }
    cout << "Suma: " << s << endl;
    return 0;
}
