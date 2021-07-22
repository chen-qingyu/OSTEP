## 8 Scheduling: The Multi-Level Feedback Queue

### Simulation

1. 

![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%208/images/1.png)

![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%208/images/2.png)

I had a question at the beginning: why is ALLOT only 1, but after running 1 ticks, it's priority is not reduced? Think about it, because ALLOT is based on a time slice.

![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%208/images/3.png)

![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%208/images/4.png)

So, there is an error in README:  ALLOT is measured in time slices, not milliseconds.![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%208/images/5.png)

2. 

Example 1: 

![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%208/images/6.png) ![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%208/images/7.png)

Example 2: 

![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%208/images/8.png) ![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%208/images/9.png)

Example 3: 

![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%208/images/10.png) ![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%208/images/11.png)

3. 

![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%208/images/12.png) ![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%208/images/13.png)

4. 

![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%208/images/14.png)

5. Boost = 10 ms / 0.05 = 200 ms.

6. 

With the `-I` flag: 
![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%208/images/15.png)

Without the `-I` flag: 
![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%208/images/16.png)

