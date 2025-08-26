# 설명
hexfont 를 불러오기 위해서 쓰입니다.

# 포맷
```
type : unihex
hex_file : .hex 파일이 담긴 .zip 리소스 경로
size_overrides :
    __range : 범위명
    from : 재정의 시작 문자입니다.
    to : 재정의 끝 문자입니다.
    left : 범위 내 가장 왼쪽에 있는 글리프 위치입니다.
    right : 범위 내 가장 오른쪽에 있는 글리프 위치입니다.
```

# 예시
`assets/minecraft/font/include/unifont.json 1줄 참고`
```
{
    "providers": [
        {
            "type": "unihex",
            "hex_file": "minecraft:font/unifont_jp.zip",
            "size_overrides": [
                {
                    "__ranges": [
                        "Enclosed CJK Letters and Months",
                        "CJK Compatibility",
                        "CJK Unified Ideographs Extension A",
                        "Yijing Hexagram Symbols",
                        "CJK Unified Ideographs"
                    ],
                    "from": "\u3200",
                    "to": "\u9FFF",
                    "left": 0,
                    "right": 15
                },
                {
                    "__ranges": [
                        "CJK Compatibility Ideographs"
                    ],
                    "from": "\uF900",
                    "to": "\uFAFF",
                    "left": 0,
                    "right": 15
                }
            ],
            "filter": {
                "jp": true
            }
        }
    ]
}

```