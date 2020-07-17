#include <iostream>

using namespace std;

bool is_prime(int in)
{
    for(int i=2;i*i<=in;i++)
        if(in%i==0)
            return false;
    return true;
}

bool perm(int in, int in2)
{
    int t1[10],t2[10];
    for(int i=0;i<10;i++)
    {
        t1[i]=0;
        t2[i]=0;
    }
    for(int i=0;i<4;i++)
    {
        t1[in%10]++;
        t2[in2%10]++;
        in/=10;
        in2/=10;
    }
    for(int i=0;i<10;i++)
        if(t1[i]!=t2[i])
            return false;
    return true;
}

int main()
{
    for(int n=1000;n<3333;n++)
    {   if(is_prime(n)==true)
        {
            int r=(10000-n)/2;
            for(r;r>0;r--)
            {
                if(is_prime(n+r)==false || is_prime(n+r+r)==false)
                    continue;
                int n2=n+r;
                int n3=n2+r;
                if(perm(n,n2)==true && perm(n,n3)==true)
                {
                    //Second chain
                    cout << "Number: " << n << endl;
                    cout << "Liczba2: " << n2 << endl;
                    cout << "Liczba3: " << n3 << endl;
                    cout << "Ciag: " << n << n2 << n3 << endl << endl;
                }
            }
        }
    }
}

