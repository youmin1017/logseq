tags:: #python #async

- ## Semaphore
	- #+BEGIN_QUOTE
	  A semaphore manages an internal counter which is decremented by each acquire() call and incremented by each release() call. The counter can never go below zero; when acquire() finds that it is zero, it blocks, waiting until some task calls release().
	  
	  The optional value argument gives the initial value for the internal counter (1 by default). If the given value is less than 0 a ValueError is raised.
	  #+END_QUOTE
	- ### Test Code
		- ```python
		  from asyncio import Semaphore
		  import asyncio
		  
		  
		  sem = Semaphore(10)
		  
		  
		  async def sem_test():
		      async with sem:
		          await asyncio.sleep(2)
		          print(sem)
		  
		  
		  async def sem_test2():
		      async with sem:
		          await asyncio.sleep(1)
		          print(sem, '2')
		  
		  
		  async def main():
		      await asyncio.gather(
		          sem_test(),
		          sem_test2()
		      )
		  
		  
		  asyncio.run(main())
		  
		  ```
-