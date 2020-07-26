#include <iostream>
#include <vector>
#include <cstdlib>

using namespace std;

int chain_n[6]={0,0,0,0,0,0};
string chain_t[6]={"","","","","",""};

void fill_in(vector<int>&nums,vector<string>&type,int num)
{
    int number;
    for(int i=num;i<10000;i++)
    {
        start:

        // P8,19 is first octagonals number which is 4-digit number
        for(int n=19;n*((3*n)-2)<10000;n++)
        {
            number=n*((3*n)-2);
            if(number==i)
            {
                nums.push_back(i);
                type.push_back("o");
                i++;
                goto start;
            }
            else if(number>i)
                break;
        }

        // P7,21 is first heptagonal number which is 4-digit number
        for(int n=21;n*(((5*n)-3))/2<10000;n++)
        {
            number=n*(((5*n)-3))/2;
            if(number==i)
            {
                nums.push_back(i);
                type.push_back("hept");
                i++;
                goto start;
            }
            else if(number>i)
                break;
        }

        // P6,23 is first hexagonal number which is 4-digit number
        for(int n=23;n*((2*n)-1)<10000;n++)
        {
            number=n*((2*n)-1);
            if(number==i)
            {
                nums.push_back(i);
                type.push_back("hex");
                i++;
                goto start;
            }
            else if(number>i)
                break;
        }

        // P5,26 is first pentagonal number which is 4-digit number
        for(int n=26;(n*((3*n)-1))/2<10000;n++)
        {
            number=(n*((3*n)-1))/2;
            if(number==i)
            {
                nums.push_back(i);
                type.push_back("p");
                i++;
                goto start;
            }
            else if(number>i)
                break;
        }

        // P4,32 is first square number which is 4-digit number
        for(int n=32;n*n<10000;n++)
        {
            number=n*n;
            if(number==i)
            {
                nums.push_back(i);
                type.push_back("s");
                i++;
                goto start;
            }
            else if(number>i)
                break;
        }

        // P3,45 is first triangle number which is 4-digit number
        for(int n=45;n*(n+1)/2<10000;n++)
        {
            number=n*(n+1)/2;
            if(number==i)
            {
                nums.push_back(i);
                type.push_back("t");
                i++;
                goto start;
            }
            else if(number>i)
                break;
        }
    }
    return;
}

bool check(int num1, int num2)
{
    string n1=to_string(num1);
    string n2=to_string(num2);
    if(n1[2]==n2[0] && n1[3]==n2[1])
        return true;
    return false;
}

bool if_not_repeat(int num, int t[], int t_size)
{
    for(int i=0;i<t_size;i++)
        if(t[i]==num)
            return false;
    return true;
}

bool if_not_string_repeat(string text, string t[],int t_size)
{
    for(int i=0;i<t_size;i++)
        if(t[i]==text)
            return false;
    return true;
}

void program(vector<int>&n, vector<string>&t, int position)
{
    for(int c=0;c<n.size();c++)
    {
        if(position==0)
        {
            chain_n[position]=n[c];
            chain_t[position]=t[c];
            program(n, t, position+1);
        }
        if(position==5)
        {
            if( check(chain_n[position-1],n[c])==true
                && check(n[c],chain_n[0]) == true
                && if_not_repeat(n[c],chain_n,position) == true
                && if_not_string_repeat(t[c],chain_t,position) == true)
                {
                    chain_n[position]=n[c];
                    chain_t[position]=t[c];

                    int sum=0;
                    for(int i=0; i<6;i++)
                    {
                        cout << chain_n[i] << "  ";
                        sum+=chain_n[i];
                    }
                    cout << "\n\nSum: " << sum << endl;
                    exit(0);
                }
        }
        else
        {
            if( check(chain_n[position-1],n[c])==true
                && if_not_repeat(n[c],chain_n,position) == true
                && if_not_string_repeat(t[c],chain_t,position) == true)
            {
                chain_n[position]=n[c];
                chain_t[position]=t[c];
                program(n, t, position+1);
            }
        }
    }
    return;
}

int main()
{
    vector<int> numbers;
    vector<string> types;
    fill_in(numbers,types,1001);
    program(numbers,types, 0);
}
