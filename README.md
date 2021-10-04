# 20211004

LeetCode 169. Majority Element - homework for Algorithm

#1
class Solution:
    def majorityElement(self, nums: List[int]) -> int:
        majority = len(nums) / 2
        for i in range(len(nums)):
            count = nums.count(nums[i])
            if count > majority:
                return nums[i]
                
                
: time limit exceeded.


#2 Boyer-Moore Algorithm
class Solution:
    def majorityElement(self, nums: List[int]) -> int:
        candidate = nums[0]
        count = 1
        for i in range(len(nums)):
            if candidate == nums[i]:
                count += 1
            else:
                count -= 1
            
            if count == 0:
                candidate = nums[i]
                count = 1
            
        return candidate







[새로운 정보]
dictionary.get(a, b) : a는 얻고 싶은 value의 key값, b는 a인자가 없을 경우 출력하고 싶은 값. (list에는 X)
range(a, b, c): a부터 b까지, c간격으로. 
