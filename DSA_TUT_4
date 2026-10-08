#include <stdio.h>

struct student
{
    int roll;
    char name[20];
    float SGPA;
};

void create(struct student st[], int n)
{
    int i;

    for(i = 0; i < n; i++)
    {
        printf("\n--- Enter Student %d Data ---\n", i + 1);

        printf("Enter Roll No: ");
        scanf("%d", &st[i].roll);

        printf("Enter Name: ");
        scanf("%s", st[i].name);

        printf("Enter SGPA: ");
        scanf("%f", &st[i].SGPA);
    }
}

void display(struct student st[], int n)
{
    int i;

    printf("\n\n========== STUDENT DETAILS ==========\n");

    for(i = 0; i < n; i++)
    {
        printf("\nStudent %d", i + 1);
        printf("\nRoll No : %d", st[i].roll);
        printf("\nName    : %s", st[i].name);
        printf("\nSGPA    : %.2f\n", st[i].SGPA);
    }

    printf("\n=====================================\n");
}

void modify(struct student st[], int n)
{
    int i, roll;

    printf("\nEnter Roll No to modify: ");
    scanf("%d", &roll);

    for(i = 0; i < n; i++)
    {
        if(st[i].roll == roll)
        {
            printf("Enter New Name: ");
            scanf("%s", st[i].name);

            printf("Enter New SGPA: ");
            scanf("%f", &st[i].SGPA);

            printf("Record Modified Successfully!\n");
            return;
        }
    }

    printf("Record Not Found!\n");
}

void search(struct student st[], int n)
{
    int i, roll;

    printf("\nEnter Roll No to search: ");
    scanf("%d", &roll);

    for(i = 0; i < n; i++)
    {
        if(st[i].roll == roll)
        {
            printf("\nRoll No : %d", st[i].roll);
            printf("\nName    : %s", st[i].name);
            printf("\nSGPA    : %.2f\n", st[i].SGPA);
            return;
        }
    }

    printf("Record Not Found!\n");
}

void sort(struct student st[], int n)
{
    int i, j;
    struct student temp;

    for(i = 0; i < n - 1; i++)
    {
        for(j = 0; j < n - i - 1; j++)
        {
            if(st[j].roll > st[j + 1].roll)
            {
                temp = st[j];
                st[j] = st[j + 1];
                st[j + 1] = temp;
            }
        }
    }

    printf("\nRecords Sorted Successfully!\n");
}

int main()
{
    struct student st[100];
    int n, choice;

    printf("Enter Number of Students: ");
    scanf("%d", &n);

    create(st, n);

    do
    {
        printf("\n\n========== STUDENT DATABASE ==========");
        printf("\n1. Display");
        printf("\n2. Modify");
        printf("\n3. Search");
        printf("\n4. Sort");
        printf("\n5. Exit");

        printf("\n\nEnter Choice: ");
        scanf("%d", &choice);

        switch(choice)
        {
            case 1:
                display(st, n);
                break;

            case 2:
                modify(st, n);
                break;

            case 3:
                search(st, n);
                break;

            case 4:
                sort(st, n);
                break;

            case 5:
                printf("\nProgram Ended.");
                break;

            default:
                printf("\nInvalid Choice!");
        }

    } while(choice != 5);

    return 0;
}
