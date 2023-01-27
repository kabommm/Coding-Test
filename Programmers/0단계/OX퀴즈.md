# 문제
- 링크: 
<https://school.programmers.co.kr/learn/courses/30/lessons/120907>

# 소스코드
```
class Solution {
    public String[] solution(String[] quiz) {
        String[] answer = new String[quiz.length];
        for (int i = 0; i < quiz.length; i++) {
            String[] arr = quiz[i].split(" ");
            if (arr[1].equals("+")) {
                if (Integer.parseInt(arr[0]) + Integer.parseInt(arr[2]) == Integer.parseInt(arr[4])) {
                    answer[i] = "O";
                } else {
                    answer[i] = "X";
                }
            } else if (arr[1].equals("-")) {
                if (Integer.parseInt(arr[0]) - Integer.parseInt(arr[2]) == Integer.parseInt(arr[4])) {
                    answer[i] = "O";
                } else {
                    answer[i] = "X";
                }
            }
        }
        return answer;
    }
}
```
# 풀이
- 제공받은 quiz의 길이만큼 반환할 배열을 생성
- split()을 통해 quiz[i]의 문자열을 배열로 생성
- 조건문을 이용해 +인 경우와 -인경우 안에서 각각 연산 값이 맞으면(이때 Integer.parseInt로 변환해서 정수형으로 계산)O 틀리면 X의 조건문 이용
