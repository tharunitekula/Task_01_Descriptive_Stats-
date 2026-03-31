# Comparison: Pure Python vs Pandas

This run shows that both the pure Python script and the Pandas script are working at a basic level, but they are both being fed the wrong or malformed input. The pure Python version interprets the file as one categorical column with 11 distinct values, while Pandas reports a `(11, 1)` DataFrame with no usable numeric columns. That agreement is useful because it confirms that the problem is not just one script — the input file itself is the issue.

## Pure Python

The pure Python script makes the parsing issue very obvious. It shows one column, one inferred type, and a list of values that look like port names rather than dataset fields. Because the script handles type inference manually, it is easier to see that nothing in the file resembles the rich row-and-column structure expected for the assignment.

One strength of the pure Python approach is that it exposes malformed input immediately. There is no hidden preprocessing or silent correction, so if the file is wrong, the output looks wrong right away. That makes the script useful for debugging data-loading problems.
## Pandas

The Pandas script is shorter and more concise, but it reaches the same conclusion: the file is not giving meaningful analytical output. Pandas shows the shape, dtype, and missingness clearly, and `describe()` confirms that there are no usable numeric summaries. It is very efficient for confirming structural problems in a dataset.

The downside is that Pandas can make a malformed file look somewhat orderly at first glance, because it still loads as a DataFrame. Without checking the actual values, it would be easy to miss the fact that the file is not the intended dataset.

## Main Lesson

In this case, both approaches agree that the input data is unusable for the assignment in its current form. The pure Python version is better for exposing exactly how the values are being interpreted, while the Pandas version is better for quickly confirming shape, dtypes, and missing values.

The most important conclusion is that I need to replace the current file with the correct political ads CSV before making any final findings. Once the correct dataset is loaded, both scripts should produce meaningful descriptive statistics and a real comparison of results.
