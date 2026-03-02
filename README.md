# Competitive Programming Template (C++)

This repository provides a minimal template for competitive programming in C++.
It is designed to be a starting point for solving problems quickly during contests
or practice sessions.

## Structure

- `temp.cpp`: The main C++ source file where you can write your solution code.
- `LICENSE`: The license for the repository (e.g., MIT).

## Usage

1. Open `temp.cpp` and implement your solution. The template is geared toward lightweight editors — **Vim** is recommended for local contests, or you can paste it into an online tool like **onlineGDB** if you prefer a web IDE.
2. Compile using a C++17 compatible compiler, e.g.:
   ```bash
   g++ -std=c++17 temp.cpp -O2 -o main
   ```
3. Run with input redirection if needed:
   ```bash
   ./main < input.txt
   ```

## Explanation (line-by-line)
Each line in `temp.cpp` represents a common element you might start with when writing a solution. Here's what the template typically contains:

1. `#include <bits/stdc++.h>` - includes the standard C++ library header for convenience.
2. `using namespace std;` - brings standard names into the global namespace to reduce typing.

Each numbered description above helps you understand the purpose of that line in the template file, so you can adapt it as needed during contests.

## Types and constants
The template also declares a common type alias and a couple of frequently‑used constants:

- `typedef long long ll;`
  - Creates the shorthand `ll` for `long long`, making it easier to declare 64‑bit integers which are common in competitive problems.

- `const int INF = 0x3f3f3f3f;`
  - A large integer value often used as a stand‑in for infinity when initializing distances or DP tables. The hex literal is chosen because adding it repeatedly doesn't overflow and it fits in a 32‑bit int.

- `const ll LINF = 0x3f3f3f3f3f3f3f3fll;`
  - The 64‑bit version of `INF` for `long long` types, used in similar contexts when bigger limits are needed.

## Macros (defines)
The template uses several `#define` directives in `temp.cpp` to shorten common patterns:

- `#define _ ios_base::sync_with_stdio(0);cin.tie(0);`
  - A shorthand macro executed at the start of `main()` to speed up C++ I/O by disabling the synchronization with C stdio and untieing `cin` from `cout`.

- `#define endl '\n'`
  - Redefines `endl` to a newline character only, avoiding the flush that the standard `endl` performs. This improves performance when printing many lines.

- `#define f first` and `#define s second`
  - Shortcuts for accessing the `.first` and `.second` members of `std::pair` objects.

- `#define dbg(x) cout << #x << " = " << x << endl`
  - A simple debugging macro that prints both the variable name and its value followed by a newline. Useful during development but usually removed in contest submissions.

Feel free to adapt or extend the template as needed for your contests.