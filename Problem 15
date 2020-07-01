#include <iostream>

using namespace std;

int main()
{
    long long tab[21][21];
    for(int i=0;i<=20;i++)
    {
        tab[i][0]=1;
        tab[0][i]=1;
    }
    for(int j=1;j<=20;j++)
    {
        for(int i=1;i<=20;i++)
            tab[i][j]=tab[i-1][j]+tab[i][j-1];
    }
    cout << tab[20][20] << endl;
    return 0;
}
