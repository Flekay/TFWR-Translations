# Pumpkins
[Pumpkins](objects/pumpkin)는 경작된 흙에서 당근처럼 자랍니다. 심을 때는 당근이 필요합니다.

정사각형 안의 모든 호박이 완전히 자라면 하나로 합쳐져 거대한 호박이 됩니다. 불행히도 호박은 완전히 자라면 20%의 확률로 죽을 수 있으므로, 합쳐지길 원한다면 죽은 호박을 재배해야 합니다.

거대한 호박의 수확량은 호박의 크기에 따라 다릅니다.

1x1 호박은 `1*1*1 = 1`개의 호박을 제공합니다.
2x2 호박은 `4`개 대신 `2*2*2 = 8`개의 호박을 제공합니다.
3x3 호박은 `9`개 대신 `3*3*3 = 27`개의 호박을 제공합니다.
4x4 호박은 `16`개 대신 `4*4*4 = 64`개의 호박을 제공합니다.
`n`x`n` 호박은 `n >= 5`에 대해 `n*n*5`개의 호박을 제공합니다.

완전한 배수를 얻기 위해 최소한 5x5 크기의 호박을 얻는 것이 좋습니다.

이는 심지어 모든 정사각형의 타일에 호박을 심어도, 하나의 호박이 죽어 거대한 호박이 자라지 못하게 될 수 있음을 의미합니다.