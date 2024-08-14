//# Calculator
//solve your maths problems!!
#include<iostream>
using namespace std;
int factorial(int n){
    if(n<=1){ 
        return 1;}
    return n*factorial(n-1);
}
double ln(double X){
    
double s=0;
 if(X<=2){double t=X-1;
 for ( int k=1; k<1000; k++){
    s= s+ t;
    t= ((-1)*t*(X-1)*(k))/(k+1);}
    return s;
}
else if (X>2){double t= (X-1)/(X+1);
for( int i=0; i<1000; i++)
{s= s+ t/(2*i +1);
t= (t*(X-1)*(X-1))/((X+1)*(X+1));
}
return 2*s; }
}

int main(){

    int q;
cout<<"Choose the number to run your mathematical operation "<<endl;
cout<<"1. Addition          2. Subtraction \n3. Multiplication    4. Division \n5. Modulo            6. Greatest Common Divisor \n7. lnx               8. exp(x) \n9. n!               10. sinx \n11. cosx            12. tanx \n13. cosecx          14. secx \n15. cotx  "<<endl<<endl;
cin>>q;
double a,b;
int u; 
if(q==1)
{

cout<<"Enter first number"<<endl;
cin>>a;
cout<<"Enter second number"<<endl;
cin>>b;
cout<<"The sum of "<<a<<" and "<<b<<" is "<< (a+b)<<endl;}


else if(q==2) 
{cout<<"Enter first number"<<endl;
cin>>a;
cout<<"Enter second number"<<endl;
cin>>b;
cout<<"The difference of "<<a<<" and "<<b<<" is "<< (a-b)<<endl;
}

else if(q==3) 
{cout<<"Enter first number"<<endl;
cin>>a;
cout<<"Enter second number"<<endl;
cin>>b;
cout<<"The product of "<<a<<" and "<<b<<" is "<< (a*b)<<endl;}


else if(q==4) 
{cout<<"Enter first number"<<endl;
cin>>a;
cout<<"Enter second number"<<endl;
cin>>b;
cout<<"The value of "<<a<<"/"<<b<<" is "<< (a/b)<<endl;}


else if(q==5) 
{int A,B;
cout<<"Enter first number"<<endl;
cin>>A;
cout<<"Enter second number"<<endl;
cin>>B;
cout<<"The remainder when "<<A<<" is divided by "<<B<<" is "<< (A%B)<<endl;}

else if(q==6) 
{int C,D;
cout<<"Enter the two natural numbers "<<endl;
cin>>C>>D;

while( C%D !=0)
{ int r= C%D;
C=D;
D= r;}

cout<<"The GCD is "<<D<<endl;}


else if(q==7)
{double X;
cout<<"Enter value of x"<<endl;
cin>>X;
cout<<double(ln(X)); } 


else if (q==8) 
{double M;
double SUM, T;
cout<<"to find value of exp(x) enter the value of x"<<endl;
cin>>M;
 SUM=0, T=1;
for(int k=1; k<100;k++){
    SUM= SUM+T;
    T= T*M/k;
};
cout<< SUM ;}

else if(q==9) 
{

int n;
    cout<<"find the value of n! \nenter the value of n "<<endl;
    cin>>n;
    cout<<"the value of "<<n<<"! is "<<factorial(n);
}

else if(q==10){
  double x;
cout<<"calculating the value of sinx for x = ? \n Enter the value of x in radian"<<endl;
cin>>x;
double s=0, t=x;
for(int k=1; k<10; k++){
    s= s+t;
    t= -(t*x*x)/(2*k)/((2*k)+1);
};
cout<<s;  
}
else if(q==11)
{double x;
cout<<"to calculate the value of cosine x. \n Enter the value of x in radian"<<endl;
cin>>x;
double s=0,t=1;

for(int k=1;k<100; k++){
s= s+t;
t= -(t*x*x)/(2*k)/((2*k)-1);
};
cout<<s;}
else if (q==12)
{
    double y;
cout<<"enter the angle x in radian"<<endl;
cin>>y;
double sum=0, T=y;
for(int k=1; k<10; k++){
    sum= sum+T;
    T= -(T*y*y)/(2*k)/((2*k)+1);
};
    

double s=0,t=1;

for(int k=1;k<100; k++){
s= s+t;
t= -(t*y*y)/(2*k)/((2*k)-1);
};
cout<<"tanx = "<<sum/s;
}
else if(q==13){
    double x;
cout<<" Enter the value of x in radian"<<endl;
cin>>x;
double s=0, t=x;
for(int k=1; k<10; k++){
    s= s+t;
    t= -(t*x*x)/(2*k)/((2*k)+1);
};
cout<<(1/s);  
}
else if(q==14)
{double x;
cout<<"Enter the value of x in radian"<<endl;
cin>>x;
double s=0,t=1;
for(int k=1;k<100; k++){
s= s+t;
t= -(t*x*x)/(2*k)/((2*k)-1);
};
cout<<1/s;}

else if (q==15)
{    double y;
cout<<" Enter the value of x in radian"<<endl;
cin>>y;
double sum=0, T=y;
for(int k=1; k<10; k++){
    sum= sum+T;
    T= -(T*y*y)/(2*k)/((2*k)+1);
};    
double s=0,t=1;
for(int k=1;k<100; k++){
s= s+t;
t= -(t*y*y)/(2*k)/((2*k)-1);
};
cout<<s/sum;}

return 0;
}
