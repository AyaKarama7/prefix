# prefix
*used in range query + sum
*in subsequence you can sort then sum or vice versa 
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
