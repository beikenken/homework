## “自顶向下，逐步求精”的思想方法
 自顶向下、逐步求精的设计方法符合抽象和分解的原则，是日常处理问题的一种方法，是人们解决复杂问题时常用的方法，实际上就是对要处理的问题分层考虑。用这种方法进行程序设计，通常是与模块化设计、结构化设计相结合。它的基本设计思想是：首先从总体出发，把待解决的问题分解为若干个功能相对独立的子问题 ，每个子问题对应于一个子程序，通常也称模块；然后把每一个子问题再分解为若干个低一层的子问题，这样分解下去，直到最低层的所有子问题意义单一、要求明确，再把它们写成基本函数或基本过程，这称其为基本模块；每个函数或过程可以再分解成一个个基本任务，每个基本任务都可选用顺序结构、选择结构和循环结构来实现。这种从总体到局部、从抽象到具体、先粗后细逐步深入的求解方法，就是"自顶向下、逐步求精"的程序设计方法。
![image](https://img-blog.csdn.net/20171129145149190?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemhhbmd3ZWlrdW4xOTk4/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
# 使用伪代码分解“正常洗衣”程序的大步骤。
## set the water in >> soap the clothes >> wash the clothes >> dewatering the clothes >> stop the work 注水 >> 浸泡 >> 洗涤和漂洗 >> 脱水 >> 停机
# 进一步用基本操作、控制语句（IF、 FOR、 WHILE等）、变量与表达式，写出每 个步骤的伪代码
## 注水：
turn on the water_in_switch <br>
set the water volume <br>
while(water_input is less than the water volume) <br>
 keep the water_in_switch open <br>
while(water_input is more than the water volume or volume timeout) <br>
  stop input water<br>

## 浸泡 
set the soaping time <br>
for(set the left time is zero ;the left time is less than the setting time; increase the left time) <br>
 keep the clothes soaping <br>
if(the left time is equal to the setting time) <br>
  begin to wash<br>

## 洗涤和漂洗 
set the washing times to 3 <br>
set the washing time to 20 <br>
for(set a to zero; a is less than setting times; add 1 to a;) <br>
  if(the washing times is not the 1st time) <br>
   pouring the water <br>
   pouring in the new and clean water <br>
do <br>
  washing and motor runs <br>
while(the pass time is less than the washing time) <br>
pouring the water<br>

## 脱水 
set the motor run’s frequency <br>
set the running time <br>
while the past time is less than the running time <br>
 keep the motor running in the setting frequency<br>

## 提取一些共性功能模块（函数），简化“正常洗衣”程序，使程序 变得更利于人类理解和修改维护。
int wait(time) <br>
set the waiting time<br> 
return the waiting time<br>

int the washing(time) <br>
set the washing time <br>
return the washing time<br>

int pour_out the water(timeout)<br> 
set the time <br>
while the time is over <br>
 stop pouring<br>

int pour_in the water(volume,timeout) <br>
set the time <br>
while the time is over<br> 
stop pouring<br>

