## Purpose
- Perform prime factorization of a given number n.
- Output each prime factor along with its power (exponent).

## Full Code

#include <iostream>
#include <vector>

using namespace std;

struct Factor
{
    long long Prime;
    long long Power;
};

vector<Factor> Factorisation(long long n)
{
    Factor F;
    vector<Factor> FF;
    long long d{ 2 };
    while (n != 1)
    {
        if (n % d == 0)
        {
            F.Power = 0;
            F.Prime = d;
            while (n % d == 0)
            {
                n /= d;
                F.Power += 1;
            }
            FF.push_back(F);
        }
        d++;
        if (n != 1 && d * d > n)
        {
            FF.push_back({ n, 1 });
            break;
        }
    }

    return FF;
}

int main()
{
    long long n;
    cin >> n;
    vector<Factor> FF = Factorisation(n);
    for (auto x : FF)
    {
        cout << x.Prime << "^" << x.Power << endl;
    }
    return 0;
}

## Explanation
1. Reads a number n from input.
2. Performs prime factorization using trial division.
3. Stores results as vector of Factor structs with Prime and Power.
4. Prints each factor in the format "prime^power".

## Example
Input:
360

Output:
2^3  
3^2  
5^1  

Explanation: 360 = 2³ × 3² × 5¹

## Key Points
- Simple trial division algorithm.
- Stops early if divisor squared is greater than remaining n.
- Efficient for small and medium numbers.
- Returns a vector of factors for easy reuse.
