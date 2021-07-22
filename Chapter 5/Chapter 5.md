## 5 Interlude: Process API

### Simulation

1. 
![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%205/images/1.png)

2. 
While fork percentage is higher, the final process tree is bigger.

3. 
![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%205/images/2.png)

   a forks b; b exits; a forks c; a forks d; d forks e.

4. 
When 'c' exits, orphaned process re-parent to 'a'. When use -R flag, orphaned process re-parent to 'b' (re-parent to local parent).

5. 
![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%205/images/3.png)

```
   a
   |-b
   | |-f
   |-c
   |-d
     |-e
```

6. 
![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%205/images/4.png)

   - a forks b; b forks c; c exits; b forks d; b forks e.
   - a forks b; b forks c; b forks d; c exits; b forks e.
   - a forks b; b forks c; b forks d; b forks e; c exits.
   - a forks b; a forks c; c exits; b forks d; b forks e.
   - a forks b; a forks c; b forks d; c exits; b forks e.
   - a forks b; a forks c; b forks d; b forks e; c exits.

### Code

1. `x = 100`, the variable in the child process is 100 too. `x` is independent.![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%205/images/5.png) ![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%205/images/6.png)
2. Yes, both child and parent can access the file descriptor. When they write at the same time, they all write successfully.![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%205/images/7.png)

3. Yes, just use `sleep()`.![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%205/images/8.png)

4. Because system have to meet different needs.![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%205/images/9.png)

5. `wait()` return the PID of child process. In the child, `wait()` return -1.![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%205/images/10.png)

6. When know the exact PID, use `waitpid()`.![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%205/images/11.png)

7. After close standard output, there are no outputs.![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%205/images/12.png)

8. 
![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%205/images/13.png)

