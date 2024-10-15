# LEETCODE-Strings-2938
### Dry Run Example:

**Input:** `"10101"`

**Step-by-step Dry Run:**
- `n = 5` (length of the string)
- `swaps = 0` (initial number of swaps)
- `white = 0` (initial number of '0's)

**Iterating from the end of the string:**
1. **i = 4, `s.charAt(4)` = '1':**
   - Encounter '1' → Add `white` (which is 0) to `swaps`: `swaps = 0 + 0 = 0`
   - Result: `swaps = 0`, `white = 0`
   
2. **i = 3, `s.charAt(3)` = '0':**
   - Encounter '0' → Increment `white`: `white = 0 + 1 = 1`
   - Result: `swaps = 0`, `white = 1`

3. **i = 2, `s.charAt(2)` = '1':**
   - Encounter '1' → Add `white` (which is 1) to `swaps`: `swaps = 0 + 1 = 1`
   - Result: `swaps = 1`, `white = 1`

4. **i = 1, `s.charAt(1)` = '0':**
   - Encounter '0' → Increment `white`: `white = 1 + 1 = 2`
   - Result: `swaps = 1`, `white = 2`

5. **i = 0, `s.charAt(0)` = '1':**
   - Encounter '1' → Add `white` (which is 2) to `swaps`: `swaps = 1 + 2 = 3`
   - Result: `swaps = 3`, `white = 2`

### Final Output:
After the loop, the final value of `swaps` is `3`. Therefore, the minimum number of swaps required is `3`.

**Explanation:**
- We swap the '1' at index 0 with the '0' at index 1 → 1 swap.
- We swap the '1' at index 2 with the '0' at index 3 → 1 more swap.
- We swap the '1' at index 4 with the '0' at index 1 (after moving the '1' at index 0) → 1 more swap.
Thus, the total swaps are 3.

**Output:** `3`
