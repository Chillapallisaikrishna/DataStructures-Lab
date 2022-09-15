#include<stdio.h>
#include<ctype.h>
#include<string.h>

char stk[20];
int top=-1;

void push(char c)
{
	stk[++top]=c;
}


char pop()
{
	return(stk[top--]);
}

int priority(char c)
{
	if(c=='^'|| c=='&' || c=='|')
		return 3;
	else if (c=='/'|| c=='*' || c=='%')
		return 2;
	else if(c=='+' || c=='-')
		return 1;
	else
		return 0;
}


main()
{
	char in[50],post[50],ch;
	int i,j,l;

	printf("Enter the string :");
	gets(in);

	l=strlen(in);
	j=0;

	for(i=0;i<l;i++)
	{
		if(isalpha(in[i]))
				post[j++]=in[i];
		else
		{
			if(in[i]=='(')
					push(in[i]);
			else if(in[i]==')')
					while((ch=pop())!='(')
						post[j++]=ch;
			else
			{
				while(priority(in[i])<=priority(stk[top]))
					post[j++]=pop();
				push(in[i]);
			}
		}
	}
		while(top!=-1)
			post[j++]=pop();

		post[j]='\0';

        printf("\n equivalent infix to postfix is:%s",post);

}
