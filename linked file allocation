#include <stdio.h>
#include <stdbool.h>

#define MAX_BLOCKS 100

bool allocated[MAX_BLOCKS] = { false };

void addFile() {
    int numBlocks, startBlock;
    printf("Enter the number of blocks to be allocated and starting block:\n");
    scanf("%d %d", &numBlocks, &startBlock);

    int count = 0, currentBlock = startBlock;

    while (count < numBlocks) {
        if (!allocated[currentBlock]) {
            allocated[currentBlock] = true;
            printf("bno: %d ---->1\n", currentBlock);
            count++;
        } else {
            printf("bno: %d is already allocated. Trying next block.\n", currentBlock);
        }
        currentBlock++;
    }
}

int main() {
    int numAlreadyAllocated;
    printf("Enter the number of blocks which are already allocated: ");
    scanf("%d", &numAlreadyAllocated);

    printf("Enter the blocks which are already allocated: ");
    for (int i = 0; i < numAlreadyAllocated; i++) {
        int block;
        scanf("%d", &block);
        allocated[block] = true;
    }

    int choice;
    while (1) {
        printf("1. add file 2. exit\n");
        scanf("%d", &choice);
        if (choice == 2) {
            break;
        } else if (choice == 1) {
            addFile();
        } else {
            printf("Invalid choice. Try again.\n");
        }
    }

    return 0;
}
