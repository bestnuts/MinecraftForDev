# 목록
`아직 값이 들어가있지 않은 스코어를 감지합니다.`
```
execute as @a unless score @s id.player = @s id.player store result score @s id.player run return run scoreboard players add #id id.player 1
```