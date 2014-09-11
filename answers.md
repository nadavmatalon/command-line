##Guidelines &amp; Answers:

* Change into the temporary directory

```bash
$> cd /tmp
```

* Using one command, create a directory structure `my/private/files`

```bash
$> mkdir -p my/private/files
```

* Using one command, create a directory structure `my/public/files`

```bash
$> mkdir -p my/public/files
```

* Create an empty file `t-vars.env` in `my/private/files`

> In `/tmp/my/private/files/`

```bash
touch t-vars.env
```

* Using command-line only add the line `List of env vars that begin with T` to the file, 
  make sure it ends with a newline

> In `/tmp/my/private/files/`

```bash
$> echo "List of env vars that begin with T" >> t-vars.env
```

> To see the content: 

```bash
$> less t-vars.env
```

* List all env variables that begin with `T` (hint: you'll need a regex that includes 
  the marker of the start of the line) and append them to the end of the file

> In `/tmp/my/private/files/`

```bash
$> env | grep "^T" >> t-vars.env
```

* export a new variable `TESTING_MAKERS=working` in such a way that it is still 
  available when you open a new shell

```bash
$> export TESTING_MAKERS=working
$> echo "export TESTING_MAKERS=working" >> ~/.bash_profile
```bash


* open a new terminal window, check that a new variable is available

```bash
$> echo $TESTING_MAKERS
=> working
```bash

* Output the `count` of the variables that `begin with T` to a new 
  file `my/public/files/t-vars.count`, e.g. "Overall count: 5" 
  (hint: you'll need to use `command substitution` in bash)

> In `/tmp`

```bash
$> echo Overall count: `env | grep "^T" | wc -l` >> my/public/files/t-vars.count
```

* Change the `permissions` of the `my/private/files/t-vars.env` to make sure that only 
  the owner can read and write the file

> Read & write, but not execute
> In `/tmp/my/private/files`

```bash
$> chmod 600 t-vars.env
```

> Check: 

```bash
$> ls -l
```bash


* Change the `permissions` of the `my/private/files` directory to make sure that only 
  the owner can change into it

> In `private`

```bash
$> chmod 700 files
```

> Check: 

```bash
$> ls -l
```

* Give `read and write permissions` to all users on `my/public/files/t-vars.count`

> Read & write, but not execute
> in `/files`

```bash
$> chmod 666 t-vars.count
```

> Check: 

```bash
$> ls -l
```

* Create another file `my/public/files/text-files-count.txt` and output the number 
  of text files in your home directory (recursively) into that file

> In `home`

```bash
$> cd ~ 
$> find . -name *.txt | wc -w >> /tmp/my/files/text-files-count.txt
```bash

> To get the same result with quotes: 

```bash
$> find . -name “*.txt” | wc -w >> /tmp/my/files/text-files-count.txt)
```

* List all env variables sorted alphabetically and show the top 3 lines

```bash
$> env | sort -f | head -n3
```


