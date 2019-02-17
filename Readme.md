시작하기
========

1. antlr4 , Visitor를 이용해 계산기 만들기
1. 참고 : https://github.com/shmatov/antlr4-calculator
1. 해당 예제를 maven 프로젝트로 변경. maven을 설치 후 콘솔에서 실행될 수 있도록 해야합니다.
1. antlr4 , 디자인패턴중 Visitor패턴을 공부 후 코드를 분석하세요.

Run
====
 
- clean goal 실행
 mvn clean
 
 - 아래의 명령을 수행하면 src/main/antlr4 아래의 g4파일을 읽어들여 target/generated-sources/antlr4 에 파일을 생성
 mvn antlr4:antlr4
 
 - 빌드 수행
 mvn package
 
 - 실행 
 
mvn -e exec:java -Dexec.mainClass="kr.co.sunnyvale.calc.Run"
 
 
 - 키보드로 아래의 내용을 입력 후 마지막줄에 EoF 입력을 해야 결과가 나옵니다. (ctrl+D or ctrl+Z)
 
 ```
 a = 1+2
 b = a^2
 c = a + b * (a - 1)
 a + b + c
 ```
 
 
 Result should be equal 33.0
