# Problem-Solving

##### PS 입문자를 위한 간단 안내서



## 목차

1. [온라인 저지 채점 결과](#온라인-저지-채점-결과)
2. [언어별 빠른 입출력 방법](#언어별-빠른-입출력-방법)
3. [시간 복잡도](#시간-복잡도)
4. [공간 복잡도](#공간-복잡도)
5. [BOJ](#BOJ)
6. [Codeforces](#Codeforces)



# 온라인 저지 채점 결과

### 기다리는 중, Pending

채점을 기다리는 중입니다. 조금 기다리면 채점 결과를 받을 수 있습니다.



### 채점 중, Judging

채점을 하는 중입니다.



### 맞았습니다!!, Accept, Correct

제출한 프로그램이 채점 서버에 준비된 모든 데이터를 맞은 경우에 받게 됩니다.



### 틀렸습니다, Wrong Answer, WA

제출한 프로그램의 출력 결과가 채점 서버에 준비된 정답과 다른 경우입니다.



### 시간 초과, Time Limit Exceeded, Time Limit, TLE

프로그램이 제한된 시간 이내에 끝나지 않은 경우입니다. 시간 제한을 초과하면 실행을 즉시 중단합니다. 따라서, 정답이 맞았는지 틀렸는지는 알 수 없습니다.



### 메모리 초과, Memory Limit Exceeded, Memory Limit, MLE

프로그램이 허용된 메모리보다 많은 메모리를 사용한 경우입니다. 시간 초과와 마찬가지로, 메모리 제한을 초과하면 실행을 즉시 중단합니다. 즉, 메모리 초과도 정답이 맞았는지 틀렸는지는 알 수 없습니다.



### 런타임 에러, Runtime Error

프로그램이 비정상적으로 종료한 경우입니다. Exit code가 0이 아닌 경우, 잘못된 메모리 주소를 참조하여 `segmentation fault`가 발생한 경우가 대표적입니다.



### 컴파일 에러, Compile Error

컴파일에 실패한 경우입니다. 경고(Warning)가 있어도 컴파일에 성공하면 이 결과를 받지 않습니다. 컴파일 에러 글씨를 클릭하면 컴파일 에러 메시지를 볼 수 있습니다.



[참고 사이트](https://www.acmicpc.net/help/judge)





# 언어별 빠른 입출력 방법

### C

scanf/printf는 충분히 빠릅니다.



### C++

- C++에서도 scanf/prinf로 입출력을 하신다면 충분히 빠릅니다. 단, cin/cout을 사용할 경우 아래 내용을 참고하세요.
- endl은 개행문자를 출력할 뿐만 아니라 출력 버퍼를 비우는 역할까지 하는데, 버퍼를 비우는 작업이 매우 느립니다. PS에서는 버퍼를 관리할 필요는 없기때문에 endl을 '\n'으로 바꾸는 것만으로도 굉장한 속도 향상이 나타납니다.
- cin.tie(NULL)은 cin과 cout의 묶음을 풀어서 입출력 요청이 올 때 서로의 버퍼를 비우지 않도록 합니다. 기본적으로 cin으로 읽을 때 먼저 출력 버퍼를 비우는데, PS에서는 이 작업이 중요하지 않습니다. 대량의 입력과 출력이 번갈아서 발생하는 경우에 필수적입니다.
- ios_base::sync_with_stdio(false)는 C와 C++의 버퍼를 분리합니다. 이것을 사용하면 cin/cout이 더 이상 stdin/stdout과 맞춰 줄 필요가 없으므로 속도가 빨라집니다. 단, 버퍼가 분리되었으므로 cin과 scanf, gets, getchar 등을 같이 사용하면 안 되고, cout과 printf, puts, putchar 등을 같이 사용하면 안 됩니다.

main 함수 첫 줄에 아래 코드를 넣고 사용하면 입출력으로 인한 시간 초과를 예방할 수 있습니다.

```
ios::sync_with_stdio(false);
cin.tie(0);
cout.tie(0);
```

[참고 사이트](https://su-m.tistory.com/7)



### Java

BufferedWriter 외에도, StringBuilder로 출력을 모아 놓았다가 그 String을 System.out.println하는 방법도 있습니다.



### Python

문자열 자체를 변수에 저장할 때는 rstrip을 사용합니다. 개행문자가 맨 끝에 들어와도 int 변환이나 split()은 그대로 할 수 있기 때문에 문자열 자체를 저장하고 싶은 상황이 아니라면 입력받은 문자열을 바로 처리해도 됩니다.

int(sys.stdin.readline()), sys.stdin.readline().split()



[참고 사이트](https://www.acmicpc.net/board/view/22716)





# 시간 복잡도

[참고 사이트](https://www.weeklyps.com/entry/시간복잡도)





# 공간 복잡도

공간복잡도는 프로그램의 메모리 사용량을 분석하는 것입니다.

간단하게 사용한 배열의 크기 * (해당 자료형의 크기) 의 총합으로 계산할 수 있습니다.

대부분의 문제에서 메모리 제한을 넉넉하게 주기 때문에 크게 사용한 메모리들을 중심으로 어림잡아 계산하면 비교적 빠르게 공간 복잡도를 알아볼 수 있습니다.





# BOJ

백준 온라인 저지

프로그래밍 문제를 풀고 온라인으로 채점받을 수 있는 곳입니다.

[solved.ac](https://solved.ac/) 사이트를 이용하면 BOJ 문제 난이도, 태그를 보거나 자신의 BOJ 티어를 확인해볼 수 있습니다.





# Codeforces

코드포스

[참고 사이트](https://m.blog.naver.com/PostView.nhn?blogId=qkfldkeh&logNo=220722548956&proxyReferer=https%3A%2F%2Fwww.google.com%2F)

