# haocheng
LeetCode- Two Sum(python)
class Solution(object):
    def twoSum(self, nums, target):
        # Create a dictionary to store the indices of elements
        num_indices = {}

        for i, num in enumerate(nums):
            complement = target - num

            # Check if the complement is in the dictionary
            if complement in num_indices:
                # Return the indices of the two numbers that add up to the target
                return [num_indices[complement], i]

            # If the complement is not in the dictionary, store the current number and its index
            num_indices[num] = i

        # If no solution is found
        return None


# Example usage:
solution = Solution()

nums1 = [2, 7, 11, 15]
target1 = 9
print(solution.twoSum(nums1, target1))  # Output: [0, 1]

nums2 = [3, 2, 4]
target2 = 6
print(solution.twoSum(nums2, target2))  # Output: [1, 2]

nums3 = [3, 3]
target3 = 6
print(solution.twoSum(nums3, target3))  # Output: [0, 1]
