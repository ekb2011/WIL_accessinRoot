# Centos 사용자 접근 계정 변경 방법

  
![](https://lh3.googleusercontent.com/bynbnOy1dE-eA0Ysf1NVYLxHCFpyC5I_Y8m41bpkZZ0ODpGKb2MJz-mG7chxgGsMidrC1sJ1eE05)
  

>Please login as the user "centos" rather than the user "root".

  

* root 계정으로 접속하고 싶은 경우 OS 레벨에서 어떤 설정을 변경해야 될지

  

### centos 계정으로 Login

```$ssh -i PrivateKey.pem centos@IP_Address```

  

### 로그인 중인 계정 root로 변경

```$sudo -s```

  

### /root/.ssh/authorized_keys 파일 변경 : ssh-rsa 이전 문구 삭제

```$vi /root/.ssh/authorized_keys```

  

### /etc/ssh/sshd_config 파일 열어서 "PermitRootLogin yes"의 주석처리 해제 또는 수정 기입**

```$vi /etc/ssh/sshd_config```

  

### SSH 재시작
```$service sshd restart```

