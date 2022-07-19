- ## Sandbox
	- [[ioi-isolate]]
- ## [[Docker]]
	- ### Development
	- ```bash
	  docker run -itd --privileged -p 8000:8000 -v ~/Desktop/dev/judger:/app  --name compiler youmin1017/compilers
	  ```
	- Building Judger
	- ```bash
	  docker build -t youmin1017/judger .
	  ```
- ## FastAPI
	- ### Submit Code
	- ```json
	  {
	  "problem_id": "string",
	  "lang": "c",
	  "source": "string",
	  "input_path": "string",
	  "ans_output_path": "string"
	  }
	  ```
	-