# 문제
- 링크: 
<https://school.programmers.co.kr/learn/courses/30/lessons/120905>

# 소스코드1
```
import java.util.*;
class Solution {
    public int[] solution(int n, int[] numlist) {
        return Arrays.stream(numlist).filter(i -> i%n==0).toArray();
    }
}
```

# 소스코드2
```
import java.util.*;
class Solution {
    public int[] solution(int n, int[] numlist) {
        List<Integer> list = new ArrayList<>();
        for(int i = 0; i<numlist.length; i++)
            if(numlist[i]%n==0) 
                list.add(numlist[i]);
        
        return list.stream().mapToInt(i->i).toArray();
    }
}
```

# 풀이
## 소스코드1
- Arrays.stream() → int 배열을 stream으로 변환
- filter()를 사용해 n으로 나뉘어지는 요소만 stream에 남긴다
- toArray()으로 배열로 변환

## 소스코드2

- Integer List를 생성
- 반복문에서 조건에 맞는 요소를 List에 추가
- List를 Stream으로 바꿨다가 배열로 바꿔 제출
