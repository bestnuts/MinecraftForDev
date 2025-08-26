# 함수 우선순위
`data/main/function/tick/core.mcfunction 예시 mctd 참고`  
```
execute as @e[type=#api:ticking] at @s run function main:core/entity/shared/main
execute as @e[type=item_display,tag=entity.bullet] at @s run function main:core/entity/bullet/main
data remove storage mctd main.instance
```
해당 코드만을 보며 추측해보면 `function main:core/entity/shared/main` 에서 태그 entity.bullet 을 가진  
아이템 디스플레이 엔티티가 생성되어 그 다음 호출에서 해당 엔티티가  
`function main:core/entity/bullet/main` 를 호출하게 되는 구조일 것이다.  
그리고 공통적인 사항으로는 스토리지 mctd main.instance 에 임시 데이터들을 저장했을 가능성이 크다.  
`data/main/function/core/entity/shared/main.mcfunction 예시 mctd 참고` 
```
execute if entity @s[type=player] run return run function main:core/entity/player/main
execute if entity @s[type=block_display] run return run function main:core/entity/shared/display
execute if entity @s[type=marker] run return run function main:core/entity/shared/marker
execute if entity @s[tag=entity.mob] run return run function main:core/entity/mob/main
```
이후 순서에 상관 없이 조건에 알맞는 함수를 호출하며 해당 함수를 벗어나게 된다.  

# 요약
모든 실행에는 순서가 있을 수 밖에 없다. 순서에 대한 의미가 없다면 한꺼번에 묶어서 실행시킨다.  