# Python 3 basics and dictionaries operations
# hackerrank problems
Hackerrank python problem for finding percentage of marks from a dictionary
There are two way solutions to this problem.
The problem is this:
You have a record of N students. Each record contains the student's name, and their percent marks in Maths, Physics and Chemistry. The marks can be floating values. The user enters some integer N followed by the names and marks for N students. You are required to save the record in a dictionary data type. The user then enters a student's name. Output the average percentage marks obtained by that student, correct to two decimal places.

Input Format:

The first line contains the integer N, the number of students. The next N lines contains the name and marks obtained by that student separated by a space. The final line contains the name of a particular student previously listed.

Constraints:

1. 2<=N<=10
2. 0<=Marks<=100

Output Format:

Print one line: The average of the marks obtained by the particular student correct to 2 decimal places.

Sample Input 0:

3
Krishna 67 68 69
Arjun 70 98 63
Malika 52 56 60
Malika
Sample Output 0

56.00



The solution number one is:

if __name__ == '__main__':
    n = int(input())
    student_marks = {}
    for x in range(n):
        name, *line = input().split()
        scores = list(map(float, line))
        student_marks[name] = scores
    query_name = input()
    print("%.2f"%(sum(student_marks[query_name])/len(student_marks[query_name])))
    
    
The solution number two is:
if __name__=='__main__':
      N = int(input())
      results = {}
      for i in range(N):
          a = input().split()
          results[a[0]] = [float(x) for x in a[1:]]
      student = input()
      print("%.2f" %(sum(results[student])/len(results[student])))
