# ranking
# python
# If the number of students is entered in N, the expected rank of the entered students is entered, and the degree of dissatisfaction occurs as much as the difference between the expected rank and the current rank after ranking from the expected rank, what is the minimum degree of dissatisfaction? N에 학생수를 입력하고 입력한 학생들의 예상 등수를 입력받고 예상등수에서 등수를 매기고 나서 예상과 현재등수의 차이만큼 불만도가 발생한다고할때, 불만도의 최소는 얼마인가?
import sys
input=sys.stdin.readline
N=int(input())
ex=[0 for i in range(N)]
for i in range(N):
    ex[i]=int(input())
ex.sort()
result=0
for i in range(N):
    result+=abs(ex[i]-(i+1))
print(result)
#input--> 5  1 5 3 1 2
#result--> 3
