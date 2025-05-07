#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node* next;
};


void insertAtBeginning(struct Node** head, int data) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = data;
    
    if (*head == NULL) {
        *head = newNode;
        newNode->next = *head;  
    } else {
        struct Node* temp = *head;
        while (temp->next != *head) {
            temp = temp->next;
        }
        temp->next = newNode;
        newNode->next = *head;
        *head = newNode;
    }
}


void insertAtEnd(struct Node** head, int data) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = data;
    
    if (*head == NULL) {
        *head = newNode;
        newNode->next = *head;  
    } else {
        struct Node* temp = *head;
        while (temp->next != *head) {
            temp = temp->next;
        }
        temp->next = newNode;
        newNode->next = *head;
    }
}

void insertAtPosition(struct Node** head, int data, int position) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = data;
    
    if (position == 0) {
        insertAtBeginning(head, data);
        return;
    }
    
    struct Node* temp = *head;
    int count = 0;
    while (count < position - 1 && temp->next != *head) {
        temp = temp->next;
        count++;
    }
    
    if (temp->next == *head) {
        printf("Position exceeds the length of the list\n");
    } else {
        newNode->next = temp->next;
        temp->next = newNode;
    }
}


void display(struct Node* head) {
    if (head == NULL) {
        printf("List is empty.\n");
        return;
    }
    
    struct Node* temp = head;
    do {
        printf("%d -> ", temp->data);
        temp = temp->next;
    } while (temp != head);
    
    printf("(head -> %d)\n", head->data); 
}

int main() {
    struct Node* head = NULL;
    
   
    insertAtBeginning(&head, 10);
    insertAtBeginning(&head, 20);
    
    
    insertAtEnd(&head, 30);
    insertAtEnd(&head, 40);
    

    insertAtPosition(&head, 25, 2);
    
    
    display(head);
    
    return 0;
}
