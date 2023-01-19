# 문제
- 링크: 
<https://school.programmers.co.kr/learn/courses/30/lessons/120886>

# 소스코드
```
import java.util.*;
class Solution {
    public int solution(String before, String after) {
      
        String[] be = before.split("");
        String[] af = after.split("");
        Arrays.sort(be);
        Arrays.sort(af);
        String bes = Arrays.toString(be);   
        String afs = Arrays.toString(af);   
        if( bes.equals(afs) ){
            return 1;
        }else{
            return 0;
        }
    }
}
```
# 풀이
- split()메소드를 사용해 문자열을 배열로 변경
- 두 문자열이 순서를 맞춰주면 같을지 확인하기 위해 Arrays.sort()를 사용해 오름차순으로 맞춰준다.(이 함수 사용을위해 배열로 변경한 것이다.)
- Arrays.toString()를 사용해 배열을 다시 문자열로 변경
- equals()를 사용해 두 문자열을 비교하고 같으면 1 다르면 0 
