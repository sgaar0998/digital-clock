//# digital-clock
//A simple clock in consol using c++.
///////////////////////////////////////////////////////////////////////////////////////////

#include <iostream>
#include <windows.h>

using namespace std;

int main()
{
    int h,m,s;

    int a=0;

    while(a==0)
    {
       cout<< "insert initial value of Hr min ans sec."<<endl;
       cin>>h;cin>>m;cin>>s;
       if(h<24&&m<60&&s<60)
       {
           a=1;
       }
    }

  while(a==1)
  {
      system("cls");
   cout<<h<<":"<<m<<":"<<s<<endl;

    Sleep(1000);
    s++;
    if(s>59)
    {
      s=0;m++;
      if(m>59)
      {
         m=0;h++;
         if(h>23)
         {
             h=0;
         }

      }

    }

  }
    return 0;
}
