# Summary

- [1.	Bumblebee内核指令集与CSR介绍](chapter1/1.md)
  - [1.1.	RISC-V指令集介绍](chapter1/1.1.md)
  - [1.2.	Bumblebee内核支持指令集](chapter1/1.2.md)
  - [1.3.	CSR寄存器](chapter1/1.3.md)
- [2.	Bumblebee内核特权架构介绍](chapter2/2.1.md)
  - [2.1.	总体介绍](chapter2/2.1.md)
  - [2.2.	特权模式（Privilege Modes](chapter2/2.2/2.2.md)
  - [2.2.1.	机器模式（Machine Mode）](chapter2/2.2/2.2.1.md)
  - [2.2.2.	用户模式（User Mode）](chapter2/2.2/2.2.2.md)
  - [2.2.3.	机器子模式（Machine Sub-Mode](chapter2/2.2/2.2.3.md)
  - [2.2.4.	模式（Mode）的查看](chapter2/2.2/2.2.4.md)
  - [2.2.5.	Machine Mode到User Mode的切换](chapter2/2.2/2.2.5.md)
  - [2.2.6.	User Mode到Machine Mode的切换](chapter2/2.2/2.2.6.md)
  - [2.2.7.	中断、异常、NMI的嵌套](chapter2/2.2/2.2.7.md)
  - [2.3.	物理存储器保护（PMP)](chapter2/2.3.md)
- [3.	Bumblebee内核异常机制介绍](chapter3/3.1.md)
  - ​	[3.1.	异常概述](chapter3/3.1.md)
  - ​	[3.2.	异常屏蔽](chapter3/3.2.md)
  - ​	[3.3.	异常的优先级](chapter3/3.3.md)
  - ​	[3.4.	进入异常处理模式](chapter3/3.4/3.4.md)
    - [3.4.1.	从mtvec定义的PC地址开始执行](chapter3/3.4/3.4.1.md)
    - [3.4.2.	更新CSR寄存器mcause](chapter3/3.4/3.4.2.md)
    - [3.4.3.	更新CSR寄存器mepc](chapter3/3.4/3.4.3.md)
    - [3.4.4.	更新CSR寄存器mtval](chapter3/3.4/3.4.4.md)
    - [3.4.5.	更新CSR寄存器mstatus](chapter3/3.4/3.4.5.md)
    - [3.4.6.	更新Privilege Mode](chapter3/3.4/3.4.6.md)
    - [3.4.7.	更新Machine Sub-Mode](chapter3/3.4/3.4.7.md)
  - ​	[3.5.	退出异常处理模式](chapter3/3.5/3.5.md)
    - [3.5.1.	从mepc定义的PC地址开始执行](chapter3/3.5/3.5.1.md)
    - [3.5.2.	更新CSR寄存器mstatus](chapter3/3.5/3.5.2.md)
    - [3.5.3.	更新Privilege Mode](chapter3/3.5/3.5.3.md)
    - [3.5.4.	更新Machine Sub-Mode](chapter3/3.5/3.5.4.md)
  - ​	[3.6.	异常服务程序](chapter3/3.6.md)
  - ​	[3.7.	异常嵌套](chapter3/3.7.md)
- [4.	Bumblebee内核NMI机制介绍](chapter4/4.1.md)
  - ​	[4.1.	NMI概述](chapter4/4.1.md)
  - ​	[4.2.	NMI屏蔽](chapter4/4.2.md)
  - ​	[4.3.	进入NMI处理模式](chapter4/4.3/4.3.md)
    - [4.3.1.	从mnvec定义的PC地址开始执行](chapter4/4.3/4.3.1.md)
    - [4.3.2.	更新CSR寄存器mepc](chapter4/4.3/4.3.2.md)
    - [4.3.3.	更新CSR寄存器mcause](chapter4/4.3/4.3.3.md)
    - [4.3.4.	更新CSR寄存器mstatus](chapter4/4.3/4.3.4.md)
    - [4.3.5.	更新Privilege Mode](chapter4/4.3/4.3.5.md)
    - [4.3.6.	更新Machine Sub-Mode](chapter4/4.3/4.3.6.md)
  - ​	[4.4.	退出NMI处理模式](chapter4/4.4/4.4.md)
    - [4.4.1.	从mepc定义的PC地址开始执行](chapter4/4.4/4.4.1.md)
    - [4.4.2.	更新CSR寄存器mstatus]( chapter4/4.4/4.4.2.md)
    - [4.4.3.	更新Privilege Mode](chapter4/4.4/4.4.3.md)
    - [4.4.4.	更新Machine Sub-Mode](chapter4/4.4/4.4.4.md)
  - ​	[4.5.	NMI服务程序](chapter4/4.5.md)
  - ​	[4.6.	NMI/异常嵌套](chapter4/4.6/4.6.md)
    - ​		[4.6.1.	进入NMI/异常嵌套](chapter4/4.6/4.6.1.md)
    - ​		[4.6.2.	退出NMI/异常嵌套](chapter4/4.6/4.6.2.md)
- [5.	Bumblebee内核中断机制介绍](chapter5/5.1.md)
  - ​	[5.1.	中断概述](chapter5/5.1.md)
  - ​	[5.2.	中断控制器ECLIC](chapter5/5.2.md)
  - ​	[5.3.	中断类型](chapter5/5.3/5.3.md)
    - ​		[5.3.1.	外部中断](chapter5/5.3/5.3.1.md)
    - ​		[5.3.2.	内部中断](chapter5/5.3/5.3.2/5.3.2.md)
      - [5.3.2.1    软件中断](chapter5/5.3/5.3.2/5.3.2.1.md)
      - [5.3.2.2    计时器中断](chapter5/5.3/5.3.2/5.3.2.2.md)
      - [5.3.2.3    存储器访问错误中断](chapter5/5.3/5.3.2/5.3.2.3.md)
  - ​	[5.4.	中断屏蔽](chapter5/5.4/5.4.1.md)
    - [5.4.1.	中断全局屏蔽](chapter5/5.4/5.4.1.md)	
    - [5.4.2.	中断源单独屏蔽](chapter5/5.4/5.4.2.md)
  - ​	[5.5.	中断级别、优先级与仲裁](chapter5/5.5.md)
  - ​	[5.6.	进入中断处理模式](chapter5/5.6/5.6.md)
    - ​		[5.6.1.	从新的PC地址开始执行](chapter5/5.6/5.6.1.md)
    - ​		[5.6.2.	更新Privilege Mode](chapter5/5.6/5.6.2.md)
    - ​		[5.6.3.	更新Machine Sub-Mode](chapter5/5.6/5.6.3.md)
    - ​		[5.6.4.	更新CSR寄存器mepc](chapter5/5.6/5.6.4.md)
    - ​		[5.6.5.	更新CSR寄存器mcause和mstatus	](chapter5/5.6/5.6.5.md)
  - ​	[5.7.	退出中断处理模式](chapter5/5.7/5.7.md)
    - ​		[5.7.1.	从mepc定义的PC地址开始执行](chapter5/5.7/5.7.1.md)
    - ​		[5.7.2.	更新CSR寄存器mcause和mstatus](chapter5/5.7/5.7.2.md)
    - ​		[5.7.3.	更新Privilege Mode](chapter5/5.7/5.7.3.md)
    - ​		[5.7.4.	更新Machine Sub-Mode](chapter5/5.7/5.7.4.md)
  - ​	[5.8.	中断向量表](chapter5/5.8.md)
  - ​	[5.9.	进出中断的上下文保存和恢复](chapter5/5.9.md)
  - ​	[5.10.	中断响应延迟](chapter5/5.10.md)
  - ​	[5.11.	中断嵌套](chapter5/5.11.md)
  - ​	[5.12.	中断咬尾](chapter5/5.12.md)
  - ​	[5.13.	中断的向量处理模式和非向量处理模式](chapter5/5.13/5.13.md)
    - ​		[5.13.1.	非向量处理模式](chapter5/5.13/5.13.1/5.13.1.1.md)
      - [5.13.1.1 非向量处理模式的特点和延迟](chapter5/5.13/5.13.1/5.13.1.1.md)
      - [5.13.1.2 非向量处理模式的中断嵌套](chapter5/5.13/5.13.1/5.13.1.2.md)
      - [5.13.1.3 非向量处理模式的中断咬尾](chapter5/5.13/5.13.1/5.13.1.3.md)
    - ​		[5.13.2.	向量处理模式](chapter5/5.13/5.13.2/5.13.2.1.md)
      - [5.13.2.1 向量处理模式的特点和延迟](chapter5/5.13/5.13.2/5.13.2.1.md)
      - [5.13.2.2 向量处理模式的中断嵌套](chapter5/5.13/5.13.2/5.13.2.2.md)
      - [5.13.2.3 向量处理模式的中断咬尾](chapter5/5.13/5.13.2/5.13.2.3.md)
- [6.	Bumblebee内核TIMER和ECLIC介绍](chapter6/6.1/6.1.1.md)
  - ​	[6.1.	TIMER介绍](chapter6/6.1/6.1.1.md)
    - ​		[6.1.1.	TIMER简介](chapter6/6.1/6.1.1.md)
    - ​		[6.1.2.	TIMER寄存器](chapter6/6.1/6.1.2.md)
    - ​		[6.1.3.	通过mtime寄存器进行计时](chapter6/6.1/6.1.3.md)
    - ​		[6.1.4.	通过mstop寄存器暂停计时器](chapter6/6.1/6.1.4.md)
    - ​		[6.1.5.	通过mtime和mtimecmp寄存器生成计时器中断](chapter6/6.1/6.1.5.md)
    - ​		[6.1.6.	通过msip寄存器生成软件中断](chapter6/6.1/6.1.6.md)
  - ​	[6.2.	ECLIC介绍](chapter6/6.2/6.2.md)	
    - ​		[6.2.1.	ECLIC简介](chapter6/6.2/6.2.1.md)	
    - ​		[6.2.2.	ECLIC中断目标](chapter6/6.2/6.2.2.md)
    - ​		[6.2.3.	ECLIC中断源](chapter6/6.2/6.2.3.md)
    - ​		[6.2.4.	ECLIC中断源的编号（ID）](chapter6/6.2/6.2.4.md)
    - ​		[6.2.5.	ECLIC的寄存器](chapter6/6.2/6.2.5/6.2.5.md)
      - [6.2.5.1	寄存器cliccfg](chapter6/6.2/6.2.5/6.2.5.1.md)
      - [6.2.5.2    寄存器clicinfo](chapter6/6.2/6.2.5/6.2.5.2.md)
      - [6.2.5.3    寄存器mth](chapter6/6.2/6.2.5/6.2.5.3.md)
      - [6.2.5.4    寄存器clicintip[i]](chapter6/6.2/6.2.5/6.2.5.4.md)
      - [6.2.5.5    寄存器clicintie[i]](chapter6/6.2/6.2.5/6.2.5.5.md)
      - [6.2.5.6    寄存器clicintattr[i]](chapter6/6.2/6.2.5/6.2.5.6.md)
      - [6.2.5.7    寄存器clicintctl[i]](chapter6/6.2/6.2.5/6.2.5.7.md)
    - ​		[6.2.6.	ECLIC中断源的使能位（IE）](chapter6/6.2/6.2.6.md)
    - ​		[6.2.7.	ECLIC中断源的等待标志位（IP）](chapter6/6.2/6.2.7.md)
    - ​		[6.2.8.	ECLIC中断源的电平或边沿属性（Level or Edge-Triggered）](chapter6/6.2/6.2.8.md)
    - ​		[6.2.9.	ECLIC中断源的级别和优先级（Level and Priority）](chapter6/6.2/6.2.9.md)
    - ​		[6.2.10.	ECLIC中断源的向量或非向量处理（Vector or Non-Vector Mode）](chapter6/6.2/6.2.10.md)
    - ​		[6.2.11.	ECLIC中断目标的阈值级别](chapter6/6.2/6.2.11.md)
    - ​		[6.2.12.	ECLIC中断的仲裁机制](chapter6/6.2/6.2.12.md)
    - ​		[6.2.13.	ECLIC中断的响应、嵌套、咬尾机制](chapter6/6.2/6.2.13.md)
- [7.	Bumblebee内核CSR寄存器介绍](chapter7/7.1.md)
  - ​	[7.1.	Bumblebee内核CSR寄存器概述](chapter7/7.1.md)
  - ​	[7.2.	Bumblebee内核的CSR寄存器列表](chapter7/7.2.md)
  - ​	[7.3.	Bumblebee内核的CSR寄存器的访问权限](chapter7/7.3.md)
  - ​	[7.4.	Bumblebee内核支持的RISC-V标准CSR](chapter7/7.4/7.4.md)
    - ​		[7.4.1.	misa](chapter7/7.4/7.4.1.md)
    - ​		[7.4.2.	mie](chapter7/7.4/7.4.2.md)
    - ​		[7.4.3.	mvendorid](chapter7/7.4/7.4.3.md)
    - ​		[7.4.4.	marchid](chapter7/7.4/7.4.4.md)
    - ​		[7.4.5.	mimpid](chapter7/7.4/7.4.5.md)
    - ​		[7.4.6.	mhartid](chapter7/7.4/7.4.6.md)
    - ​		[7.4.7.	mstatus](chapter7/7.4/7.4.7.md)
    - ​		[7.4.8.	mstatus的MIE域](chapter7/7.4/7.4.8.md)
    - ​		[7.4.9.	mstatus的MPIE和MPP域](chapter7/7.4/7.4.9.md)
    - ​		[7.4.10.	mstatus的FS域](chapter7/7.4/7.4.10.md)
    - ​		[7.4.11.	mstatus的XS域](chapter7/7.4/7.4.11.md)
    - ​		[7.4.12.	mstatus的SD域](chapter7/7.4/7.4.12.md)
    - ​		[7.4.13.	mtvec](chapter7/7.4/7.4.13.md)
    - ​		[7.4.14.	mtvt](chapter7/7.4/7.4.14.md)
    - ​		[7.4.15.	mscratch](chapter7/7.4/7.4.15.md)
    - ​		[7.4.16.	mepc](chapter7/7.4/7.4.16.md)
    - ​		[7.4.17.	mcause](chapter7/7.4/7.4.17.md)
    - ​		[7.4.18.	mtval（mbadaddr）](chapter7/7.4/7.4.18.md)
    - ​		[7.4.19.	mip](chapter7/7.4/7.4.19.md)
    - ​		[7.4.20.	mnxti](chapter7/7.4/7.4.20.md)
    - ​		[7.4.21.	mintstatus](chapter7/7.4/7.4.21.md)
    - ​		[7.4.22.	mscratchcsw](chapter7/7.4/7.4.22.md)
    - ​		[7.4.23.	mscratchcswl](chapter7/7.4/7.4.23.md)
    - ​		[7.4.24.	mcycle和mcycleh](chapter7/7.4/7.4.24.md)
    - ​		[7.4.25.	minstret和minstreth](chapter7/7.4/7.4.25.md)
    - ​		[7.4.26.	cycle和cycleh](chapter7/7.4/7.4.26.md)
    - ​		[7.4.27.	instret和instreth](chapter7/7.4/7.4.27.md)
    - ​		[7.4.28.	time和 timeh](chapter7/7.4/7.4.28.md)
    - ​		[7.4.29.	mcounteren](chapter7/7.4/7.4.29.md)
  - ​	[7.5.	Bumblebee内核自定义的CSR](chapter7/7.5/7.5.1.md)
    - ​		[7.5.1.	mcountinhibit](chapter7/7.5/7.5.1.md)
    - ​	[7.5.2.	mnvec](chapter7/7.5/7.5.2.md)
    - [7.5.3.	msubm](chapter7/7.5/7.5.3.md)
    - [7.5.4.	mmisc_ctl](chapter7/7.5/7.5.4.md)
    - [7.5.5.	msavestatus](chapter7/7.5/7.5.5.md)
    - [7.5.6.	msaveepc1和msaveepc2](chapter7/7.5/7.5.6.md)
    - [7.5.7.	msavecause1和msavecause2](chapter7/7.5/7.5.7.md)
    - [7.5.8.	pushmsubm](chapter7/7.5/7.5.8.md)
    - [7.5.9.	mtvt2](chapter7/7.5/7.5.9.md)
    - [7.5.10.	jalmnxti](chapter7/7.5/7.5.10.md)
    - [7.5.11.	pushmcause](chapter7/7.5/7.5.11.md)
    - [7.5.12.	pushmepc](chapter7/7.5/7.5.12.md)
    - [7.5.13.	sleepvalue](chapter7/7.5/7.5.13.md)
    - [7.5.14.	txevt](chapter7/7.5/7.5.14.md)
    - [7.5.15.	wfe](chapter7/7.5/7.5.15.md)
- [8.	Bumblebee内核低功耗机制介绍](chapter8/8.1.md)
  - [8.1.	进入休眠状态](chapter8/8.1.md)
  - [8.2.	退出休眠状态](chapter8/8.2/8.2.md)
    - [8.2.1.	NMI唤醒](chapter8/8.2/8.2.1.md)
    - [8.2.2.	中断唤醒](chapter8/8.2/8.2.2.md)
    - [8.2.3.	Event唤醒](chapter8/8.2/8.2.3.md)
    - [8.2.4.	Debug唤醒](chapter8/8.2/8.2.4.md)
  - [8.3.	Wait for Interrupt机制](chapter8/8.3.md)
  - [8.4.	Wait for Event机制](chapter8/8.4.md)
