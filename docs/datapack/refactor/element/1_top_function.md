# 최상위 함수
`data/main/function/load/`  
core 함수에는 데이터팩 로드시 호출되어야 하는 모든 함수들의 최상위 뿌리이다.  
해당 데이터팩에서 쓰일 모든 규칙 및 스코어 오브젝트들을 초기화해 줘야 한다.  
`core.mcfunction 예시 mctd 참고`  
```
function main:load/forceload
function main:load/gamerule
function main:load/team
function main:load/score-objective
function main:load/score-constant
```

`data/main/function/tick/`  
core 함수에는 매 틱마다 호출되어야 하는 모든 함수들의 최상위 뿌리이다.  
만약 수많은 엔티티가 쓰이는 프로젝트라면 type=<태그> 를 기반으로 적절히 묶어줘야 한다.  
또한 저장이 필요 없는 임시 데이터들을 주기적으로 제거해주는게 좋다.  
`core.mcfunction 예시 mctd 참고`  
```
execute store result score #gametime V run time query gametime

execute as @e[type=#api:ticking] at @s run function main:core/entity/shared/main
execute as @e[type=item_display,tag=entity.bullet] at @s run function main:core/entity/bullet/main
data remove storage mctd main.instance
```
눈치챘을지 모르겠지만 as @e 가 두 번 쓰였다.  
이 부분에 대해서는 다음에 이야기할 함수 호출 우선순위에 대해서 알아보며 이해한다.  

# 요약
load 는 데이터팩에 쓰일 데이터들을 초기화 시켜줘야 하고  
tick 은 매 틱마다 쌓일 데이터들을 한꺼번에 초기화 시켜줘야 한다.  