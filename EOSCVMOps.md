# EOSC VM Operations

## 远程免密登录 
RSA公私钥配置  
`ssh username@ip`

## 添加用户、设置有密登录
`addusers newname`  //添加新用户  
`passwd newname`    //设置用户密码  
  
`gpasswd -a newname wheel`  //给予sudo权限, 当权限不够时，可以用sudo  
`lid -g wheel`             //查询所有带sudo权限的用户  
`userdel -r newname`        //删除用户和相应的目录

SSH配置文件保存在`/etc/ssh/sshd_config`  
`PermitRootLogin no`  //限制root权限登录  
`AllowUsers newname`    //允许新用户ssh登录  
`PasswordAuthentication yes`    //允许用户密码登录  
配置完毕记得重启vm， `#reboot`

## 配置Jupyter Notebook Environment
