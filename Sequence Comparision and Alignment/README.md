# Sequence Comparision and Optimal Alignment

Python implementations of common algorithms used in comparing sequences and finding optimal alignment

## List of programs

### similarity.py
Finding the similarity between two sequences by constructing a similarity matrix using Dynamic programming approach.
Similarity Score for the sequnces is assigned based on the following scoring scheme -
- Matches are scored +1
- Mismatches are penalized by assigning -1 score
- InDel (Insertions and Deletions) are heavily penalized by assigning -2 score

#### Example

```
Similarity score for sequences CGATCGAGCAATCG and CGATGAGCATCA is 6 .
C G A T C G A G C A A T C G
C G A T _ G A G C _ A T C A
| | | | | | | | | | | | | |
1+1+1+1-2+1+1+1+1-2+1+1+1-1 = 6
        ^         ^
      InDel      InDel
```

### globalAlignment.py
Finding the alignment having maaximum similarity score for the given sequences using the similarity matrix
by implementation of basic algorithm for Global Comparision.

### References
- https://en.wikipedia.org/wiki/Needleman%E2%80%93Wunsch_algorithm
- Introduction to Computational Molecular Biology by Setubal and Meidanis
