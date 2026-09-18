# Reflection

## 1. When did the baseline become noticeably sluggish?

The baseline algorithm was still quick at `n = 1,000`, taking roughly 0.015 seconds on this run. At `n = 2,500` it took about 0.09 seconds, and at `n = 5,000` it took about 0.35 seconds. By `n = 10,000`, it took about 1.5 seconds. Therefore, it became noticeably sluggish around `n = 5,000` and increasingly inconvenient beyond that point.

## 2. Estimated baseline time for 1,000,000 elements

The baseline checks every contiguous subarray, so its running time is quadratic, $O(n^2)$. The benchmark took approximately 1.41 seconds for 10,000 elements. Increasing the input size by a factor of 100 increases the estimated time by a factor of $100^2 = 10,000$:

```text
1.5 sec * 10,000 = 15,000 sec
```

That is approximately 250 minutes, or 4.2 hours. This is an estimate; actual time depends on the computer and system load.

## 3. Estimated Kadane time for 1,000,000 elements

Kadane's algorithm processes each element once, so its running time is linear, $O(n)$. The benchmark took approximately 0.00024 seconds for 10,000 elements. Increasing the input size by a factor of 100 gives:

```text
0.00024 seconds * 100 = 0.024 seconds
```

Therefore, Kadane's algorithm should process 1,000,000 elements in roughly 0.02 to 0.03 seconds on a similar machine.

## Conclusion

The plot shows the practical difference between quadratic and linear growth. The baseline is easy to understand but becomes expensive quickly, while Kadane's algorithm remains fast as the input size increases.
