# 문제
- 링크: 
<https://www.acmicpc.net/problem/10757>

# 소스코드
```
import java.math.BigInteger;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        BigInteger A = sc.nextBigInteger();
        BigInteger B = sc.nextBigInteger();

        System.out.println(A.add(B));

    }
}
```
# 풀이
- 주어진 수가 long의 범위보다 크므로 ![BigInteger](https://github.com/kabommm/TIL/blob/main/Language/JAVA/Scanner.md) 사용
