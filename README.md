# 18年912真题回忆

说在前面：912 的试题在一个A4 纸一半大小的牛皮纸信封里，试卷是雪白A4竖版印刷，有好多页，在左上角钉，是对折了之后放在里面的。

## DSA:70'  
### 判断题(12*2'):  

1. $n^{log(log(log(n)))}$ 等于 $O(\biggl\lfloor log(n) \biggr\rfloor)$
2. Huffman 编码树中，如果交换深度不同的两个树结点，那么一定会增大整体编码成本
3. 即使不使用改进的 next 表，kmp 依然可以达到线性的时间复杂度
4. 如果访问不具有局部性，伸展树不能保证O(log(n)) 的访问时间
5. 对于二叉树，通过先序遍历和后序遍历不能确定其层次遍历
6. 有2019个叶节点的真二叉树数量比2018对括号的合法表达式数量要多
7. 对于叶节点数量为 2018 的二叉树，层次遍历队列容量必然小于 2018
8. 插入排序每次插入数据，即使不增加循环节，也不至减少
9. 交换两个逆序对，必然会减少总逆序对数
10. 基数排序的底层算法如果不稳定，排序的结果有可能是错的。
11. 函数的调用栈中如果有相同的函数，则他们必然紧邻
12. 如果插入的关键码独立均匀分布，堆的插入操作平均O(1)，最坏O(logn)



### 简答题(8*4'):

要求每题小于80字。

- 把中缀表达式转换成 RPN（逆波兰表达式）已经相当于是一次表达式的求值的成本，那为什么还要把他转换成RPN？RPN有啥好处？

- DFS（广度优先搜索）中， 什么时候标记前向边，什么时候标记后向边？
- Dijkstra 算法在稠密图上运行时，为什么用多叉堆而不用完全二叉堆？以及堆的分叉数怎么确定？

- 相对于开放散列，闭散列的优点？请举出两点。
- 相对锦标赛树，败者树（loser tree） 有啥优势？
- 相对选择排序，插入排序有哪些好处，举出两个并解释

- 红黑树有的时候比AVL书要好，什么时候？有什么优势？
- KMP 算法什么情况下比蛮力搜索更高效？为啥？



### 二叉树(7'+3'+4'):

给出了二叉树的结点链式实现，实现里每个节点有size（以自己为根的树的总结点个数）和左右孩子。

有一个叫`rank`的函数，参数是根节点和秩，返回指定序号元素（0开始编号，按后序遍历顺序编号），中间有一大段代码空出来了。要求是时间复杂度控制在` O(depth(x)) ` 内， 提示了不可以直接后序遍历，因为那样复杂度超高，不得分。

1. 填空实现相关功能（少于12行，按有效代码记）。
2. 解释相关算法（少于200字，可以配一张图）。
3. 证明时间和空间复杂度。















## 计算机原理:30'

### 判断(5*1')

- CPI越小，程序计算速度越快
- C语言中int x>0,问 x*x的符号是否一定>0
- 设置什么什么功能单元可以解决结构冲突【具体忘了】
- 硬盘顺序访问快于随机访问
- 冯诺依曼体系将程序当作数据存在内存中



### 填空（1',2'的都有）：

- 一个十进制正数的32位补码，用十六进制表示，小端机器。

- 一个负的小数（好像是 -27.625），转32位ieee754浮点数表示
- 写出三种解决数据冲突的方法
- 写出三种Cache缺失的原因

【好像是4道题？还有没有了？求确认】


### 选择：

【待补充，完全忘了】

1. 关于总线【同步总线比异步总线快 串行比并行快 单总线比双总线快 全不对】
2. 虚拟地址连续，物理地址可能不连续。【大概是这个意思】
3. SRAM&DRAM， 速度相对快&慢， 用作内存&Cache，需不需要刷新。【选项大概是前面的组合】
4. 哪种RAID没有纠错能力？【RAID0 RAID1 RAID5 RAID6】
5. MIPS架构只有哪种数据冲突？【RAW WAR 还有两个】



### 流水线(好像是5'?)：

MIPS架构，给了7条指令，需要计算单周期，多周期设计下的时延

这题有三个问。

1. 
2. bla
3. bla





## 操作系统:30'

### 填空(15*1'):

*填空题大概是10道题，但是每道题有至少一个空 *

- （>=3个空）Stride调度算法的溢出相关问题，溢出之后可以巧妙的回避溢出带来的问题，用了8位的无符号整数【后面忘了，貌似是天大于小于之类的】
- （1个空）CR3寄存器存的是页表的什么。【具体忘了，答案好像是地址？】
- （2个空）CPL，DPL，门和段的特权级判断问题
- （3个空）信号量的实现，PV操作的函数里面挖掉了3行，挺简单的
- （2个空）父进程退出，子进程没退出，子进程变成啥？子进程退出，父进程还没 wait，子进程变成啥？
- 【中间好像还有好几个题】
- （2个空）文件F的inode，A是F的软连接，B是F的硬链接，C是B的硬连接，求B和C的引用计数

### 判断(5*1'):

- x86开启了二级页表，则页表可以不在内存中。
- ucore的时钟中断为10ms，故不能完成 10ms以下的定时。
- 中断向量表中存放着中断门的优先级。
- 只有一个main函数的程序不能有多个线程
- 银行家算法中，不安全状态就是死锁状态

### ucore(6'):

给出了好多代码有 `switch.S` （att语义的x86汇编），进程上下文的定义，进程切换的代码。

要求读玩代码之后，写出实现功能的位置：

-  切换页表的代码
-  切换堆栈的代码
-  switch 函数中读取两个参数的代码

注：具体代码请移步ucore源码，这里给出链接。

switch.S: https://github.com/chyyuu/ucorebook_code/blob/18da356a2f3ef90680aca9cc50ef328d1e84585e/code/kern/process/switch.S

```asm
.text
.globl switch_to
switch_to:                      # switch_to(from, to)

    # save from's registers
    movl 4(%esp), %eax          # eax points to from
    popl 0(%eax)                # save eip !popl
    movl %esp, 4(%eax)
    movl %ebx, 8(%eax)
    movl %ecx, 12(%eax)
    movl %edx, 16(%eax)
    movl %esi, 20(%eax)
    movl %edi, 24(%eax)
    movl %ebp, 28(%eax)

    # restore to's registers
    movl 4(%esp), %eax          # not 8(%esp): popped return address already
                                # eax now points to to
    movl 28(%eax), %ebp
    movl 24(%eax), %edi
    movl 20(%eax), %esi
    movl 16(%eax), %edx
    movl 12(%eax), %ecx
    movl 8(%eax), %ebx
    movl 4(%eax), %esp

    pushl 0(%eax)               # push eip

    ret

```

进程上下文及相关定义：  https://github.com/chyyuu/ucorebook_code/blob/18da356a2f3ef90680aca9cc50ef328d1e84585e/code/kern/process/proc.h

```c

// process's state in his life cycle
enum proc_state {
    PROC_UNINIT = 0,  // uninitialized
    PROC_SLEEPING,    // sleeping
    PROC_RUNNABLE,    // runnable(maybe running)
    PROC_ZOMBIE,      // almost dead, and wait parent proc to reclaim his resource
};

// Saved registers for kernel context switches.
// Don't need to save all the %fs etc. segment registers,
// because they are constant across kernel contexts.
// Save all the regular registers so we don't need to care
// which are caller save, but not the return register %eax.
// (Not saving %eax just simplifies the switching code.)
// The layout of context must match code in switch.S.
struct context {
    uint32_t eip;
    uint32_t esp;
    uint32_t ebx;
    uint32_t ecx;
    uint32_t edx;
    uint32_t esi;
    uint32_t edi;
    uint32_t ebp;
};

#define PROC_NAME_LEN               15
#define MAX_PROCESS                 4096
#define MAX_PID                     (MAX_PROCESS * 2)

extern list_entry_t proc_list;
extern list_entry_t proc_mm_list;

struct inode;
struct fs_struct;

struct proc_struct {
    enum proc_state state;                      // Process state
    int pid;                                    // Process ID
    int runs;                                   // the running times of Proces
    uintptr_t kstack;                           // Process kernel stack
    volatile bool need_resched;                 // bool value: need to be rescheduled to release CPU?
    struct proc_struct *parent;                 // the parent process
    struct mm_struct *mm;                       // Process's memory management field
    struct context context;                     // Switch here to run process
    struct trapframe *tf;                       // Trap frame for current interrupt
    uintptr_t cr3;                              // CR3 register: the base addr of Page Directroy Table(PDT)
    uint32_t flags;                             // Process flag
    char name[PROC_NAME_LEN + 1];               // Process name
    list_entry_t list_link;                     // Process link list 
    list_entry_t hash_link;                     // Process hash list
    int exit_code;                              // return value when exit
    uint32_t wait_state;                        // Process waiting state: the reason of sleeping
    struct proc_struct *cptr, *yptr, *optr;     // Process's children, yonger sibling, Old sibling
    list_entry_t thread_group;                  // the threads list including this proc which share resource (mem/file/sem...)
    struct run_queue *rq;                       // running queue contains Process
    list_entry_t run_link;                      // the entry linked in run queue
    int time_slice;                             // time slice for occupying the CPU
    sem_queue_t *sem_queue;                     // the user semaphore queue which process waits
    event_t event_box;                          // the event which process waits   
    struct fs_struct *fs_struct;                // the file related info(pwd, files_count, files_array, fs_semaphore) of process
};

#define PF_EXITING                  0x00000001      // getting shutdown

//the wait state
#define WT_CHILD                    (0x00000001 | WT_INTERRUPTED)  // wait child process
#define WT_TIMER                    (0x00000002 | WT_INTERRUPTED)  // wait timer
#define WT_KSWAPD                    0x00000003                    // wait kswapd to free page
#define WT_KBD                      (0x00000004 | WT_INTERRUPTED)  // wait the input of keyboard
#define WT_KSEM                      0x00000100                    // wait kernel semaphore
#define WT_USEM                     (0x00000101 | WT_INTERRUPTED)  // wait user semaphore
#define WT_EVENT_SEND               (0x00000110 | WT_INTERRUPTED)  // wait the sending event
#define WT_EVENT_RECV               (0x00000111 | WT_INTERRUPTED)  // wait the recving event 
#define WT_MBOX_SEND                (0x00000120 | WT_INTERRUPTED)  // wait the sending mbox
#define WT_MBOX_RECV                (0x00000121 | WT_INTERRUPTED)  // wait the recving mbox
#define WT_PIPE                     (0x00000200 | WT_INTERRUPTED)  // wait the pipe
#define WT_INTERRUPTED               0x80000000                    // the wait state could be interrupted

#define le2proc(le, member)         \
    to_struct((le), struct proc_struct, member)

extern struct proc_struct *idleproc, *initproc, *current;
extern struct proc_struct *kswapd;

void proc_init(void);
void proc_run(struct proc_struct *proc);
int kernel_thread(int (*fn)(void *), void *arg, uint32_t clone_flags);

char *set_proc_name(struct proc_struct *proc, const char *name);
char *get_proc_name(struct proc_struct *proc);
void cpu_idle(void) __attribute__((noreturn));

struct proc_struct *find_proc(int pid);
void may_killed(void);
int do_fork(uint32_t clone_flags, uintptr_t stack, struct trapframe *tf);
int do_exit(int error_code);
int do_exit_thread(int error_code);
int do_execve(const char *name, int argc, const char **argv);
int do_yield(void);
int do_wait(int pid, int *code_store);
int do_kill(int pid, int error_code);
int do_brk(uintptr_t *brk_store);
int do_sleep(unsigned int time);
int do_mmap(uintptr_t *addr_store, size_t len, uint32_t mmap_flags);
int do_munmap(uintptr_t addr, size_t len);
int do_shmem(uintptr_t *addr_store, size_t len, uint32_t mmap_flags);
```



void proc_run(struct proc_struct *proc) 函数：209行 https://github.com/chyyuu/ucorebook_code/blob/18da356a2f3ef90680aca9cc50ef328d1e84585e/code/kern/process/proc.c

```c
void
proc_run(struct proc_struct *proc) {
    if (proc != current) {
        bool intr_flag;
        struct proc_struct *prev = current, *next = proc;
        local_intr_save(intr_flag);
        {
            current = proc;
            load_esp0(next->kstack + KSTACKSIZE);
            lcr3(next->cr3);
            switch_to(&(prev->context), &(next->context));
        }
        local_intr_restore(intr_flag);
    }
}
```



### 页表(4'):

【忘了不少，求补充】

给出了内存内容的图，还有二级页表的描述（起始地址，页表项地址等虚拟地址），求物理地址。

## 计算机网络（20'）:

### 选择(6*1'):  

1. 电话网，可靠连接，IP电话分别是电路交换，分组交换，报文路径是否固定【选项是以上的组合】
2. 六边形的蜂窝网络，840个可用频率，求每个节点可用频率数量
3. 源与目的的距离越（远），传输速率越（大） ，停等协议效率越低。【选项是以上的组合】

4. 由两端链路构成，给出包大小，数字带宽，传输速率，计算延迟【1.5s 1.6s 2.1s 3.1s】


5. CSMA/CD，已知最小数据帧长度，传播速度和距离，计算最大传输数据速度【1Gbps 2Gbps 200Mbps 100Mbps】
6. TCP协议 给出MSS，RTT以及窗口为W时发生拥塞，问有足够多的数据要发时的平均吞吐量

### URL大题(4'):

给一个 URL:http://info.tsinghua.edu.cn:80/index.jsp，服务器 IP 是 `166.111.4.98` 。

1. 说出这个 URL 各个组成部分
2. 一般来说，在浏览器里输入 http://info.tsinghua.edu.cn:80/index.jsp 跟输入 http://166.111.4.98:80/index.jsp 看到的是一样的。
   1.  如果输前者能打开，后者打不开，这可能是什么原因?
   2.  如果输前者打不开，后者能打开，这可能是什么原因?



### IP、路由器大题（10')：

给了一个 子网掩码为 /24  的IP地址段，还有一张三个局域网用路由器相连的拓扑图，让分配主机和路由器的网段。

```
注：[R1]表示路由器，e1 表示端口
   [R1]~e1-------e2~[R2]~e4-------e5~[3]
    e0               e3               e6
    |                |                |
    |                |                |
    |                |                |
    V                V                V
  {网络1}           {网络2}          {网络3}
    |\               |                
    | \              |
    |  \             |
    |   \            |
    |    \           |
    |     \          |
    |      \         |
    |       \        |
  主机A     主机B    主机C
 
```



1. 给各局域网、路由器的各端口分派IP地址
2. ARP在同一局域网间的主机通信操作是做什么，在不同局域网间的主机通信操作是做什么？
3. 局域网1的主机A给局域网2的主机C发送信息，这一路径中，每一跳的源IP地址、目的IP地址各是什么？源MAC地址、目的MAC地址各是什么？