tags:: #python #async

- ## Semaphore
	- #+BEGIN_QUOTE
	  A semaphore manages an internal counter which is decremented by each acquire() call and incremented by each release() call. The counter can never go below zero; when acquire() finds that it is zero, it blocks, waiting until some task calls release().
	  
	  The optional value argument gives the initial value for the internal counter (1 by default). If the given value is less than 0 a ValueError is raised.
	  #+END_QUOTE
	- ### Test Code
		-
-