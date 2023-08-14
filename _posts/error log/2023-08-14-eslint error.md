# 配置eslint commit钩子时的错误
1. lint-staged command is not found 

#### 现象： 
widows下git commit时报错
lint-staged command is not found 

#### 原因：  
lint-staged path 的问题 

#### 解决： 
全局安装lint-staged
```
npm install lint-staged -g
```

2. node版本过低

#### 现象：
windows 下git commit时报错
```
 git -c user.useConfigOnly=true commit --quiet --allow-empty-message --file -
husky > pre-commit (node v14.3.0)
internal/modules/run_main.js:54
    internalBinding('errors').triggerUncaughtException(
                              ^

Error [ERR_UNSUPPORTED_ESM_URL_SCHEME]: Only file and data URLs are supported by the default ESM loader
    at Loader.defaultResolve [as _resolve] (internal/modules/esm/resolve.js:724:11)
    at Loader.resolve (internal/modules/esm/loader.js:97:40)
    at Loader.getModuleJob (internal/modules/esm/loader.js:242:28)
    at ModuleWrap.<anonymous> (internal/modules/esm/module_job.js:50:40)
    at link (internal/modules/esm/module_job.js:49:36) {
  code: 'ERR_UNSUPPORTED_ESM_URL_SCHEME'
}
husky > pre-commit hook failed (add --no-verify to bypass)
```

#### 解决：
node版本v14.3 升级到v14.21