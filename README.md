grades = {
    "A": 5,
    "B": 4,
    "C": 3,
    "D": 2,
    "E": 1,
    "F": 0
}


n = int(input())


student_scores = {}


for _ in range(n):
    weight, grade = input().split()
    weight = int(weight)


    if grade in student_scores:
        student_scores[grade] += weight
    else:

        student_scores[grade] = weight


sorted_scores = sorted(student_scores.items(), key=lambda x: (-x[1], x[0]))


for grade, total_weight in sorted_scores:
    print(total_weight, grade)
