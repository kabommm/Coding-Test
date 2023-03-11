# 문제
- 링크: 
<https://www.acmicpc.net/problem/15552>

# 소스코드
```
import java.io.*;
import java.util.*;
public class Main {

	public static void main(String[] args) throws IOException {

		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
		int n = Integer.parseInt(br.readLine());
		
		for (int i = 0; i < n; i++) {
            StringTokenizer st = new StringTokenizer(br.readLine());
            int a = Integer.parseInt(st.nextToken());
            int b = Integer.parseInt(st.nextToken());
            bw.write(a+b + "\n");
		}
		bw.flush();
	}
}
```
# 풀이
- 입력때 Scanner 출력때 System.out.print 둘중 하나만 사용하더라도 시간 초과가 나므로 입력엔 BufferedReader를 사용하고 출력엔 BufferedWriter나 StringBuilder를 사용

- 하지만 I/O클래스의 BufferedReader를 사용할 경우 단점이 있는데 다음과 같다.

  1.IOException의 예외처리가 필요하다.(main함수 우측에 throws IOException를 통해서 예외처리를 해야 한다.)
  
  2.입력 데이터들이 String으로 반환된다.
  
  3.데이터들을 재가공(데이터를 split 후 형 변환 등등...)

- main함수 우측에 throws IOException를 통해서 예외처리(1번 문제 해결)

- readLine을 통해 한 줄씩 입력을 받은 것을 기준으로 StringTokenizer(3번 문제 해결)을 통해 데이터를 분할하고 
형 변환(2번 문제 해결)을 해서 bw.write()로 버퍼에 씁니다(화면에 바로 출력 x).

- for문을 돌고 나면 bw.flush()로 버퍼에 있는 데이터들을 한 번에 출력하게 됩니다.

- I/O 클래스의 ![Reader / Writer 메소드](https://github.com/kabommm/TIL/blob/main/Language/JAVA/IO.md)와 ![StringTokenizer 클래스](https://github.com/kabommm/TIL/blob/main/Language/JAVA/StringTokenizer.md) 참고
