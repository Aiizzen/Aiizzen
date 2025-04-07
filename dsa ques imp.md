                              MY DSA JOURNEY QUES 
    
    
    SOURCE(SHRADDHA KHAPRA)
   ***********************************Hollow rectangle( Revision ques)**********************
    // int n = 4;
    // int m = 5;
    // // outer loop
    // for (int i = 1; i <= n; i++) {
    //   // inner loop
    //   for (int j = 1; j <= m; j++) {
    //     // cell->(i,j)
    //     if (i == 1 || j == 1 || i == n || j == m) {
    //       System.out.print("*");}
    //      else 
    //      {
    //       System.out.print(" ");}
    //     }

      
    //   System.out.println();
    // }


  // *************************INVERTED HALF PYRAMID ROTATED 180 DEGREE*******************
// int n = 4;
// // outer loop
// for(int i = 1; i<=n;i++){
//   //inner loop
//   for(int j = 1; j <=n-i; j++){
//   System.out.print(" ");  
//   }
//     int j;
//   //inner loop
//   for( j = 1; j<=i;j++){
//     System.out.print("*");
//   }
//   System.out.println();
//   }

/*********************FLOYDS TRIANGLE************* *( revesion question)
// int n =5;
// int number=1;
// for(int i = 1;i<=n;i++){
//   for(int j = 1;j<=i;j++){
// System.out.print(number+"  ");
// number ++;
//   }
//   System.out.println( );
// }

/***************PRINT A NUMBER PYRAMID****************
// int n =5;
// for(int i = 1;i<=n;i++){
//   for(int j =1; j<n-i;j++){
//     System.out.print(" ");
//   }
//   for(int j= 1;j<=i;j++){
//     System.out.print(i+" " );
//   }
//   System.out.println();
// }


/*****************PRINT A PALINDROMIC NUMBER PYRAMID*********
// int n=5;
// for(int i = 1;i<=n;i++){
//   for(int j = 1;j<=n-i;j++){
//     System.out.print(" ");
//   }
//   for(int j = i;j>=1;j--){
//     System.out.print(j);
//   }
 
    
//     for(int j = 2;j<=i;j++){
//       System.out.print(j);
//     }
//     System.out.println();
  
// }

//   }

// *******************PRINT BUTTERFLY PATTERN********************
// int n = 4;
// for(int i = 1; i<=n;i++){
//   for(int j = 1; j<=i;j++){
//     System.out.print("*");
//   }
//   int spaces = 2*(n-i);
//   for(int j = 1;j<=spaces;j++){
//     System.out.print(" ");
//   }
//   for(int j = 1;j<=i;j++){
//     System.out.print("*");
//   }
// System.out.println();
//  }

// for(int i = n; i>=1;i--){
//   for(int j = 1; j<=i;j++){
//     System.out.print("*");
//   }
//   int spaces = 2*(n-i);
//   for(int j = 1;j<=spaces;j++){
//     System.out.print(" ");
//   }
//   for(int j = 1;j<=i;j++){
//     System.out.print("*");
//   }
// System.out.println();
// }  


/ ******************PRINT THE HOLLOW BUTTERFLY PATTERN(REV QUESTION)******************

//  int n = 5;
//  for(int i = 1; i<=n;i++) {
//   for(int j =1;j<=i;j++){
//     if(j ==1 ||j==i){
//       System.out.print("*");
//     }
//     else{
//       System.out.print(" ");
//     }
//       }
  
//   for(int j =1;j<=2*(n-i);j++){
//     System.out.print(" ");
//   }
//   for(int j =1;j<=i;j++){
//     if(j ==1 ||j==i){
//       System.out.print("*");
//     }
//     else{
//       System.out.print(" ");
//     }
//   }
//   System.out.println();
//  }
//  for(int i = n; i>=1;i--) {
//   for(int j =1;j<=i;j++){
//     if(j ==1 ||j==i){
//       System.out.print("*");
//     }
//     else{
//       System.out.print(" ");
//     }
//       }
  
//   for(int j =1;j<=2*(n-i);j++){
//     System.out.print(" ");
//   }
//   for(int j =1;j<=i;j++){
//     if(j ==1 ||j==i){
//       System.out.print("*");
//     }
//     else{
//       System.out.print(" ");
//     }
//   }
//   System.out.println();
//  }


SOURCE(PEPCODE)
 **********************inverse of number**********************
Scanner scn = new Scanner(System.in);
int n = scn.nextInt();
int inv =0;
int op=1;
while(n!=0){
    int od=n%10;
    int id =op;
    int ip = od;
    inv = inv+id*(int)Math.pow(10, ip-1);
    n=n/10;
    op++;


}
System.out.println(inv);
    }
}
<!-- Explaination y dry running this code -->

Dry Run (Input: 31245)
Initial:
n = 31245

inv = 0

op = 1

First Iteration:
od = 31245 % 10 = 5 (Extract last digit: 5)

id = 1 (Position is 1)

ip = 5 (The digit itself: 5)

inv = inv + 1 * Math.pow(10, 5 - 1) = 0 + 1 * Math.pow(10, 4) = 0 + 10000 = 10000

n = 31245 / 10 = 3124

op = 2

Second Iteration:
od = 3124 % 10 = 4

id = 2 (Position is 2)

ip = 4

inv = 10000 + 2 * Math.pow(10, 4 - 1) = 10000 + 2 * Math.pow(10, 3) = 10000 + 2000 = 12000

n = 3124 / 10 = 312

op = 3

Third Iteration:
od = 312 % 10 = 2

id = 3 (Position is 3)

ip = 2

inv = 12000 + 3 * Math.pow(10, 2 - 1) = 12000 + 3 * Math.pow(10, 1) = 12000 + 30 = 12030

n = 312 / 10 = 31

op = 4

Fourth Iteration:
od = 31 % 10 = 1

id = 4 (Position is 4)

ip = 1

inv = 12030 + 4 * Math.pow(10, 1 - 1) = 12030 + 4 * Math.pow(10, 0) = 12030 + 4 = 12034

n = 31 / 10 = 3

op = 5

Fifth Iteration:
od = 3 % 10 = 3

id = 5 (Position is 5)

ip = 3

inv = 12034 + 5 * Math.pow(10, 3 - 1) = 12034 + 5 * Math.pow(10, 2) = 12034 + 500 = 12534

n = 3 / 10 = 0

op = 6

Exit Condition:
Since n = 0, the loop exits.

Final Output:
inv = 12534
  <!-- *Conclusion is that i have to inverse the input. so the function inv = inv+id*(int)Math.pow(10, ip-1); used for input not for the output* -->

******************ROTATE A NUMBER******************
Scanner scn = new Scanner(System.in);
int n = scn.nextInt();
int k = scn.nextInt();
int temp = n;
int count = 0;
while(temp!=0){
  temp = temp/10;
  count++;
}
k = k%count;
if(k<0){
  k = k+ count;
}
int div = 1;
int mult =1;
for(int i = 1;i<=count;i++){
if(i<=k){
  div = div*10;
}else{
  mult = mult*10;
}
}
int q = n/div;
int r =n%div;
int s = r*mult+q;

System.out.println(s);


<!-- Explaination y dry running this code -->



Key Observations:
If k is larger than the number of digits, rotating by k is the same as rotating by k % (number of digits).

Example: For n = 87694 (5 digits), rotating by 9 is the same as rotating by 9 % 5 = 4.

If k is negative, it means left rotation. We can convert it to an equivalent positive right rotation.

Example: Rotating left by 2 is the same as rotating right by 5 - 2 = 3 (for a 5-digit number).

Step-by-Step Explanation:
1. Count the number of digits (counter):
n = 87694 has 5 digits.

2. Adjust k to a valid positive right rotation:
If k = 9:

k = 9 % 5 = 4 (since rotating by 5 is a full rotation and brings the number back to itself).

If k = -8:

k = -8 % 5 = -3 (in Java, % gives remainder, not modulus).

Since k is negative, we add 5 to make it positive: k = -3 + 5 = 2.

3. Calculate div and mult:
div is 10^k (splits the number into two parts).

mult is 10^(counter - k) (used to combine the parts after rotation).

For k = 4:

div = 10^4 = 10000.

mult = 10^(5-4) = 10.

For k = 2:

div = 10^2 = 100.

mult = 10^(5-2) = 1000.

4. Split the number into two parts:
q = n / div (first part).

r = n % div (second part).

For k = 4:

q = 87694 / 10000 = 8.

r = 87694 % 10000 = 7694.

For k = 2:

q = 87694 / 100 = 876.

r = 87694 % 100 = 94.

5. Combine the parts to form the rotated number:
s = r * mult + q.

For k = 4:

s = 7694 * 10 + 8 = 76940 + 8 = 76948.

For k = 2:

s = 94 * 1000 + 876 = 94000 + 876 = 94876.

Final Outputs:
For k = 9 (equivalent to k = 4): 87694 rotated right by 4 is 76948.

For k = -8 (equivalent to k = 2): 87694 rotated right by 2 (or left by 3) is 94876.





// ************************GCD AND LCM**********************
Scanner scn = new Scanner(System.in);
int n = scn.nextInt();
int t = scn.nextInt();

int div = n;
int ded = t;

while( t%n != 0 ){
    int rem = t % n;
    t = n;
   n  = rem;
     
}
int gcd = n;
int lcm = ( div * ded)/ gcd;
 
System.out.println("GCD of given numbers is : " + gcd);
System.out.println("Lcm of the given numbers is : "+ lcm);

*********************BENJAMIN BULB PUZZLE********************
Scanner scn = new Scanner (System.in);
int n = scn.nextInt();
for(int i = 1;i*i<=n;i++);{
System.out.print(i*i);}

    

  // **************************PRIME FACTORIZATION**************************
Scanner scn = new Scanner(System.in);
int n = scn.nextInt();
     for(int i = 2; i * i<= n; i++){
        while(n% i ==0){
            n = n /i;
            System.out.println(i);
        }
if( n!= 1){
    System.out.println(n);
}
     }
**************************Triangle rotated by 180 degree**************************
 Scanner scn = new Scanner (System.in);
        int n  = scn.nextInt();
        int sp = n-1;
        int st =1;
    for(int i = 1 ; i <=n;i++){
        for(int j = 1; j<= sp;j++){
            System.out.print(" " ); 
        } 
        for(int j = 1; j<=st; j++){
            System.out.print("*");
        }
        sp--;
        st++;
        System.out.println();


//************************DIAMOND SHAPE******************
  Scanner scn = new Scanner (System.in);
        int n = scn.nextInt();

        int sp = n/2;
        int st = 1;
        for(int i = 1; i <=n;i++){
            for(int j =1;j<= sp;j++){
                System.out.print("\t");
            }
            for(int j = 1;j<=st;j++){
                System.out.print("*\t");
            }
            if(i<=n/2){
                sp--;
                st+=2;
            }else{
                sp++;
                st-=2;
            }
            System.out.println();
        }
            }
// ****************HOLLOW DIAMOND PATTERN***********

        Scanner scn = new Scanner (System.in);
        int n = scn.nextInt();

        int st= n/2+1;
        int sp = 1;
        for(int i =1;i<=n;i++){
           for(int j = 1; j<= st;j++){
            System.out.print("*\t");
           }

            for(int j =1;j<= sp;j++){
                System.out.print("\t");
            }
            for(int j = 1;j<=st;j++){
                System.out.print("*\t");
            }
       
            if(i<=n/2){
                sp+=2;
                st--;
            }else{
                sp-=2;
                st++;
            }
            System.out.println();
        }
    
//**************DIAMOND PATTERN CODE**********
                         *
                      *     *
                   *           *
                      *     *
                         *


      Scanner scn = new Scanner(System.in);
int n = scn.nextInt();
int os = n/2;
int is=-1;
for(int i = 1 ; i<=n; i++){
    for(int j = 1; j<= os;j++){
        System.out.print("\t");
    }
    System.out.print("*\t");

    for(int j =1 ; j<=is;j++){
        System.out.print("\t");
    }
    if(i> 1 && i<n){
        System.out.print("*\t");
    }
    if(i<=n/2){
        os--;
        is+=2;
    }else{
        os++;
        is-=2;
    }
    System.out.println();
}                      
//**************PASCAL TRIANGLE***********
Scanner scn = new Scanner (System.in);
int n = scn.nextInt();
for(int i = 0;i<=n;i++){
    int icj = 1;
    for(int j = 0;j<=i;j++){
        System.out.print(icj+"\t");
        int icjp1 = icj*(i-j)/(j+1);
        icj =icjp1;
    }
    System.out.println();
}

//**************Table*************
Scanner scn = new Scanner (System.in);
int n = scn.nextInt();

for(int i = 1 ; i<=10;i++){
    int k = n*i;
    System.out.print(n +" * "+ i+ " = "+ k);
  System.out.println();
}

//********************pattern*******************
               1
            2  3  2
        3   4  5  4  3
            2  3  2
               1
  Scanner scn = new Scanner (System.in);
int n = scn.nextInt();

int sp = n/2;
int st = 1;
int val = 1;    
for(int i = 1; i <=n;i++){
    for(int j =1;j<= sp;j++){
       System.out.print("\t");
    }
    int cval = val;
    for(int j = 1;j<=st;j++){
          System.out.print(cval +"\t");
        if(j<=st/2){
            cval++;
        }else{
            cval--;
        }   
    }    
    if(i<=n/2){
        sp--;
        st+=2;
        val++;
    }else{
        sp++;
        st-=2;
        val--;
    }
    System.out.println();
}
    }
    }

  ******************PYTHAGOREAN TRIPLET**************


Scanner scn = new Scanner (System.in);
int a = scn.nextInt();
 int  b= scn.nextInt();
 int c = scn.nextInt();
  int max = a;
  if(b>= max){
    max = b;
    if(c>= max){
        max=c;}
if(max==a){
 boolean flag = ((b*b + c*c)==(a*a));
}   
else if(max==b){
    boolean flag = ((a*a + c*c)==(b*b));
}   
}
else if(max == c){
    boolean flag = (( c*c)==(a*a + b*b));
}   

//********************PATTERN**********************
               1           1
               1 2       2 1
               1 2 3   3 2 1
               1 2 3 4 3 2 1
Scanner scn = new Scanner (System.in);
int n = scn.nextInt();

int st = 1;
int sp = 2*n-3;

 for(int i = 1;i<=n;i++){
   int val = 1;
    for(int j = 1;j<=st;j++){
        System.out.print(val +"\t");
       val++;
    }
    for(int j = 1; j<= sp; j++){
        System.out.print("\t");
    }
  😉if(i==n){
        st--;
        val--;
    }

    for(int j = 1;j<=st;j++){
        val--;
  System.out.print(val +"\t");

       }
  
    st++;
    sp-=2;
 System.out.println(); 
    }

  *******************ARROW PATTERN****************
     Scanner scn = new Scanner(System.in);
    int n = scn .nextInt();
    int sp = n/2;
    int st = 1;
     for(int i = 1; i<=n;i++ ){
        for(int j =1;j<= sp;j++){
            if(i==n/2+1){
                System.out.print("*\t");
            }else{
                System.out.print("\t");
            }
        }
        for(int j = 1 ; j<= st; j++){
            System.out.print("*\t");
        }
        if(i<=n/2){
          st++;
        }else{
            st--;
        }
        System.out.println();
     }
//********************PATTERN**************************

                 * * * * * * *
                   *      *
                     *  *
                      *
                    * * *
                 * *  * * *
               * * * * * * *
Scanner scn = new Scanner(System.in);
int n = scn.nextInt();
 int st = n;
 int sp =0;
 for(int i = 1; i<= n;i++){
  for(int j = 1; j<=sp;j++){
    System.out.print("\t");
  }
  for(int j  = 1; j<=st;j++){
    if(i>1 && i<=n/2+1 && j>1 &&j<st){
System.out.print("\t");
    }else{
 System.out.print("*\t");
} 
}
if(i <= n/2)
{sp++;
st-=2;
}else{
  sp--;
  st+=2;
}  
System.out.println();  
}

//********************SWASTIK******************************
Scanner scn = new Scanner(System.in);
int n = scn.nextInt();
 for(int i = 1; i<= n;i++){
  for(int j = 1; j<=n;j++){

    if(i==1 ){

      if(j==n  || j<=n/2+1){
        System.out.print("*\t");
      }else{
        System.out.print("\t");
      }

    }else if(i<=n/2) {

      if(j==n/2+1 || j==n){
        System.out.print("*\t");
      }else{
        System.out.print("\t");
      }

        
    }else if(i==n/2+1){

  System.out.print("*\t");
    }else if(i<n) {
      if(j==1|| j==n/2+1){
        System.out.print("*\t");
      }else{
        System.out.print("\t");
      }    

    }else{

      if(j==1||j>=n/2+1){
        System.out.print("*\t");
      }else{
      System.out.print("\t");}

    }
    
  }
  System.out.println();
 }
} 
*******************'PRINT W*************************
Scanner scn = new Scanner(System.in);
int n = scn.nextInt();

for(int i = 1;i<=n;i++){
  for(int j =1 ; j<= n;j++){
    
      if(j==1 || j==n){
        System.out.print("*\t");
      }else if ( i>n/2 && (i==j|| i+j ==n+1)){
        System.out.print("*\t");
      } else{
        System.out.print("\t");
      }
          
      }
  
  System.out.println();
} 

*******QUES - is number prime?***********


Scanner scn = new Scanner(System.in);
int t = scn.nextInt();
int counter = 0;
for(int i = 1;i<=n;i++){
int n =scn.nextInt();
for(div = 2; div*div <= n;div++){
if(n%div==0){
count++;
break;
}
if(count == 0){
System.out.println("prime")
}
else{
System.out.println("not prime")
}
}

*************QUES -PRINT ALL THE PRIME NUMBER TILL N****************
Scanner scn = new Scanner(System.in);
int low = scn.nextInt();
int high = scn.nextInt();
for(int i = low;i<=high;i++){
int counter = 0;
int n =scn.nextInt();
for(div = 2; div*div <= n;div++){
if(n%div==0){
count++;
break;
}
if(count == 0){
System.out.println(i)
}
}
************QUES - FIBONACCI NUMBERS*******************

Scanner scn = new Scanner(System.in);
int n= scn.nextInt();
int a = 0;
int b = 1;
for(int i = 1; i<=n;i++){
  System.out.println(a);
  int c =  a+b;
a = b;
b =c;
}
**************QUES - COUNT DIGIT IN A NUMBER*****************
Scanner scn = new Scanner(System.in);
int n   = scn.nextInt();
int count=0;
while(n%10==0){ 
   
  count++;


}System.out.println(count);
*************QUES- DIGITS OF A NUMBER******************
Scanner scn = new Scanner(System.in);
int n   = scn.nextInt();
 int count = 0;
 int temp = n;
 while(temp!=0){
temp = temp/10;
 count++;
 }
 int div = (int)Math.pow(10,count -1);
 while(div!=0){
  int q = n/div;
System.out.println(q);
n = n % div;
div = div/10;
 }
 *********************REVERSE A NUMBER***********
Scanner scn = new Scanner(System.in);
int n = scn.nextInt();
while(n != 0){
  int r = n%10;
  System.out.println(r);
  n = n/10;
}
 

