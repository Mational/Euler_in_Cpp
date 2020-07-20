#include <iostream>
#include <vector>

using namespace std;

bool is_prime(long long iNumber)
{
    for(int divider=2;divider*divider<=iNumber;divider++)
        if(iNumber%divider==0)
            return false;
    return true;
}

void fill_in(vector<int>&iNumbers)
{
    for(int number=2;number<10000;number++)
        if(is_prime(number)==true)
            iNumbers.push_back(number);
    return;
}

bool check(int candidate, int concat[], int limit)
{
    for(int i=0;i<limit;i++)
    {
        unsigned long long num1 = stoll( to_string(candidate) + to_string(concat[i]) );
        unsigned long long num2 = stoll( to_string(concat[i]) + to_string(candidate) );
        if( is_prime(num1)==false || is_prime(num2)==false )
            return false;
    }
    return true;
}

void program(vector<int>&iNumbers)
{
    int chain_length=5;
    int concatenate[chain_length];
    int concat_pos[chain_length];
    for(int j=0;j<chain_length;j++)
    {
        concatenate[j]=0;
        concat_pos[j]=0;
    }
    int pos=0;
    for(int i=1;i<iNumbers.size();i++)
    {
        if(pos==0)
        {
            concatenate[pos]=iNumbers[i];
            concat_pos[pos]=i;
            pos++;
        }

        if( check(iNumbers[i], concatenate, pos)==true )
        {
            concatenate[pos]=iNumbers[i];
            concat_pos[pos]=i;
            pos++;
            if(pos==chain_length)
            {
                long long sum=0;
                vector<int> t_sum;

                for(int j=0;j<chain_length;j++)
                    sum+=concatenate[j];

                t_sum.push_back(sum);
                cout << "Sum: " << sum << endl;
                for(int j=0;j<pos;j++)
                    cout << concatenate[j] << "  ";
                cout << endl;

                return;
            }
        }
        else if(iNumbers.size()-i==1 && pos<5 )
        {
            pos--;
            i=concat_pos[pos]+1;
        }
    }
    return;
}

int main()
{
    vector<int> numbers;
    fill_in(numbers);
    program(numbers);
    return 0;
}
