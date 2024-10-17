# 문자열 덧셈 계산기

## 기능 요구 사항
입력한 문자열에서 **숫자**를 추출하여 더하는 계산기를 구현한다.
- 쉼표(,) 또는 콜론(:)을 **구분자**로 가지는 문자열을 전달하는 경우 구분자를 기준으로 분리한 각 숫자의 합을 반환한다.
    - 예: "" => 0, "1,2" => 3, "1,2,3" => 6, "1,2:3" => 6
- 앞의 기본 구분자(쉼표, 콜론) 외에 **커스텀 구분자**를 지정할 수 있다. 커스텀 구분자는 문자열 앞부분의 "//"와 "\n" 사이에 위치하는 문자를 커스텀 구분자로 사용한다.
    - 예를 들어 "//;\n1;2;3"과 같이 값을 입력할 경우 커스텀 구분자는 세미콜론(;)이며, 결과 값은 6이 반환되어야 한다.
- 사용자가 잘못된 값을 입력할 경우 IllegalArgumentException을 발생시킨 후 애플리케이션은 종료되어야 한다.

## 기능 목록
1. 구분자로 나누어 숫자 더하기
	1. 구분자로 나누어 배열로 저장
		1. 배열 중 **정수** 이외의 문자가 포함될 시 예외 처리
	2. 나누어진 배열의 합 구하기
2. 커스텀 구분자 추가하기
	1. "//"와 "\n" 사이에 위치하는 문자를 커스텀 문자로 추가
	2. 커스텀 추가 규칙 위반 시 예외 처리