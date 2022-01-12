# nrm-manage-registry
nrm 管理多个 registry 源

## nrm (npm registry manager )是npm的镜像源管理工具，有时候国外资源太慢或访问不了，使用这个就可以快速地在 npm 源间切换

### 1 全局安装

```
npm install -g nrm
```

### 2 查看是否安装成功

```
nrm --version
```

或

```
nrm -V
```

### 3 查看可选择的全部源列表

```
nrm ls
```

结果如下

```
* npm ---------- https://registry.npmjs.org/
  yarn --------- https://registry.yarnpkg.com/
  tencent ------ https://mirrors.cloud.tencent.com/npm/
  cnpm --------- https://r.cnpmjs.org/
  taobao ------- https://registry.npmmirror.com/
  npmMirror ---- https://skimdb.npmjs.com/registry/
```

#### 注意: "*" 代表当前 npm 源指向的仓库

### 4 切换使用源

```
nrm use taobao
```

### 5 添加使用源,语法如下: nrm add [registry] [url]

#### 其中，registry 为源名，url为源地址。 比如：添加一个公司私有的npm源，源地址为：http://mtnpm.bd.com ; 源名为 mt（随意取）。

```
nrm add mt http://mtnpm.bd.com
```

### 5 查看源的主页

```
nrm home taobao
```

### 6 删除使用源: nrm del [registry]

```
nrm del taobao
```

### 7 测试使用源速度

```
nrm test [registry]
```

### 8 查看 npm 源地址

```
npm config list
```

```
npm config get registry
```

### 9 npm 修改registry源地址

```
npm config set registry https://registry.npm.taobao.org/
```

### 10 安装包使用特定源

#### 全部使用特定源安装
```
npm install --registry=https://registry.npm.taobao.org
```
#### 安装一个或者多个包使用特定源

```
npm install logo  --registry=https://registry.npm.taobao.org
```



