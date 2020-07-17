#include <iostream>

using namespace std;

const int r=5000;

bool czy_pen(long long t[],int var)
{
    for(int i=0;t[i]<=var;i++)
    {
        if(t[i]==var)
            return true;
    }
    return false;
}

int main()
{
    long long pentagonal[r];
    for(int i=1;i<=r;i++)
        pentagonal[i]=i*((3*i)-1)/2;
    for(int j=1000;j<r;j++)
        for(int k=j+1;k<=r;k++)
        {
            int sum=pentagonal[j]+pentagonal[k];
            int roznica=pentagonal[k]-pentagonal[j];
            if( czy_pen(pentagonal,sum)==true && czy_pen(pentagonal,roznica)==true )
            {
                //cout << "Pj: " << pentagonal[j];
                //cout << "     Pk: " << pentagonal[k];
                cout << "D: " << abs(pentagonal[k]-pentagonal[j]) << endl;
                return 0;
            }
        }
}
