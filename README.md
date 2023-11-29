# search-front

## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn serve
```

### Compiles and minifies for production
```
yarn build
```

### Lints and fixes files
```
yarn lint
```

### axios解决跨域
#### 部署axios
```
npm install axios
```
#### 创建axios实例
```
import axios from "axios";
const request = axios.create(
	{ 
		baseURL: "http://localhost:8101", //配置后端host端口
		timeout: 1000 
	}
);
export default request;
```
#### 全局注册axios
```
main.js:
...
import request from "./api/request.js";//引入创建的axios实例
...
app.provide("$axios", request);//全局注入
...
app.config.globalProperties.$axios = request; //注册axios的全局引用
```
#### 在页面中使用axios
https://www.axios-http.cn/docs/req_config

http://www.axios-js.com/zh-cn/docs/#axios-request-config

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
