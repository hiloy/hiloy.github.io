# linux ssh

### ssh-config
选项参数查看：man ssh,匹配-o参数即可看到
eg：
    Host github.com
        Hostname github.com
        Port 22
        User git
        IdentityFile ~/.ssh/id_rsa