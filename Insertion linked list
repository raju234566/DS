#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node* next;
};

void insert(struct Node** head_ref, int new_data) {
    struct Node* new_Node = (struct Node*)malloc(sizeof(struct Node));
    new_Node->data = new_data;
    new_Node->next = *head_ref;
    *head_ref = new_Node;
}
  void insertatend(struct Node** head_ref, int new_data){
    struct Node* new_node = (struct Node*)malloc(sizeof(struct Node));
    struct Node* last = *head_ref;
    new_node->data = new_data;
    new_node->next = NULL;
    
    struct Node*temp = *head_ref;
    while(temp->next!= NULL){
      temp = temp->next;
    }
     temp->next = new_node;
  }

void printList(struct Node* node) {
    while (node != NULL) {
        printf("%d -> ", node->data);
        node = node->next;
    }
    printf("NULL\n");
}

int main() {
    struct Node* head = NULL;

    insert(&head, 10);
    insertatend(&head,70);
    insert(&head, 20);
    insert(&head, 30);
      insertatend(&head,70);
        insertatend(&head,80);

    printf("Linked list: ");
    printList(head);

    return 0;
}
