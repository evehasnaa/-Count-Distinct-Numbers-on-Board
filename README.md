class Solution:
    def monkeyMove(self, n: int) -> int:
        mod=10**9+7
        res=pow(2,n,mod)-2
        #res=(2**n %1_000_000_007)-2
        if res >=0:
            return res
        else :
             res +=mod
             return res
