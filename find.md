# find

kaishen, 24 Feb, 2018

A command to find/serach things.

#### find by name

Search `abc.txt` in the current directory, use this cmd:

```shell
find . -name abc.txt
```

If we want to use case-insensitive seach, use this cmd:

```shell
find . -iname abc.txt
```

If we want to use **"*"**, need to double quote the name:

```shell
find . -name "*.txt"
```



#### find by type

`-type` accpects some useful arguements like

* **d**: directory
* **f**: normal files

Search `abc` directory in the current directory, use this:

```shell
find . -type d -nanme abc
```



#### find followed by exec

`-exec` can add the command that you want to apply on the result by find.

The following code use `ls` command for those ".suffix" files.  

```shell
find . -name "*.suffix" -exec ls {} \;
```

`{} \;` is nothing special, `{}` represents the result from `find`, `\;` sents this to find command. 



Here is just very simple notes. For more advanced usage, please refer to the references link.

#### References

https://blog.gtwang.org/linux/unix-linux-find-command-examples/