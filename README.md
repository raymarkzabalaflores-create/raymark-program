while True:
    print("================= PYHTON TUTORAIL ==================")
    print()
    print()
    print("FUNDAMENTALS OF PROGRAMMING LESSONS!")
    print("[1] BASIC SYNTAX")
    print("[2] INTRODUCTION TO PROGRAMMING")
    print("[3] ARITHMETIC OPERATORS")
    print("[4] BASIC INPUT AND OUTPUT IN PYTHON")
    print("[5] MIDTERM FIRST LESSON - CONDITIONAL STATEMENT IN PYHTON")
    print("[6] MIDTERM SECOND LESSON - LOGICAL OPERATOR")
    print("[7] FINAL LESSON - INTRODUCTION TO ITERATION AND LOOPS")
    print("[8] EXIT")

    try:
        code = int(input("Choose One lesson [1-7]"))
    except ValueError:
        print("Please Enter a number")
        input("Enter anything to continue...")
        continue

    if code == 1:
        print("Lesson 1 - BASIC SYNTAX")
        print("[A] WHAT IS PROGRAMMING LANGUAGE?")
        print("[B] WHO BUILD PYTHON PROGRAMMING?")
        print("[C] WHAT IS PYTHON PROGRAMMING?")
        print("[D] WHY LEARN PYTHON?")
        print("[E] WHAT DO YOU NEED TO START PYTHON PROGRAMMING?")
        print("[F] EXIT LESSON?")

        while True:
            Letters = input("Enter letter in lesson 1 and enter (F) if EXIT: ")

            if Letters == "A":
                print("======= WHAT IS PROGRAMMING LANGUAGE? =======")
                print()
                print("A PROGRAMMING LANGUAGE IS A SPEACIAL LANGUAGE")
                print("EXAMPLE OF PROGRAMMING LANGUAGE IS 'PYHTON', ")
            elif Letters == "B":
                print("======= WHO BUILD PYTHON PROGRAMMING? =======")
                print()
                print("PYTHON US A WIDELY USED PROGRAMMING LANGUAGE.")
                print("A DUTCH SOFTWARE ENGINEER BEST KNOW FOR CREATING")
                print("HE DESIGNED PYTHON WITH THE GOAL OF MAKING PROGRAM")
            elif Letters == "C":
                print("======= WHAT IS PYTHON PROGRAMMING? =======")
                print()
                print("PYTHON IS A HIGH LEVEL, AND INTERPRETED.")
            elif Letters == "D":
                print("============ WHY LEARN PYTHON? ============")
                print()
                print("1. SIMPLE AND EASY TO LEARN - GREATFOR BEGINNERS.")
                print("2. HUGE COMMUNITY - LOT OF SUPPORT. AND TUTORIALS.")
                print("3. READABLE SYNTAX - CODE LOOKS ALMOST LIKE ENGLISH")
                print("4. VERSATILE - USE INAMY FIELDS (AI,WEB,)")
            elif Letters == "E":
                print("====== WHAT DO YOU NEED TO START PYTHON PROGRAMMING? =====")
                print()
                print("A COMPUTERS OR LAPTOPS")
                print()
                dev = input("DO YOU HAVE COMPUTERS OR LAPTOPS? (Y)YES OR N?(NO): ")
                if dev == "Y":
                    print("NICE!, YOU'RE READY TO START.")
                elif dev == "N":
                    print("NO PROBLEM, YOU CAN EVEN RUN PYHTON")
                else:
                    print("INVALID INPUT!")

                print("PROFESSIONAL IDES/ CODE EDITORS")
                print("PYCHARM (BY JETBRAINS)")
            elif Letters == "F":
                print("EXITING LESSON")
                break

            else:
                print("INVALID LETTER CHOICE!!")
