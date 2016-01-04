Scripts
=====
Tiny Bash Scripts

# map

paths.txt
```txt
/path/to/fizz.txt
/path/to/buzz.txt
```

```bash
$ cat paths.txt | map 'basename $1'
fizz.txt
buzz.txt
```

# reduce

path.txt
```txt
path
to
fizz.txt
```

```bash
$ cat path.txt | reduce '' 'echo $1/$2'
/path/to/fizz.txt
```

# flatten

fizz.txt
```txt
fizz
```

buzz.txt
```txt
buzz
```

files.txt
```txt
fizz.txt
buzz.txt
```

```bash
$ cat files.txt | flatten 'cat $@'
fizz
buzz
```

# pipemap

fizz.txt
```txt
fizz
buzz
```

```bash
$ cat fizz.txt | pipemap cat
fizz
buzz
```

# total

nums.txt
```txt
1
2
3
```

```bash
$ cat nums.txt | total
6
```

# isnum

```bash
$ isnum -12.3 && echo true || echo false
true
```
