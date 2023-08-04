# MySql Change Password

_Many a time your security scan shall fail for having_

/etc/mysql/debian.cnf file in your linux instance. Typically, after a image has been made, you need to remove this file and set a special user _debian-sys-maint which can be used to reset your root user login._

**Step 1:**

```bash
mysql -u debian-sys-maint -p%oldpassword%
```

(replace %oldpassword% with the password you are being given by us when you first time do SSH to your instance)

&#x20;**Step2:**

_SET PASSWORD = PASSWORD(‘%newpassword%’);_

(replace %newpassword% with the  new password)

&#x20;**Step3:**

_exit_

**Step 4:**

Now you can login with this user and set password for any user including root

Mysql Debian conf file vulnerability remediation on public clouds – AWS Azure GCP Oracle04.16.2022
