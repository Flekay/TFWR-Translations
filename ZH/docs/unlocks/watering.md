# 浇水
植物在浇水后生长得更快。地面的水位范围从 `0` 到 `1`。
函数 `get_water()` 返回它所在位置的地面水位。

植物的生长速度随着水位线性增加：水位为 0 时，植物生长速度为 1 倍；水位为 1 时，速度为 5 倍。

地面会随着时间变干：平均而言，每秒会失去当前水量的 1%，但这一数字会有所波动。保持高水位会比保持低水位消耗更多的水。

你可以给你的植物浇水。每 10 秒你的库存里会自动增加一桶水。
升级 `Unlocks.Watering` 每隔 10 秒会多给你一桶水。

一桶水包含 `0.25` 水。

在任意地面上调用 `use_item(Items.Water)` 来给地面浇水。