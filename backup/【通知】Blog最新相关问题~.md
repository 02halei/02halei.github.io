# 前言

> 关于Github将暂停使用Ubuntu20.4并更新版本系统导致博客`Actions`无法正常完成
>
> 本文是相应的解决办法，将更改为使用Ubuntu24.4

# 问题解决

## 更改配置文件

**打开博客的仓库地址并在 `Code`中打开`.github/workflows`文件夹**

我们更该Gmeek的workflows相关文件`Gmeek.yml`

【示例如下】

[Gmeek.yml](https://github.com/02halei/02halei.github.io/blob/main/.github/workflows/Gmeek.yml)

## 更改第*13*行为

```
runs-on: ubuntu-24.04
```

## 更改第*74*行为

```
runs-on: ubuntu-24.04
```

**保存后手动全局生成一次即可解决问题~**