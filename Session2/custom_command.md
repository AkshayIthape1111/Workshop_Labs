# Create Own Linux Command
## Step 1 :- 
Write the particular program in scripting lang, low level lang or in high level lang <br/>
I am going to select c programming lang for create custom command <br/>
Create the file called love.c and paste the following code in it .
```
#include<stdio.h>
int main()
{
printf("Love is not find");
return 0;
}

```
Compile that program using gcc 
```
gcc love.c
``` 
Rename that file name a.out to love
```
mv a.out love
```
## Stepp 2 :-
Put that particular 'love' binary file to the proper location so that execute as a command
```
cp love /usr/bin
chmod a+x /bin/love
```
## You Create Your Custom Command
```
love
```
