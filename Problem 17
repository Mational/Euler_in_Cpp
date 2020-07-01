#include <iostream>

using namespace std;

int main()
{
    int dl=0;
    string one[10]={"one","two","three","four","five","six","seven","eight","nine"};
    string ten[11]={"ten","eleven","twelve","thirteen","fourteen","fifteen","sixteen","seventeen","eighteen","nineteen"};
    string twenty[9]={"twenty","thirty","forty","fifty","sixty","seventy","eighty","ninety"};
    string a="and";
    string h="hundred";
    string t="thousand";

    for(int i=0;i<9;i++)
    {
        //cout << one[i] << endl;
        dl+=one[i].size();
    }

    for(int i=0;i<10;i++)
    {
        //cout << ten[i] << endl;
        dl+=ten[i].size();
    }

    for(int i=0;i<8;i++)
    {
        //cout << twenty[i] << endl;
        dl+=twenty[i].size();
        for(int j=0;j<9;j++)
        {
            //cout << twenty[i] << " " << one[j] << endl;
            dl+=twenty[i].size()+one[j].size();
        }
    }

    for(int i=0;i<9;i++)
    {
        //cout << one[i] << " " << h << endl;
        dl+=one[i].size()+h.size();
        for(int j=0;j<9;j++)
        {
            //cout << one[i] << " " << h << " " << a << " " << one[j] << endl;
            dl+=one[i].size()+h.size()+a.size()+one[j].size();
        }
        for(int j=0;j<10;j++)
        {
            //cout << one[i] << " " << h << " " << a << " " << ten[j] << endl;
            dl+=one[i].size()+h.size()+a.size()+ten[j].size();
        }
        for(int j=0;j<8;j++)
        {
            //cout << one[i] << " " << h << " " << a << " " << twenty[j] << endl;
            dl+=one[i].size()+h.size()+a.size()+twenty[j].size();
            for(int k=0;k<9;k++)
            {
                //cout << one[i] << " " << h << " " << a << " " << twenty[j] << " " << one[k] << endl;
                dl+=one[i].size()+h.size()+a.size()+twenty[j].size()+one[k].size();
            }
        }
    }

    //cout << one[0] << " " << t << endl;
    dl+=one[0].size()+t.size();
    cout << "\n\nIlosc liter: " << dl << endl;
    return 0;
}
