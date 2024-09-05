The fastcms has a security problem that arbitrary files can be uploaded and system permissions can be obtained

**Project Address**  
https://gitee.com/dianbuapp_admin/fastcms

**Project Issues**  
https://gitee.com/dianbuapp_admin/fastcms/issues/IAP5ET

**This interface has an arbitrary file writing capability (path controllable)**  
/fastcms/api/admin/template/files/upload

com.fastcms.cms.controller.admin.TemplateController#upload,receiving parameter. Although the parameter "dirName" is filtered, the final uploaded file name is controlled by the operator.
![](https://github.com/wave-to/SomeCms/blob/main/images/fastcms_01.png)
![](https://github.com/wave-to/SomeCms/blob/main/images/fastcms_02.png)
Upload a request packet for any file to be written (the uploaded content is an ssh public key)
![](https://github.com/wave-to/SomeCms/blob/main/images/fastcms_03.png)
The ssh public key is successfully written to the target machine
![](https://github.com/wave-to/SomeCms/blob/main/images/fastcms_04.png)
Successfully have logged in to the ssh and obtained the permission of the server.
![](https://github.com/wave-to/SomeCms/blob/main/images/fastcms_05.png)
