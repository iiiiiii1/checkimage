checkimage
---------------
本项目是一个图片鉴黄`api`接口，支持`jpg`、`png`、`jpeg`格式文件，参考[nsfwjs][1]。

接口地址
---------------

    https://checkimage.querydata.org/api

使用示例
---------------

    curl https://checkimage.querydata.org/api -F "image=@/root/xx.png"

返回信息：

    [
        {
            "className": "Neutral",
            "probability": 0.9277840852737427
        },
        {
            "className": "Drawing",
            "probability": 0.07143104821443558
        },
        {
            "className": "Hentai",
            "probability": 0.0007780276937410235
        },
        {
            "className": "Porn",
            "probability": 0.000005075656645203708
        },
        {
            "className": "Sexy",
            "probability": 0.0000018030658566203783
        }
    ]
类型参考：

    #指数越高，越接近该类型
    Drawing 和 Neutral：均为正常图片
    hentai：二次元类型的暴露图片指数
    sexy：露点图片的指数
    porn：就是色情图片的指数

  [1]: https://github.com/infinitered/nsfwjs
