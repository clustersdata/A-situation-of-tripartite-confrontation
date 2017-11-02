# A-situation-of-tripartite-confrontation

A situation of tripartite confrontation

Problem Description

MCA山中人才辈出，洞悉外界战火纷纷，山中各路豪杰决定出山拯救百姓于水火，曾以题数扫全场的威士忌，曾经高数九十九的天外来客，曾以一剑铸十年的亦纷菲，歃血为盟，盘踞全国各个要塞（简称全国赛）遇敌杀敌，遇佛杀佛，终于击退辽军，暂时平定外患，三人位置也处于稳态。

可惜辽誓不甘心，辽国征南大将军<耶律javac++>欲找出三人所在逐个击破，现在他发现威士忌的位置s,天外来客的位置u，不过很难探查到亦纷菲v所在何处，只能知道三人满足关系：


arctan(1/s) = arctan(1/u)+arctan(1/v)


注：(其中0 <= x <= 1)

定义 f(s, u, v) = v*u-s*u-s*v 的值 为<三足鼎立>


<耶律javac++>想计算<三足鼎立>的值

Input

首先输入一个t,表示有t组数据，跟着t行：

输入s, u (s <= 12^3, u <= 2^20 且 s, u, v > 0)

且s,u,v均为实数

Output

输出 v*u-s*u-s*v 的值，为了简单起见，如果是小数，直接取整


比如：答案是1.7 则输出 1

Sample Input

1 1 2

Sample Output

1

代码：

#include<stdio.h>

#include<math.h>


int main()

{

	int t;
  
	double s,u,v,ans;
  
	scanf("%d",&t);
  
	while(t--&&scanf("%lf%lf",&s,&u))
  
	{
  
		v = atan(1.0/s)-atan(1.0/u);
    
		v = 1.0/tan(v);
    
		ans = v*u-s*u-s*v;
    
		printf("%.0lf\n",ans);
    
	}
  
}
