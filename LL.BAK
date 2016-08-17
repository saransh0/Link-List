#include<stdio.h>
#include<stdlib.h>
#include<conio.h>

struct node
{
  int data;
  struct node* next;
};
struct node* head=NULL;
void insert(int,int);
void print();
void del(int);
void rev();
void revrec(struct node*);
void precf(struct node*);
void search(int);

void main()
{
  int c,x,d,p,s;
  clrscr();
  printf("\t\t\t________________________\n");
  printf("\t\t\t|WELCOME TO LINKED LIST|");
  printf("\n\t\t\t|______________________|\n");
  getch();
  clrscr();
  while(1)
  {
    clrscr();
    printf("Enter your choice\n");
    printf("1. To insert\n");
    printf("2. To delete\n");
    printf("3. To print\n");
    printf("4. To reverse list\n");
    printf("5. To search an element\n");
    printf("6. Print using recursion\n");
    printf("7. Reversing list using recursion\n");
    printf("8. To exit\n");
    scanf("%d",&c);

    switch(c)
    {
      case 1:
	    {
	      printf("Enter the number and its position you want to enter\n");
	      scanf("%d%d",&x,&p);
	      insert(x,p);
	      break;
	    }
      case 2:
	    {
	      printf("Enter the position of the element you want to enter\n");
	      scanf("%d",&d);
	      del(d);
	      break;
	    }
      case 3:
	    {
	      print();
	      getch();
	      break;
	    }
      case 4:
	    {
	      rev();
	      print();
	      getch();
	      break;
	    }
      case 5:
	    {
	       printf("Enter the element to search\n");
	       scanf("%d",&s);
	       search(s);
	       getch();
	       break;
	     }
       case 6:
	     {
	       precf(head);
	       getch();
	       break;
	     }
       case 7:
	     {
	       revrec(head);
	       print();
	       getch();
	       break;
	     }
       case 8:
	     {
	       exit(0);
	     }
     default:
	    {
	      printf("Invalid choice\n");
	      break;
	    }

    }

  }

}

void insert(int x,int p)
{
  struct node* temp=(struct node*)malloc(sizeof(struct node));
  temp->data=x;
  temp->next=NULL;
  if(p==1)
  {
    temp->next=head;
    head=temp;
    return;
  }
  struct node* t=head;
  for(int i=0;i<p-2;i++)
  {
    t=t->next;
  }
  temp->next=t->next;
  t->next=temp;
}

void del(int d)
{
 struct node* t=head;
 if(d==1)
 {
   head=t->next;
   delete t;
   return;
 }
 for(int i=0;i<d-2;i++)
 {
   t=t->next;
 }
 struct node* temp=t->next;
 t->next=temp->next;
 delete temp;
}

void print()
{
 struct node* temp=head;
 printf("List is: ");
 while(temp!=NULL)
 {
   printf("%d ",temp->data);
   temp=temp->next;
 }
 printf("\n");
}

void rev()
{

  struct node *current,*next,*prev;
  current=head;
  prev=NULL;
  while(current!=NULL)
  {
    next=current->next;
    current->next=prev;
    prev=current;
    current=next;
  }
  head=prev;
}

void search(int s)
{
  struct node* temp=head;
  int c=0;
  while(temp!=NULL)
  {
   if(temp->data==s)
   {
     printf("Element is there!\n");
     c++;
     break;
   }
   temp=temp->next;
  }
  if(c==0)
  printf("Element not founded\n");
}

void precf(struct node* p)
{
  if(p==NULL)
  {
    return;
  }
  printf("%d ",p->data);
  precf(p->next);
}

void revrec(struct node* p)
{
  if(p->next==NULL)
  {
    head=p;
    return;
  }
  revrec(p->next);
  struct node* q=p->next;
  q->next=p;
  p->next=NULL;
}