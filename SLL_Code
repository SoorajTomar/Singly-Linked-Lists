#include <stdio.h>
#include <stdlib.h>
struct node{
  int data;
  struct node *next;
};
typedef struct node sn;
sn *head;
sn* insertb(sn* h,int val){
    sn *t=(sn*)malloc(sizeof(sn));
    t->data=val;
    t->next=h;
    h=t;
    return h;
}
sn* inserte(sn* h,int val){
    sn *t=(sn*)malloc(sizeof(sn));
    t->data=val;
    sn* p=h;
    while(p->next!=NULL){
        p=p->next;
    }
    t->next=NULL;
    p->next=t;
    return h;
}
sn* insertp(sn* h,int val,int pos){
    sn *t=(sn*)malloc(sizeof(sn));
    t->data=val;
    sn* p=h;
    int i;
    for(i=0;i<pos-1;i++)p=p->next;
    t->next=p->next;
    p->next=t;
    return h;
}
sn* delb(sn* h){
    sn* x=h;
    h=h->next;
    free(x);
    return h;
}
sn* dele(sn* h){
    sn* p=h;
    while(p->next->next!=NULL)p=p->next;
    sn* x=p->next;
    p->next=NULL;
    free(x);
    return h;
}
sn* delp(sn* h,int pos){
    sn* p=h;
    int i;
    for(i=0;i<pos-1;i++)p=p->next;
    sn* x=p->next;
    p->next=p->next->next;
    free(x);
    return h;
}
void print(sn* h){
    sn* p=h;
    while(p){
        printf("%d->",p->data);
        p=p->next;
    }
}
int main()
{
    int i;
    for(i=0;i<5;i++)
    head=insertb(head,i);
    print(head);
    printf("\n");
    head=inserte(head,45);
    print(head);
    printf("\n");
    head=insertp(head,97,2);
    print(head);
    printf("\n");
    head=delb(head);
    print(head);
    printf("\n");
    head=dele(head);
    print(head);
    printf("\n");
    head=delp(head,2);
    print(head);
    printf("\n");
    return 0;
}
