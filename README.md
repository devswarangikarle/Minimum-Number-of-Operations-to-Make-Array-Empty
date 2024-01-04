# Minimum-Number-of-Operations-to-Make-Array-Empty

from collections import Counter
from typing import List

class Solution:
    def minOperations(self, nums: List[int]) -> int:
        num_counter = Counter(nums)      
        count = 0       
        for frequency in num_counter.values():
            
            if frequency == 1:
                return -1
            
           
            count += frequency // 3
            
           
            if frequency % 3:
                count += 1
                
       
        return count
