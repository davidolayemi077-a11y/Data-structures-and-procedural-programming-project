# Data-structures-and-procedural-programming-project
Project outline
Javascript solution for the first Problem
 for (let i = 0; i < arr1.length; i++) {
        if (!arr2.includes(arr1[i])) {
            sum += arr1[i];
        }
    }

    // Elements in arr2 but not in arr1
    for (let i = 0; i < arr2.length; i++) {
        if (!arr1.includes(arr2[i])) {
            sum += arr2[i];
        }
    }

    return sum;
}

// Example
let set1 = [3, 1, 7, 9];
let set2 = [2, 4, 1, 9, 3];

console.log(sumOfDistinct(set1, set2)); // Output: 13


Solution for Problem 2
Algorithm Procedure
Procedure dot_product(v1, v2, n, ps)
    ps ← 0
    For i ← 1 to n do
        ps ← ps + (v1[i] * v2[i])
    EndFor
EndProcedure

 Algorithm using Procedure
Algorithm Check_Orthogonal
    Read number_of_pairs

    For k ← 1 to number_of_pairs do
        Read n   // size of vectors

        Declare v1[n], v2[n]

        // Input vectors
        For i ← 1 to n do
            Read v1[i]
        EndFor

        For i ← 1 to n do
            Read v2[i]
        EndFor

        // Call procedure
        dot_product(v1, v2, n, ps)

        If ps = 0 then
            Print "Vectors are orthogonal"
        Else
            Print "Vectors are not orthogonal"
        EndIf
    EndFor
EndAlgorithm

Modified Version Using a Function
Function dot_product(v1, v2, n)
    ps ← 0
    For i ← 1 to n do
        ps ← ps + (v1[i] * v2[i])
    EndFor
    Return ps
EndFunction
Algorithm Check_Orthogonal_Function
    Read number_of_pairs

    For k ← 1 to number_of_pairs do
        Read n

        Declare v1[n], v2[n]

        // Input vectors
        For i ← 1 to n do
            Read v1[i]
        EndFor

        For i ← 1 to n do
            Read v2[i]
        EndFor

        ps ← dot_product(v1, v2, n)

        If ps = 0 then
            Print "Vectors are orthogonal"
        Else
            Print "Vectors are not orthogonal"
        EndIf
    EndFor
EndAlgorithm
