# prefix
*used in range query + sum
*in subsequence you can sort then sum or vice versa 
*used in update range problems to check if a number found in a range
*it's not include prefixsum only,there are prefix xor,prefix multiplication and others also
-Example for xor prefix:https://leetcode.com/problems/maximum-xor-for-each-query
-Examole for prefix multiplication: https://leetcode.com/problems/product-of-array-except-self/submissions/
*Sum of Absolute Differences in a Sorted Array:https://leetcode.com/problems/sum-of-absolute-differences-in-a-sorted-array---->PROBLEMMMMMMMM
in 2D array to do prefix:
first you should do prefix for rows (r+1)+=(r)
second for columns (c+1)+=c
code:
for(int i=0;i<1005;i++)//prefix for rows (r+1)+r
        {
            for(int j=0;j<1005;j++)
            a[i+1][j]+=a[i][j];
        }
         for(int i=0;i<1005;i++)//prefix for columnss (c+1)+c
        {
            for(int j=0;j<1005;j++)
            a[i][j+1]+=a[i][j];
        }
 Another Better code:
 vector<vector<int>>sum(m+1,vector<int>(n+1));
         for(int i=0;i<m;i++)
         {
             for(int j=0;j<n;j++)
                 sum[i+1][j+1]=sum[i+1][j]+sum[i][j+1]-sum[i][j]+mat[i][j];
         }
  //D-b-c+a---->for last answer one way for this implementation:
  sum[maxr][maxc]-sum[maxr][minc]-sum[minr][maxc]+sum[minr][minc];// if sum start from 1 add 1 to maxr and maxc;
  Example for 2D prefix problems:https://leetcode.com/problems/matrix-block-sum
  
