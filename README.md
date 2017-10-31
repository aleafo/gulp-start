# gulp-start
gulp 开发环境脚手架


# start
```bash
cnpm i
gulp
```

# intro

使用方法：

- 1. 首先需具备node环境，以及package.json文件，建议安装cnpm（可自行搜索如何安装cnpm）；
- 2. 在当前目录打开cmd，运行 cnpm install 安装所有依赖
- 3. 定义项目目录的结构，例如
```bash
www
    examples => 示例html文件
    static
        css
        img
        js
        sass => sass源文件，将编译为css并输出到 css文件夹
```
- 4. 配置目录变量
在本文件中定义变量，例如
```javascript
//变量名即为命令号传入的参数值，参数名为 dir
var yxsm = {

    //basedir 代表相对于 node_modules ，项目的目录，也是根目录
    basedir : './', 

    // sass文件目录，相对于项目根目录
    sassdir : 'static/sass/',

    //sass编译后输出的文件目录
    cssdir  : 'static/css/'
}
```
- 5. 定义好以上变量后，在命令行运行

```bash
gulp
```
即可启动项目，其中项目根目录默认为 index.html  如果没有建立该文件，可以手动输入文件名

- 6. 与后台联调时，可直接修改配置文件中的 proxyOpt选项，并将 proxyMiddleWare的注释打开。

  <strong>需要重启gulp生效</strong>
