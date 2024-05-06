# Mario_salary
Dynamic Programming to find the max work days

## Description
Mario, a plumber by profession, has a passion for films. Whenever he has free time, he takes on temporary acting jobs in movies or music videos. These temporary acting jobs span multiple consecutive days, and the payment is calculated on a daily basis.

Currently, Mario has received multiple opportunities for temporary acting jobs. Each job has a start date and an end date. Since filming starts at noon and ends at noon, the number of days for payment calculation is determined by subtracting the start date from the end date.

Given the start and end dates of multiple temporary acting jobs, as well as Mario's availability for acting from a certain start date to an end date, help Mario select the acting jobs that maximize his income.

For example, if there are 7 temporary acting jobs with start and end dates as follows: {[6, 10], [10, 12], [8, 13], [3, 7], [1, 6], [13, 16], [5, 9]}, and Mario is available from the 1st to the 16th day, selecting {[1, 6], [6, 10], [10, 12], [13, 16]} would yield the highest income for Mario, totaling 14 days of income (5 + 4 + 2 + 3 = 14). If Mario is available from the 3rd to the 12th day, then selecting {[3, 7], [10, 12]} or {[5, 9], [10, 12]} or {[6, 10], [10, 12]} would maximize his income, totaling 6 days of income (4 + 2 = 6).

## Input
- The first line of input contains an integer N, representing the number of temporary acting jobs. N is a positive integer where 1 ≤ N ≤ 1000.

- The next N lines (from the 2nd line to the N+1th line) each contain the start date and end date of a temporary acting job, denoted as X and Y, respectively. X and Y are positive integers where 1 ≤ X < Y ≤ 3650, and they are separated by a single space.

- The (N+2)th line of input contains the start and end dates when Mario is available for acting, denoted as U and V, respectively. U and V are positive integers where 1 ≤ U < V ≤ 3650, and they are separated by a single space.

## Output
The output is a positive integer P, where P ≥ 0, representing the maximum number of days Mario can work to earn the highest income.
