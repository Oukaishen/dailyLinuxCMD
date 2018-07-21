# ssh

record down the setup of ssh

**Generate the ssh key**

```shell
cd to where you want to put this key, there will be one public key and one private key
```

```shell
ssh-keygen -t rsa -C "your email"
```

<br>

The "t" specify the type of the key. "C" is the comment. The parameter detail can be found [here](man.linuxde.net/ssh-keygen).



**Configure ssh to use the key**

```shell
edit the "config" file under the .ssh
```

Input something like this 

```shell
HOST 18.221.143.156
HostName 18.221.143.156
  User ointeract
  IdentityFile ~/.ssh/id_rsa_ointeract/id_rsa_ointeract  
```



**copy your key to your server(if the server are yours)**

```shell
ssh-copy-id -i /path/to/key.pub SERVERNAME
```



***Most Importantly***

can use the `-vvv` option to debug

```
ssh -vvv -i <where is your private key> username@host
```



can refer to this [link](https://askubuntu.com/questions/311558/ssh-permission-denied-publickey).



