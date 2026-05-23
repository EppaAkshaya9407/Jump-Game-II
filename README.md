# Jump-Game-II
nums = list(map(int, input("Enter array elements: ").split()))
jumps = 0
current_end = 0
farthest = 0
for i in range(len(nums) - 1):
    farthest = max(farthest, i + nums[i])
    if i == current_end:
        jumps += 1
        current_end = farthest
print("Minimum jumps:", jumps)
