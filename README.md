# Minimum-number-of-operation-required-to-make-all-array-element-equal-in-cpp

**PROBLEM STATEMENT**
Given an array with n positive integers. We need to find the minimum number of operation to make all elements equal. We can perform addition, multiplication, subtraction or division with any element on an array element. 

Examples: 
 

Input : arr[] = {1, 2, 3, 4}

Output : 3

Since all elements are different, 
we need to perform at least three
operations to make them same. For
example, we can make them all 1
by doing three subtractions. Or make
them all 3 by doing three additions.

Input : arr[] = {1, 1, 1, 1}

Output : 0

**CODE**
Time complexity : O(N)
```


#include <bits/stdc++.h>

using namespace std;

int main()
{
   int a[]={1,2,3,4};
   int n=sizeof(a)/sizeof(a[0]);
   unordered_map<int,int>mp;
    for(int i=0;i<n;i++)
    {
        mp[a[i]]++;
    }
    int max_ct=0;
    for(auto i:mp)
    {
        if(i.second>max_ct)
        {
            max_ct=i.second;
        }
    }
    cout<<n-max_ct;

    return 0;
}
