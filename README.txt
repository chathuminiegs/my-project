def calculate_average(subject_scores):
    total_score = sum(subject_scores)
    num_subjects = len(subject_scores)
    average = total_score / num_subjects
    return average

def main():
    subject_scores = []  # List to store the scores for each subject

    # Input scores for each subject
    for i in range(1, 10):
        while True:
            try:
                score = float(input(f"Enter the score for subject {i}: "))
                if score < 0 or score > 100:
                    raise ValueError("Score must be between 0 and 100")
                subject_scores.append(score)
                break
            except ValueError as e:
                print(str(e))

    # Calculate the average
    average_score = calculate_average(subject_scores)

    # Print the average score
    print("Average score across all subjects:", average_score)

if __name__ == "__main__":
    main()

