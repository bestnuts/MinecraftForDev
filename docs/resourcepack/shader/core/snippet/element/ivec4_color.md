# 설명
`ivec4으로 RGBA를 받아온다.`
```
ivec4 get_color(sampler2D tex, ivec2 pixel) {
    return ivec4(texelFetch(tex, pixel, 0) * 255.5);
}
```