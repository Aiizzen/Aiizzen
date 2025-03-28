                              MY DSA JOURNEY QUES 
    
    
    SOURCE(SHRADDHA KHAPRA)
    // ***********************************Hollow rectangle **********************( Revision ques)
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

/***************PRINT A NUMBER PYRAMID */
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


/*****************PRINT A PALINDROMIC NUMBER PYRAMID */
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

// *******************PRINT BUTTERFLY PATTERN***********************
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


/ ******************PRINT THE HOLLOW BUTTERFLY PATTERN(REV QUESTION)

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
