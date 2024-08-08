#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#define MAX_FILES 10
struct File
{
    char name[20];
    int startBlock;
    int length;
};
struct File files[MAX_FILES];
int fileCount = 0;

void addFile() 
{
    if (fileCount >= MAX_FILES) 
    {
        printf("File limit reached.\n");
        return;
    }

    struct File newFile;
    printf("Enter the name of the file %d: ", fileCount + 1);
    scanf("%s", newFile.name);
    printf("Enter the start block of the file %d: ", fileCount + 1);
    scanf("%d", &newFile.startBlock);
    printf("Enter the length of the file %d: ", fileCount + 1);
    scanf("%d", &newFile.length);

    files[fileCount++] = newFile;
}

void displayFileAllocationTable() {
    //printf("\nFile Allocation Table\n");
    printf("\n");
    for (int i = 0; i < fileCount; i++) {
        printf("File Name : %s\n", files[i].name);
        printf("Start Block : %d\n",files[i].startBlock);
        printf("Length : %d\n",files[i].length);
        printf("The file is allocated from block %d to block %d(%d blocks)",files[i].startBlock,files[i].startBlock+files[i].length-1,files[i].length);
        printf("\n\n");
    }
}

int main() {
    int numFiles;
    printf("Enter the number of files to be allocated: ");
    scanf("%d", &numFiles);

    for (int i = 0; i < numFiles; i++) {
        addFile();
    }

    displayFileAllocationTable();

    return 0;
}
