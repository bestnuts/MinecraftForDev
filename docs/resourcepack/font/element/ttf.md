# 설명
TrueTypeFont 를 마인크래프트 내로 불러오기 위해 쓰입니다.  

# 포맷
```
type : ttf
file : .ttf 리소스 경로
oversample : 렌더링될 해상도입니다.
shift : 두 개의 정수로 구성된 배열입니다.
    : 수평으로의 이동 위치입니다.
    : 수직으로의 이동 위치입니다.
size : 출력 크기를 결정합니다.
skip : 문자 혹은 문자로 구성된 배열로 불러올 때 제외할 문자들입니다.
```

# 예시
`커스텀 폰트 예시`
```
{
    "providers": [
		{
            "type": "ttf",
            "file": "minecraft:unifont.ttf",
            "oversample": 8,
            "shnift": [0,0],
            "size": 8,
			"skip": ["1", "2"]
        }
    ]
}

```