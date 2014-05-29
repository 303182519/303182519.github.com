---
layout: post
title: node基础：文件系统-文件写操作
category : nodejs
---



##fs.writeFile(filename, data, [options], callback)：

	/**
	 * 往文件里异步写数据，写入的内容可以是字符串，也可以是二进制数据。
	 * 如果文件不存在，则创建；如果文件已存在，那么内容会被覆盖
	 * @param {String} filename 文件名
	 * @param {String|Buffer} data 要往文件里写的内容，可以是字符串，也可以是二进制数据。当为二进制数据时候，options.encoding 会被忽略
	 * @param {Object} [options]
	 * @param {String} options.encoding 编码，默认是utf8
	 * @param {Number} options.mode=438 模式
	 * @param {String} options.flag=w 写文件的模式
	 * @param {Function} callback 回调方法
	 */
	fs.writeFile(filename, data, [options], callback)

##例子一：往不存在的文件里写内容

往一个不存在的文件里写内容，则会先创建该文件，再往里面写内容

	var noneExistFileName = ['async_create.', new Date()-0, '.txt'].join('');
	fs.writeFile(noneExistFileName, '文件不存在，则创建', function(err){
	    if(err) throw err;
	    console.log(noneExistFileName+'不存在，被创建了！');
	});


##例子二：往存在的文件里写内容

如果该文件已存在，则原有文件内容会被覆盖

	fs.writeFile('async_exists.txt', '文件已存在，则覆盖内容 -- '+(new Date()-0), function(err){
	    if(err) throw err;
	    console.log('exists.txt已存在，内容被覆盖！');
	});

##例子三：往已经存在的文件里追加内容

options.flag 设置为 'a' 时，则会将写模式变为追加内容

	fs.writeFile('async_add.txt', '\n文件已存在，并追加内容 -- '+(new Date()-0), {
	    flag: 'a'
	}, function(err){
	    if(err) throw err;
	    console.log('exists.txt已存在，内容被覆盖！');
	});