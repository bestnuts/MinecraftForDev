# 설명
`대상이 GUI 에서 렌더링되고 있는지 감지한다.`
```
bool isgui(mat4 projMat) {
    return projMat[2][3] == 0.0;
}
```