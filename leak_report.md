# Leak report

Memory leaks happen when some memory is allocated but is then not freed up.

So when memory is allocated like below:
```
  result = calloc(size-num_spaces+1, sizeof(char));
```
It needs to be freed by using 
```
free(result);
```

Otherwise, the memory that was allocated keeps taking up memory even though it is not being used.