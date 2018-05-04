自定义了三个对象
- `Message` 表示弹幕信息：弹幕ID(id)，弹幕内容(msg)，弹幕坐标(px, py)，弹幕长度(width)
- `Pipe` 表示展示信息的管道，为`Message`信息集合
- `BarrageQueue` 表示管理管道的池子，默认设置三个管道

### `Message`
- `setWidth`: 设置 `Message` 宽度

### `Pipe`
- `addBarrage`: 生成 `Message`实例，并初始化 `Message`坐标以及长度
- `clearDisabledMsg`: 清除超出边界(`msg`宽 + `px` <= 0)的`Message`
- `deleteBarrage`: 删除指定`Message`
- `isEmpty`: 判断管道内是否为空
- `clear`: 清除所有弹幕

### `BarrageQueue`
- `init`: 生成三个`Pipe`实例，并把数据平均分配至三个管道
- `clearPipe`: 清除`Pipe`内失效的数据
- `isAllEmpty`: 判断三个`Pipe`是否都为空
    