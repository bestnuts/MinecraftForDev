# 틱 과 로드
`data/minecraft/tags/function/`  
여기서 tick 과 load 로 다양한 함수를 순서에 알맞게 호출한다.  
tick 과 load 는 각자 한 함수만을 호출하여 최상위 root(뿌리)가 되어야 한다.  
`tick.json 안 좋은 예시 mctd 참고`  
```
{
    "values": 
    [
        "game:main",
        "tower:main",
        "map:main",
        "enemy:main"
    ]
}
```
`tick.json 좋은 예시`  
```
{
    "values": [
        "main:tick/core"
    ]
}
```
load 도 tick 과 마찬가지로 설계하면 좋다.  
다음에 이야기할 최상위 함수 호출을 알아보며 이게 왜 좋은 예시였는지 알아보자.  

# 요약
tick 과 load 는 각자 한 함수만을 호출하며 그 안에 모든 것을 담아내야 한다.  