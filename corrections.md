# Page 130
## `str_replace_all()` verus `str_replace()`

On this page there is an inadevertent error. The error wasn't picked up because in this particulalr case the code generates the same outcome.

The book code:
```r
messy %>%
  mutate(income_before = str_replace(income_before, "[$]", ""))
```

Should read:

```r
messy %>%
  mutate(income_before = str_replace_all(income_before, "[$]", ""))
```

The difference between `str_replace_all()` and `str_replace()` is that the former replaces all instances, where as the later only replaces the first instance