# 설명
`ivec4으로 RGBA를 받아온다.`
```
ivec4 get_color(sampler2D tex, vec2 pixel) {
    return ivec4(texture(tex, pixel) * 255.5);
}
```