# 문제
- 링크: 
<https://school.programmers.co.kr/learn/courses/30/lessons/120887>

# 소스코드1
```
class Solution {
    public int solution(int i, int j, int k) {
        int answer = 0;
        for(int m=i; m<=j; m++){
            int num = m;
            
            while(num!=0){
                if(num%10==k){
                    answer++;
                    num /= 10;
                }else{
                    num /= 10;
                }
            }
        }
        return answer;
    }
}
```

# 소스코드2
```
class Solution {
    public int solution(int i, int j, int k) {
        int answer = 0;

        for(int n = i; n<=j; n++){
            String str = n+"";
            for(int l = 0; l<str.length(); l++){
                if(str.charAt(l)-'0'==k) answer++;
            }

        }

        return answer;
    }
}
```
# 풀이1
- while 반복을 통해 10으로 나눠 자릿수마다 k가 있으면 answer++

# 풀이2
- +""을 이용하여 문자열을 생성하고 문자열의 길이만큼 반복문을 생성
- 반복문 내에서 charAt()과 - '0'을 통해 문자열을 정수로 만든 값이 k일때 answer++

