#include <iostream>
#include <stdio.h>
#include <windows.h>

using namespace std;

class Time
{
private:
    int birth_year,birth_month,birth_day;
    int current_year,current_month,current_day;
public:
    Time(int y,int m,int d,int cy,int cm,int cd)
    {
        birth_year=y;
        birth_month=m;
        birth_day=d;
        current_year=cy;
        current_month=cm;
        current_day=cd;
    }

    void calcuteTime();
};

int main()
{
    int yearOfBirth,monthOfBirth,dayOfBirth,yearOfCurrent,monthOfCurrent,dayOfCurrent;
    cout<<"还记得您的出生年月日吗？";
    cin>>yearOfBirth>>monthOfBirth>>dayOfBirth;
    cout<<"现在是什么时候呢？";
    cin>>yearOfCurrent>>monthOfCurrent>>dayOfCurrent;
    Time tm(yearOfBirth,monthOfBirth,dayOfBirth,yearOfCurrent,monthOfCurrent,dayOfCurrent);
    tm.calcuteTime();
    return 0;
}

void Time::calcuteTime()
{
    int month[12]={31,28,31,30,31,30,31,31,30,31,30,31};
    int i=0,j=0,totalDay=0,daysOfCurrentYear=0,daysOfBirthYear=0,daysOfNowYear=0;

    // 计算当前年份还剩多少天
    for(i=0;i<current_month-1;i++)
    {
        daysOfCurrentYear+=month[i];
    }
    if(current_month>2)
    {
        if((current_year%4==0&&current_year%100!=0)||current_year%400==0)
            daysOfCurrentYear=daysOfCurrentYear+current_day+1;
    }
    else daysOfCurrentYear=daysOfCurrentYear+current_day;


    // 计算出生时本年还剩多少天
    for(i=0;i<birth_month-1;i++)
    {
        daysOfBirthYear=daysOfBirthYear+month[i];
    }
    if((birth_year%4==0&&birth_year%100!=0)||birth_year%400==0)
    {
        if(birth_month>2)
            daysOfBirthYear=366-(daysOfBirthYear+birth_day);
    }
    else
        daysOfBirthYear=365-(daysOfBirthYear+birth_day);

    // 计算出中间的天数
    for(j=birth_year;j<current_year;j++)
    {
        if((j%4==0&&j%100!=0)||j%400==0)
            daysOfNowYear=daysOfNowYear+366;
        else
            daysOfNowYear=daysOfNowYear+365;
    }

    // 总共的天数
    totalDay=daysOfCurrentYear+daysOfNowYear+daysOfBirthYear;

    cout<<endl;
    printf("您今年的时间进度：%d%%\n",(int)((daysOfCurrentYear*1.0/365)*100));
    Sleep(2*1000);

    cout<<'[';
    for(i=1;i<=(int)((daysOfCurrentYear*1.0/365)*100);i++)
        cout<<'>';
    for(j=(int)((daysOfCurrentYear*1.0/365)*100);j<99;j++)
        cout<<'_';
    cout<<"]";
    cout<<endl<<endl;;
    Sleep(3*1000);

    printf("根据WHO寿命均值76岁可知，您的人生进度已过了%d%%\n",(int)((totalDay*1.0/27056)*100));
    Sleep(2*1000);

    cout<<'[';
    for(i=1;i<=(int)((totalDay*1.0/27056)*100);i++)
        cout<<'>';
    for(j=(int)((totalDay*1.0/27056)*100)+1;j<=99;j++)
        cout<<'_';
    cout<<']';
    cout<<endl<<endl;

    Sleep(4*1000);
    printf("所以呢，你该做点什么？\n");
    Sleep(3*1000);
    printf("漠视它，选择继续娱乐至死？还是...\n");
    Sleep(3*1000);
    printf("选择做点有意义的事\n");
    Sleep(2*1000);
    printf("无论你选择什么\n");
    Sleep(2*1000);
    printf("请珍视它\n");
    Sleep(2*1000);
    printf("学点有用的东西\n");
    Sleep(3*1000);
    printf("做点有意义的事\n");
    Sleep(3*1000);
    printf("花点时间提升自己\n");
    Sleep(2*1000);
    printf("学习\n");
    Sleep(3*1000);
    printf("亦或是选择一个人远足\n");
    Sleep(2*1000);
    printf("这都可以\n");
    Sleep(2*1000);
    printf("总之\n");
    Sleep(3*1000);
    printf("做点有意义的事\n");
    Sleep(3*1000);
    printf("勿让人生虚度\n");
    Sleep(2*1000);
    printf("时间至上\n");
}
