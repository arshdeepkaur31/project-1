
#include <iostream>
#include <string>


using namespace std;


int main ()
{
    int  option;
    string en;
    string cp="";
    string str="abcdefghijklmnopqrstuvwxyz";
    string decryption1;
    int shift;
    cout << "enter 1 for encryption and 2 for decryption \n";
    cin >>  option;

    if (option == 1)
    {
        cout << "enter string to encrypt \n";
        cin>>en;
        cout << "Value for Shift: \n";
        cin>>shift;
            for(int i=0;i<en.length();i++)
    {
        for( int j=0;j<26;j++)
        {
            if(en[i]==str[j])
            {
                if((j+shift)>25)
                {
                    int t=(j+shift-1)-25;
                    cp+=str[t];
                }
                
                else
                {
                    cp+=str[j+shift];
                }
            }
  
        }
       
    }
       cout<<"Encrypted string is : "<<cp;

        
        
    }
cp="";
    if (option == 2)
    {
        cout << "What do you want to decrypt \n";
        cin>>en;
        cout << "Value for Shift: \n";
        cin>>shift;
     for(int k=0;k<en.length();k++)
    {   // cout<<"\ns2 : "<<s2[k];
        for(int l=0;l<26;l++)
        {
            if(en[k]==str[l])
            {
                if(l-shift<0)
                {
                    int t=(l-shift)-(2*(l-shift));
                    cp+=str[26-t];
                }
                 else
                {
                    cp+=str[l-shift];
                }
                               
                                 

            }
            
        }
    }
    cout<<"Decrypted string is : "<<cp;

 
 
    }
    return 0;
}
