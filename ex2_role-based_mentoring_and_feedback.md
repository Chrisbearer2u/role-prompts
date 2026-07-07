1.  Ask the model to act as a coding mentor.

        Prompt: "Act as a Coding Mentor specializing in Python, focusing on code readability, security, and efficiency".

2.  Provide a simple piece of code.

        Python function with a bug:
```py
            numbers = [10, 20, 30, 40]

            average = sum(numbers) / len(numbers + 1)

            print("Average:", average)
```

3.  Prompt the model: "Act as a mentor reviewing this code. Provide corrections and explain improvements."

    Model Output:

        🔍 Issues in the code:

            A.  'len(numbers + 1)' is invalid

                    . 'numbers' is a list. You cannot add an integer '(1)' to a list. This will throw a 'TypeError'.

                    . 'len()' should be called on the list itself: 'len(numbers)'.

            B.  Logic: calculating average

                    . The average is correctly calculated as the sum of elements divided by the number of elements. The mistake is only in the 'len(numbers + 1)' part.

            C.  Minor suggestion: clarity

                    . It’s good practice to check if the list is not empty before dividing, to avoid a division by zero error.

        ✅ Corrected and improved code:
```py
            numbers = [10, 20, 30, 40]

            # Check if the list is not empty
            if numbers:
                average = sum(numbers) / len(numbers)
                print("Average:", average)
            else:
                print("Cannot compute average of an empty list.")
```

        💡 Improvements explained:

            A.  'len(numbers)' instead of 'len(numbers + 1)'

                    . 'len(numbers)' returns the number of items in the list correctly.

            B.  Empty list safety

                    . Adding the 'if numbers:' check ensures the program won’t crash if the list is empty.

            C.  Readability

                    . Separating the check from the calculation makes the code more maintainable.


4.  Review the response and check if the role influences feedback style.

        The role clearly influences feedback style because the coding mentor emphasizes more on teaching rather than just fixing code. It explains why errors occur, guides step-by-step through issues and corrections, suggests preventive practices like handling empty lists, encourages readability, and invites further exploration. This approach fosters understanding, good habits, and curiosity in learners.

        Key points:

            . Explains errors and their causes

            . Provides step-by-step guidance

            . Suggests preventive practices (e.g., empty list check)

            . Encourages readability and maintainability

            . Invites exploration and curiosity