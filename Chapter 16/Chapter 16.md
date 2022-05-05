## 16 Segmentation

### Simulation

1. It's so easy.
   
   address space size = 128(7 bits): VA >= 0x40 (0100 0000) --> SEG1; VA < 0x40 (0100 0000) --> SEG0.
   
   legal seg0: 0\~19; legal seg1: 108\~127.
   
   VA 0x6c (108) --> seg1: base1-(size-108) --> seg1: 512-(128-108) --> seg1: 492.
   
   VA 0x61 (97) --> 97 not in valid segs --> seg1 violation.
   
   and so on.
   
   ![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%2016/images/1.png)

2. The highest legal virtual address in segment 0 is 19. The lowest legal virtual address in segment 1 is 108. The lowest and highest illegal addresses in this entire address space is 20 and 107. `segmentation.py -a 128 -p 512 -b 0 -l 20 -B 512 -L 20 -s 0 -A 19,20,107,108 -c`
   
   ![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%2016/images/2.png)

3. `segmentation.py -a 16 -p 128 -A 0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15 --b0 0 --l0 2 --b1 16 --l1 2 -c`
   
   ![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%2016/images/3.png)

4. Just let `(limit0 + limit1) / address_size = 0.9`.
   
   ![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%2016/images/4.png)

5. Just let `--l0 0 --l1 0`.
   
   ![img](https://gitee.com/ChobitsY/ostep/raw/master/Chapter%2016/images/5.png)
