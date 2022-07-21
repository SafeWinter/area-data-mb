# area-data-mb

适用于慢病系统的中国行政区域数据(含港澳台)，基于 `area-data` 模块改造，精确到区县。数据为 2022 年版本。

## v1.0.0

- 重新改造区市县模块 `pcaa.js`，封装为适用于贵阳项目的行政区划版本。

## doc

[详见 area-data 文档页](https://github.com/dwqs/area-data#readme)

## Installation

Install the pkg with npm:

```
npm install area-data-mb --save
```

or yarn

```
yarn add area-data-mb
```

or bower

```
bower install area-data-mb
```

## 获取数据

```
// v5之前的版本
import AreaData from 'area-data-mb';

// v5及之后的版本
import { pca, pcaa } from 'area-data-mb';
// 可以根据需要按需引入：
import PCA from 'area-data-mb/pca';
import PCAA from 'area-data-mb/pcaa';

pca['86'] // 等同于 AreaData['86']
// 所有省份：{'110000': '北京市', '120000': '天津市', '130000': '河北省', ...}

pcaa['130000'] // 等同于 AreaData['130000']
// 对应省份的所有城市：{'130100': '石家庄市', '130200': '唐山市', '130300': '秦皇岛市', ...}

pcaa['130200'] // 等同于 AreaData['130200']
// 对应市的所有县区：{'130201': '市辖区', '130202': '路南区', '130203': '路北区', ...}

### v1
AreaData['130202']
// 对应县区的所有街道：{'130202001000': '学院南路街道', '130202002000': '友谊街道', ...}
```

> 官方数据(截止到 2016.07.31): [城乡区域划分](http://www.stats.gov.cn/tjsj/tjbz/tjyqhdmhcxhfdm/2016/index.html)

**数据来源：** 最新省市区数据来自 [area-puppeteer](https://github.com/dwqs/area-puppeteer/).

## LICENSE

MIT
