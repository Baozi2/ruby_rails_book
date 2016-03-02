# Rails config
### 1. config.autoload_paths

```
rails将自动加载该配置下定义的所有常量，默认加载app下的所有目录
config.autoload_paths 是一个Array的实例
使用方式：
    config.autoload_paths += %W(#{config.root}/lib/puff)
说明:  
config.autoload_paths accepts an array of paths from which 
Rails will autoload constants. Default is all directories under app.

```
### 2.config.eager_load_paths 
当config.eager_load = true的时才会立即加载
```
使用方式：
   config.eager_load_paths += %W(#{config.root}/lib/apple)
说明:   
config.eager_load_paths accepts an array of paths from which Rails will
eager load on boot if cache classes is enabled. Defaults to every folder 
in the app directory of the application
```
### 3. autoload_paths 和 eager_load_paths的不同
```
当开启config.eager_load = true的时候 eager_load_paths中的会立即加载执行require
而autoload_paths不会
```
[参考链接](http://stackoverflow.com/questions/19773266/confusing-about-autoload-paths-vs-eager-load-paths-in-rails-4)