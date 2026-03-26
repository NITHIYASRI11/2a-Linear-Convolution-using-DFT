# EXPT 2a: LINEAR CONVOLUTION-USING-DFT

## AIM
To perform and verify linear convolution operation of two given sequences using SCILAB.

## APPARATUS REQUIRED
PC installed with SCILAB

## PROGRAM:
LINEAR CONVOLUTION

```
clc;
clear;
x=[3,2,1,1];
h=[1,2,3];
m=length(x);
n=length(h);
a=0:1:m-1;
b=0:1:n-1;
subplot(3,1,1);
plot2d3(a,x);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Input Signal X');
subplot(3,1,2);
plot2d3(b,h);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Impulse Signal h');
for i=1:n+m-1
    conv_sum=0;
    for j=1:i
        if(((i-j+1)<=n)&(j<=m))
            conv_sum=conv_sum+x(j)*h(i-j+1);
        end;
        y(i)=conv_sum;
   end;
end;
disp(y,'Convolution Sum using Direct Formula Method=')
subplot(3,1,3);
plot2d3(y)
title('Graphical Representation of Input Signal y');


```
## CALCULATIONS:

![WhatsApp Image 2026-03-25 at 20 36 38](https://github.com/user-attachments/assets/849d15e9-4144-423b-8bda-1880b15a2e01)

![WhatsApp Image 2026-03-25 at 20 37 09](https://github.com/user-attachments/assets/bcb5eb50-0f23-4669-90e5-2dda0c443108)

![WhatsApp Image 2026-03-25 at 20 38 30](https://github.com/user-attachments/assets/344d1451-ce59-4870-9ac7-14b3099a89af)

## SAMPLE OUTPUT:
<img width="597" height="568" alt="image" src="https://github.com/user-attachments/assets/15c3dea5-c335-462d-bb83-ed7b8bed1439" />





## RESULT:
Thus, the linear convolution of the two given sequences were performed and its result was verified.
