## 单一文件workers图床.直接copy all to  workers就可以了
### if startswith  upload or file  跳转到tg官方地址. 实现api 苹果捷径上传. 
### 其它情况,可以二选一, 可以跳转到你的网址, 或默认.
## 两个演示地址
## https://pic.51xmi.com  
## https://pichub.51xmi.com
 
 ![ujf](https://pichub.51xmi.com/file/31c49357111e7830858cb.png)
 
- 打开cloudflare CF网站, 
- 点左面的workers and pages. 创建应用程序 
- 创建 workers, 名称处改一个好记的, 占右下角的部署 
- 编辑代码 直接替换
- 设置 触发器, 增加一个自定义域, 再把85,91,120,122行 改成你的自定义域名 就可以了
- - 136 行可以二选一
+ 第二种直接转到你自己的网页界面
+ 
![第二种界面]( https://pichub.51xmi.com/file/fc4416675856c796fdbd1.png)
