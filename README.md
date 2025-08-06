# some-issues-in-front-end-development
Handling of some issues in front-end developmentSome issues in front-end development，前端开发的一些问题处理
# 1、Windows7下在浏览器中上传ofd文件file.type可能为空，window10下正常
   不能使用file.type作为文件类型判断，需要使用file.name的后缀判断ofd文件
   例如    const fileName = file.name || file.fileName
    const indexf = fileName.lastIndexOf('.')
    const fileType = fileName.substring(indexf).toLowerCase()
    if( fileType==='ofd'){
    //通过ofd文件类型验证
    }
