## 单一文件workers图床.直接把代码copy过去就可以了
###  自带前端界面
###  绑定d1数据库,绑定R2存储
## 演示地址

## https://pichub.51xmi.com
 
 ![pichub 51xmi](./file_36.jpg)
 
- 打开cloudflare CF网站, 
- 点左面的workers and pages. 创建应用程序 
- 创建 workers, 名称处改一个好记的, 占右下角的部署 
- 编辑代码 直接替换
- 设置 增加一个自定义域
- 设置 增加两个变量, 一个DOMAIN = 你r2存储桶的自定义域名, 另一个 APIKEY = 密码
- 设置 绑定,增加d1,增加R2绑定
 



## 可以用如下命令行直接新建D1数据库

第一步, 新建 images 表, 做为记录
CREATE TABLE IF NOT EXISTS images (
    id TEXT PRIMARY KEY,
    original_name TEXT NOT NULL,
    stored_name TEXT NOT NULL UNIQUE,
    size INTEGER,
    mime_type TEXT,
    file_hash TEXT, -- 新增的哈希字段
    upload_time DATETIME DEFAULT CURRENT_TIMESTAMP
);
第二步,index
CREATE INDEX IF NOT EXISTS idx_images_hash ON images(file_hash);
