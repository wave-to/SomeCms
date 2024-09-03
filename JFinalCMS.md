The /admin/template/update interface of the JFinalCMS system has any file upload security problems and can obtain server permissions  

**Project Address**  
https://gitee.com/heyewei/JFinalcms
&nbsp;  
&nbsp;  
**Project Issues**  
https://gitee.com/heyewei/JFinalcms/issues/IAOKSQ
&nbsp;  
&nbsp;  
**This interface has an arbitrary file writing capability (path controllable)**  
/admin/template/update
&nbsp;  
&nbsp;  
com.cms.controller.admin.TemplateController#update,accepts the parameters passed in, including the file name and file contents
![](https://github.com/wave-to/SomeCms/blob/main/images/JFinalCMS_1.png)
Then call the com.cms.util.TemplateUtils#write method to write to the system file.
![](https://github.com/wave-to/SomeCms/blob/main/images/JFinalCMS_2.png)
Upload a request packet for any file to be written (the uploaded content is an ssh public key)
![](https://github.com/wave-to/SomeCms/blob/main/images/JFinalCMS_3.png)
The ssh public key is successfully written to the target machine
![](https://github.com/wave-to/SomeCms/blob/main/images/JFinalCMS_4.png)
Successfully have logged in to the ssh and obtained the permission of the server.
![](https://github.com/wave-to/SomeCms/blob/main/images/JFinalCMS_5.png)
