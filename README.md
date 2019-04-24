## renren-fast-vue
- renren-fast-vue基于vue、element-ui构建开发，实现[renren-fast](https://gitee.com/renrenio/renren-fast)后台管理前端功能，提供一套更优的前端解决方案
- 前后端分离，通过token进行数据交互，可独立部署
- 主题定制，通过scss变量统一一站式定制
- 动态菜单，通过菜单管理统一管理访问路由
- 数据切换，通过mock配置对接口数据／mock模拟数据进行切换
- 发布时，可动态配置CDN静态资源／切换新旧版本
- 演示地址：[fast.demo.renren.io](http://fast.demo.renren.io) (账号密码：admin/admin)

## 说明文档

 **前端部署**
 - 本项目是前后端分离的，还需要部署前端，才能运行起来
 - 前端下载地址：https://gitee.com/renrenio/renren-fast-vue
 - 前端部署文档：https://gitee.com/renrenio/renren-fast-vue/wikis/Home
 - 前端部署完毕，就可以访问项目了，账号：admin，密码：admin


开发环境，需要安装node8.x最新版
 - 安装依赖
    npm install
 - 启动服务
    npm run dev
    
生成环境，打包并把dist目录文件，部署到Nginx里

 - 构建生产环境(默认) 
 npm run build
    <br/>
 - 构建测试环境
    npm run build --qa
     <br/>
 - 构建验收环境
    npm run build --uat
     <br/>
 - 构建生产环境
    npm run build --prod
     <br/>
 - 安装Nginx，并配置Nginx server {
        listen       80;
        server_name  localhost;
    location / {
    root E:\\renren-fast-vue; index index.html index.htm;
    } }
     <br/>
 - 启动Nginx后，访问如下路径即可 http://localhost
