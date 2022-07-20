- ## [[ioi-isolate]] Sandbox
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
		- Testing Json Data
		  ```json
		  {
		    "problem_id": "string",
		    "lang": "c",
		    "source": "#include <stdio.h>\n/*3n+1*/\nvoid math(int n,int *MAX){\n    int count = 1;\n    while(n-1){\n        if(n&1) n = 3*n+1;\n        else    n /= 2;\n        ++count;\n    }\n    if(count > *MAX) *MAX = count;\n}\nint main(){\n    int a,b,i,MAX=1;\n    while(scanf(\"%d%d\", &a,&b) == 2){\n        printf(\"%d %d \", a,b);\n        if(a > b) a^=b^=a^=b;\n        for(i=a; i <= b; ++i)\n            math(i,&MAX);\n        printf(\"%d\\n\", MAX);\n        MAX=1;\n    }\n    return 0;\n}",
		    "input_path": "/home/ubuntu/Home/Desktop/vmshare/judger/tmp/uva_100_input.txt",
		    "ans_output_path": "/home/ubuntu/Home/Desktop/vmshare/judger/tmp/uva_100_input.txt"
		  }
		  ```
	- ### Stringified 3n+1  C code
	- ```
	  "#include <stdio.h>\n/*3n+1*/\nvoid math(int n,int *MAX){\n    int count = 1;\n    while(n-1){\n        if(n&1) n = 3*n+1;\n        else    n /= 2;\n        ++count;\n    }\n    if(count > *MAX) *MAX = count;\n}\nint main(){\n    int a,b,i,MAX=1;\n    while(scanf(\"%d%d\", &a,&b) == 2){\n        printf(\"%d %d \", a,b);\n        if(a > b) a^=b^=a^=b;\n        for(i=a; i <= b; ++i)\n            math(i,&MAX);\n        printf(\"%d\\n\", MAX);\n        MAX=1;\n    }\n    return 0;\n}"
	  ```
-