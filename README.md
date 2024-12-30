graph TD;
    A[Start] --> B[Menu]
    B -->|1. Add Student| C[readStudentData]
    B -->|2. Exit| D[End]
    
    C --> E[Input student name]
    E --> F{Check if MAX_STUDENTS reached}
    F -->|Yes| G[Print "Maximum number of students reached"]
    F -->|No| H[Input study hours for each day]
    H --> I[Store student data]
    I --> J[Increment numStudents]
    J --> K[Ask for next student name or -1 to exit]
    K -->|Enter -1| L[Return to Menu]
    K -->|Continue| E

    B -->|After adding students| M[Calculate totals and averages]
    M --> N[calculateTotalsAndAverages]
    N --> O[Update totals and averages]

    B -->|2. See Result| P[printResults]
    P --> Q[Display table of results]
    Q --> L

    B -->|3. Search Student| R[searchStudent]
    R --> S[Input search term]
    S --> T{Search for student}
    T -->|Found| U[Display student data]
    T -->|Not Found| V[Print "Student not found"]
    U --> L
    V --> L

    B -->|4. Exit| D
