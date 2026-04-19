# Student Data Sorting Benchmark

## Overview
A C++ console application that implements and benchmarks multiple classical sorting algorithms to organize structured student records. The program reads student data from a text file, sorts the records by name and GPA using various algorithms, measures execution time for each, and exports the formatted results to separate output files.

## Features
- Implements seven fundamental sorting algorithms: Insertion, Selection, Merge, Quick, Counting, Bubble (recursive), and Shell sort.
- Supports dual sorting criteria: alphabetical order by student name and numerical order by GPA.
- Automated execution time measurement using CPU clock cycles, reported in milliseconds.
- Template-based implementation for algorithm reusability across different data types.
- Structured file I/O: reads from `students.txt` and appends benchmarked results to `SortedByName.txt` and `SortedByGPA.txt`.
- Operator overloading for intuitive custom object comparison.

## Technologies Used
- Language: C++
- Standard Libraries: iostream, fstream, vector, map, algorithm, string, clock
- Compiler: Compatible with GCC, Clang, MSVC, or any standard C++11+ compliant compiler

## Setup and Usage
1. Clone or download the repository to your local machine.
2. Ensure a `students.txt` file exists in the same directory as the executable. The input format must be:
   - Line 1: Integer representing the number of students
   - Following lines: Groups of three lines per student (Name, ID, GPA)
3. Compile the source code:
```bash
g++ SortingAlgorithms.cpp -o SortingAlgorithmsv
```
4. Run the executable:
```
./SortingAlgorithms
```
5. Open `SortedByName.txt` and `SortedByGPA.txt` to view sorted records and algorithm performance metrics.

## Output Format

- Each output file contains sequentially appended blocks for every executed algorithm, structured as:
  - Algorithm name
  - Execution time in milliseconds
  - Sorted student entries (Name, ID, GPA)
  - Visual separator for readability

## Notes

- Execution times are measured using clock() and may vary depending on system load and hardware.
- The program uses template functions to enable easy extension to other comparable data structures.
- Input files must strictly follow the specified line-by-line format to ensure correct parsing.
