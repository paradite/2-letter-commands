# 2-Letter Commands

I was doing `fg` and `bg` today and got curious on how many valid 2-letter commands are there on a UNIX (macOS) system.

So I made a command that lists them (to my best knowledge):

```
$ ls -1 /usr/bin/ /usr/sbin/ /bin/ /sbin/ | awk 'length == 2' | sort
aa
ab
ac
ar
as
at
bc
bg
cc
cd
cp
cu
dc
dd
df
du
ed
ex
fc
fg
id
ld
ln
lp
ls
m4
mg
mv
nc
nl
nm
od
pl
pp
pr
ps
ri
rm
rs
sa
sh
su
tr
ul
vi
wc
```

I also counted them:

```
$ ls -1 /usr/bin/ /usr/sbin/ /bin/ /sbin/ | awk 'length == 2' | sort | wc -l
      46
```

There are 46 of them. 45 if you don't count `m4` which contains a digit not a letter.

Total number of possible combinations of 2 letters are 26 * 26 = 676.

So the chance of a random combination being a valid command is 45 / 676 = 6.66%.

That's pretty high.

---

PRs are welcomed!
A brief explanation of what each of them do would be a nice addition. Some of them can be found [here](https://www.davekb.com/browse_computer_tips:linux_two_letter_commands:txt)
