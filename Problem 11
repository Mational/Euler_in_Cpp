#include <iostream>
#include <fstream>
#include <vector>

using namespace std;

void czytaj(int t[20][20],string sciezka)
{
    fstream plik;
    plik.open(sciezka,ios::in);
    while(!plik.eof())
    {
        int liczba;
        for(int i=0;i<20;i++)
        {
            for(int j=0;j<20;j++)
            {
                plik >> liczba;
                t[i][j]=liczba;
            }
        }
    }
    plik.close();
    return;
}

void poziomo(int t[20][20],long long&maks)
{
    for(int i=0;i<20;i++)
    {
        for(int j=0;j<17;j++)
        {
            long long iloczyn=1;
            for(int z=0;z<4;z++)
                iloczyn*=t[i][j+z];
            if(iloczyn>maks)
                maks=iloczyn;
        }
    }
    return;
}

void pionowo(int t[20][20],long long&maks)
{
    for(int j=0;j<20;j++)
    {
        for(int i=0;i<17;i++)
        {
            long long iloczyn=1;
            for(int z=0;z<4;z++)
                iloczyn*=t[i+z][j];
            if(iloczyn>maks)
                maks=iloczyn;
        }
    }
    return;
}

void przekatna_p(int t[20][20],long long&maks)
{
    for(int i=0;i<17;i++)
    {
        for(int j=0;j<17;j++)
        {
            long long iloczyn=1;
            for(int z=0;z<4;z++)
                iloczyn*=t[i+z][j+z];
            if(iloczyn>maks)
                maks=iloczyn;
        }
    }
    return;
}

void przekatna_l(int t[20][20],long long&maks)
{
    for(int i=0;i<17;i++)
    {
        for(int j=19;j>=3;j--)
        {
            long long iloczyn=1;
            for(int z=0;z<4;z++)
                iloczyn*=t[i+z][j-z];
            if(iloczyn>maks)
                maks=iloczyn;
        }
    }
    return;
}

int main()
{
    long long maks=0;
    int tab[20][20];
    czytaj(tab,"liczby.txt");
    poziomo(tab,maks);
    pionowo(tab,maks);
    przekatna_p(tab,maks);
    przekatna_l(tab,maks);
    cout << maks << endl;
    return 0;
}
