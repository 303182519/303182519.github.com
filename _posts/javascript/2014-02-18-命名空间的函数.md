---
layout: post
tagline: "项目无Bug之日即是下线之时"
title: 命名空间的函数
category : javascript
---






    var GLOBAL = GLOBAL || {};
    //处理命名空间的函数
    GLOBAL.namespace = function(str) {
	    var arr = str.split("."),
	    	o = GLOBAL;
	    for (i = (arr[0] == "GLOBAL") ? 1 : 0; i < arr.length; i++) {
	    	o[arr[i]] = o[arr[i]] || {};
	    	o = o[arr[i]];
	    }
    }
    //注册一个模块(即给一个模块划分一个命名空间)
    GLOBAL.namespace("Module1");
    //给Module1添加一个print方法
    GLOBAL.Module1.print = function(msg){
    console.log(msg);
    }
    //调用Module1的print函数
    GLOBAL.Module1.print("1");  //1
    //也可以这样调用
    GLOBAL.Module1.print.call(null, "3"); //3