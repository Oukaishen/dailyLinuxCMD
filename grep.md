# grep

kaishen, 27 June, 2018 

find some content in specific file

## Common used sample

find some content in specific file, show all matched lines

```shell
grep "some content" filename
```

<br>

show the matched line **and below 3** lines

```shell
grep -A 3 "some content" filename
```

<br>

Sometimes using grep will encounter this kind of problem

> Binary file (standard input) matches

This parameter will help you `-a`

> Process a binary file as if it were text; this is equivalent to the ‘--binary-files=text’ option.

```shell
grep -a "pattern" filename
```





## Regular expression example, [problem](https://leetcode.com/problems/valid-phone-numbers/description/).

```shell
987-123-4567     | valid
123 456 7890     | invalid
(123) 456-7890   | valid
---

grep '^\([0-9]\{3\}-\|([0-9]\{3\}) \)[0-9]\{3\}-[0-9]\{4\}$' file.txt

---

987-123-4567
(123) 456-7890
```





Further used sample will be added when I use them next time.