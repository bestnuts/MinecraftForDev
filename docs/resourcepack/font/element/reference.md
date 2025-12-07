# 설명
정의된 다른 폰트 파일을 참조할 때 쓰입니다.  

# 포맷
```
type : reference
id : 리소스 경로입니다.
```

# 예시
`assets/minecraft/font/default.json 전체 참고`
```
{
    "providers": [
        {
            "type": "reference",
            "id": "minecraft:include/space"
        },
        {
            "type": "reference",
            "id": "minecraft:include/default",
            "filter": {
                "uniform": false
            }
        },
        {
            "type": "reference",
            "id": "minecraft:include/unifont"
        }
    ]
}
```