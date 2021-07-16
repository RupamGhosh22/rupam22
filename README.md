#include<stdio.h>
int main(){
	
	int m,n,o,p,i,j,k;
	printf("Enter the number of rows & columns respectively of the First Matrix:\n");
	scanf("%d\t%d",&m,&n);
	int a[m][n];
	printf("Enter the First matrix of order: %d * %d :\n",m,n);
	for(i=0;i<m;i++){
		for(j=0;j<n;j++){
			scanf("%d",&a[i][j]);
		}
	}
    printf("Enter the number of rows & columns respectively of the Second Matrix:\n");
	scanf("%d\t%d",&o,&p);
	int b[o][p];
	printf("Enter the First matrix of order: %d * %d :\n",o,p);
	for(i=0;i<o;i++){
		for(j=0;j<p;j++){
			scanf("%d",&b[i][j]);
		}
	}
	if(n!=o){
		printf("This matrix multiplication is not possible\n");
	}
	else {
		int sum=0,c[m][p];
		for(i=0;i<m;i++){
			for(j=0;j<p;j++){
				for(k=0;k<o;k++){
				sum += a[i][k]*b[k][j];
		        }
		        c[i][j]=sum;
		        sum=0;
			}
		}
	    printf("The resultant matrix is of order %d * %d and it is:\n",m,p);
	    for(i=0;i<m;i++){
	    	for(j=0;j<p;j++){
	    		printf("%d\t",c[i][j]);
			}
			printf("\n\n");
		}
	}
	return 0;
}
