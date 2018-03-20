# my-good-teacher-work
#include<stdio.h>
 
int main()
{
    int i,j,k;
    printf("\n");
    for(i=1;i<5;i++) { // 以下为三重循环
        for(j=1;j<5;j++) {
            for (k=1;k<5;k++) { // 确保i、j、k三位互不相同
                if (i!=k&&i!=j&&j!=k) { 
                    printf("%d,%d,%d\n",i,j,k);
                }
            }
        }
    }
}

#include<stdio.h>
int main()
{
    double i;
    double bonus1,bonus2,bonus4,bonus6,bonus10,bonus;
    printf("你的净利润是：\n");
    scanf("%lf",&i);
    bonus1=100000*0.1;
    bonus2=bonus1+100000*0.075;
    bonus4=bonus2+200000*0.05;
    bonus6=bonus4+200000*0.03;
    bonus10=bonus6+400000*0.015;
    if(i<=100000) {
        bonus=i*0.1;
    } else if(i<=200000) {
        bonus=bonus1+(i-100000)*0.075;
    } else if(i<=400000) {
        bonus=bonus2+(i-200000)*0.05;
    } else if(i<=600000) {
        bonus=bonus4+(i-400000)*0.03;
    } else if(i<=1000000) {
        bonus=bonus6+(i-600000)*0.015;
    } else if(i>1000000) {
        bonus=bonus10+(i-1000000)*0.01;
    }
    printf("提成为：bonus=%lf",bonus);
 
    printf("\n");
}

#include <stdio.h>
 
int main (void)
{
    int  i, j, m, n, x;
    for (i = 1; i < 168 / 2 + 1; i++)
    {
        if (168 % i == 0)
        {
            j = 168 / i;
            if ( i > j && (i + j) % 2 == 0 && (i - j) % 2 == 0)
            {
                m = (i + j) / 2;
                n = (i - j) / 2;
                x = n * n - 100;
                printf ("%d + 100 = %d * %d\n", x, n, n);
                printf ("%d + 268 = %d * %d\n", x, m, m);
            }
        }
    }
    return 0;
}

#include <stdio.h>
int main()
{
    int day,month,year,sum,leap;
    printf("\n请输入年、月、日，格式为：年,月,日（2015,12,10）\n");
    scanf("%d,%d,%d",&year,&month,&day);  // 格式为：2015,12,10
    switch(month) // 先计算某月以前月份的总天数
    {
        case 1:sum=0;break;
        case 2:sum=31;break;
        case 3:sum=59;break;
        case 4:sum=90;break;
        case 5:sum=120;break;
        case 6:sum=151;break;
        case 7:sum=181;break;
        case 8:sum=212;break;
        case 9:sum=243;break;
        case 10:sum=273;break;
        case 11:sum=304;break;
        case 12:sum=334;break;
        default:printf("data error");break;
    }
    sum=sum+day; // 再加上某天的天数
    if(year%400==0||(year%4==0&&year%100!=0)) {// 判断是不是闰年
        leap=1;
    } else {
       leap=0;
    }
    if(leap==1&&month>2) { // *如果是闰年且月份大于2,总天数应该加一天
        sum++;
    }
    printf("这是这一年的第 %d 天。",sum);
    printf("\n");
}
//  Created by www.runoob.com on 15/11/9.
//  Copyright © 2015年 菜鸟教程. All rights reserved.
//
 
#include <stdio.h>
 
int main()
{
    int x,y,z,t;
    printf("\n请输入三个数字:\n");
    scanf("%d%d%d",&x,&y,&z);
    if (x>y) { /*交换x,y的值*/
        t=x;x=y;y=t;
    }
    if(x>z) { /*交换x,z的值*/
        t=z;z=x;x=t;
    }
    if(y>z) { /*交换z,y的值*/
        t=y;y=z;z=t;
    }
    printf("从小到大排序: %d %d %d\n",x,y,z);
}
