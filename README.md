# 找了一些代码并写了一些bug

- [@captcha 源码来源](https://github.com/Master-Gao/codecheck)
- [@OCR 识别](https://pypi.org/project/muggle-ocr)
	- [@xp_CAPTCHA](https://github.com/smxiazi/NEW_xp_CAPTCHA)


| 文件夹 | 用途 |
| :--- | :--- |
| [php-traning-captcha](https://github.com/Bin4xin/orc-php-captcha/tree/main/php-traning-captcha) | OCR训练文件夹 |
| [php-captcha-demo](https://github.com/Bin4xin/orc-php-captcha/tree/main/php-captcha-demo) | php验证码参考代码 |
|  [xp_CAPTCHA](https://github.com/Bin4xin/orc-php-captcha/tree/main/php-traning-captcha/xp_CAPTCHA) | OCR - BurPGui 接口 |

## 一、总述

`codecheck php`验证码程序。

## 二、详解

- ①index.html测试文件
- ②CodeFactory.php产生五种图片验证码（即数字验证码、字符验证码、汉字验证码、仿谷歌验证码、算术表达式验证码）文件
- ③CodeCheck.php测试文件（接收index.html文件的异步请求，并判断输入的验证码是否正确）
- ④official.ttf，汉字验证码中汉字所用字体文件
- ⑤t1.ttf，仿谷歌验证码中字符所用字体文件

## 三、php验证码原理

先随机产生验证码上的内容，并将此内容写入session（方便后面校验），再使用php绘图技术绘制带有前面所产生内容的图片，并在图片上加上一些干扰线，最后输出图片。

## 四、OCR Logs

| 时间 | 成功率 | 备注 |
| :--- | :--- | :--- |
| 2021/12/07/10:22:12 CST | 识别率0% | ![截屏2021-12-07 上午10.18.28.png](https://s2.loli.net/2021/12/07/NIkRZrbwKBTe47c.png) |