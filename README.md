***** CLICK RAW FOR BETTER VIEW ********

# linkedList-middle-value-for-odd-numbers-in-c
linkedList middle value for odd numbers in C

#include <stdio.h>
struct node{
    int data;
    struct node* next;
    
};

void midval(struct node* fptr , struct node* sptr){
    while(fptr->next!=NULL){
        fptr=fptr->next->next;
        sptr=sptr->next;
        
    }
    printf("\nmid value is = %d",sptr->data);
    
}



void display(struct node* ptr){
    while(ptr!=NULL){
        printf("%d",ptr->data);
        ptr=ptr->next;
        
    }
    
    
}


int main()
{
    struct node* head, *second , *third , *fourth , *fifth , *sixth , *seven;
    head= (struct node *)malloc(sizeof(struct  node));
    second= (struct node *)malloc(sizeof(struct  node));
    third= (struct node *)malloc(sizeof(struct  node));
    fourth= (struct node *)malloc(sizeof(struct  node));
    fifth= (struct node *)malloc(sizeof(struct  node));
    sixth= (struct node *)malloc(sizeof(struct  node));
    seven= (struct node *)malloc(sizeof(struct  node));
    
    
    head->data=1;
    head->next=second;
    
    second->data=2;
    second->next=third;
    
    third->data=3;
    third->next=fourth;
    
    fourth->data=4;
    fourth->next=fifth;
    
    fifth->data=5;
    fifth->next=sixth;
    
    sixth->data=6;
    sixth->next=seven;
    
    seven->data=7;
    seven->next=NULL;
    
    display(head);  
    midval(head , head);
    
    


    
    return 0;
}
