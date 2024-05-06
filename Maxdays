def max_work_days(works):
    n = len(works)

    # dp[i] will store the maximum work days until the i-th work
    dp = [0] * n

    # Calculate the maximum work days for each work
    for i in range(n):
        # The work days if we include the i-th work
        include = works[i][1] - works[i][0]

        # Find the latest work that doesn't conflict with the i-th work
        j = i - 1
        # print("i",{i},"j",{j})
        while j >= 0:
            if works[j][1] <= works[i][0]:
                include += dp[j]
                # print("include",{include})
                break
            j -= 1
        
        # The maximum work days until the i-th work is the maximum of the work days if we include or exclude the i-th work
        dp[i] = max(include, dp[i - 1] if i > 0 else 0)
        # print(dp)

    # The maximum work days is the maximum work days until the last work
    return dp[-1]

# read the the first line of input
n = int(input())
# read the next n lines of input and store the values in a list of tuples
# where each tuple is a pair of integers representing the start and end date of a work
works = [tuple(map(int, input().split(' '))) for _ in range(n)]
#read the last line of input
start, end = map(int, input().split(' '))
# remove the works that are outside the available start and end date
works = [work for work in works if work[0] >= start and work[1] <= end]
# resort the works list by the end date and the period of work
works.sort(key=lambda x: (x[1], x[1] - x[0]))
#print(works)

print(max_work_days(works))
