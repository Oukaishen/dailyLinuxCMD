## chown

**Change** the **ownership** of files and directories in Linux file system.

<br>

Three types of file permissions:

- **User** permissions. These permissions apply to a single user who has special access to the file. This user is called the **owner**.
- **Group** permissions. These apply to a single group of users who have access to the file. This group is the **owning group**.
- **Other** permissions. These apply to every other user on the system. These users are known as **others**, or **the world**.

<br>

### Example

```shell
chown -R hadoop:hadoop directory
```

Change the directory ownership recursively to user: hadoop, group: hadoop. 

<br>



## References

https://www.computerhope.com/unix/uchown.htm