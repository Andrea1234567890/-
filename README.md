//随机产生n个元素的值，建立带表头结点的单链线性表L（头插法）
#include <stdio.h> 
void CreatListHead ( *L,int n)
{
	LinkList p;
	int i;
	srand(time(0));
	*L=(LinkList)malloc(sizeof(Node));
	(*L)->next=NULL;//先建立一个带头结点的单链表
	for(i=0;i<n;i++)
	{
		p=(LinkList)malloc(sizeof(Node));//生成新结点
		p->data=rand()%100+1;
		p->next=(*L)->next;
		(*L)->next=p;
	}
}
