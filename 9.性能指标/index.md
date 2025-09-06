### 系统性能设计 - 性能指标

- 字长和数据通路宽度
- 主存容量和存取速度
- 运算速度
- 吞吐量与吞吐率
- 响应时间 (RT) 与完成时间 (TAT)
- 兼容性

> 主频与 CPU 时钟周期
> CPI 与 IPC
> MIPS 与 MFLOPS

---

**MIPS = 指令条数 / (执行时间 × 10^6) = 主频 / CPI = 主频 × IPC**

**MFLOPS = 浮点操作次数 / (执行时间 × 10^6)**

---

- **CPI (Cycles Per Instruction):** 平均每条指令的平均时钟周期数
- **IPC (Instructions Per Clock):** 每时钟周期的平均指令数 (CPU, instruction per clock)
- **MIPS (Million Instructions Per Second):** 每秒百万条指令 (MIPS, Million Instructions Per Second)
- **MFLOPS (Million Floating-point Operations Per Second):** 每秒百万次浮点操作 (MFLOPS, Million Floating-point Operations per Second)

---

_（图片中手写部分：32bit, 2^32 = 4G）_

## 真题

#### 1. 软件质量属性中，（）是指软件每分钟可以处理多少个请求

- A、响应时间
- B、吞吐量
- C、负载
- D、容量

> 答案：B

#### 2. 某计算机系统的 CPU 主频为 2.8GHz。某应用程序包括 3 类指令，各类指令的 CPI (执行每条指令所需的时钟周期数) 及指令比例如下表所示。

|          | 指令 A | 指令 B | 指令 C |
| :------- | :----: | :----: | :----: |
| **比例** |  35%   |  45%   |  20%   |
| **CPI**  |   4    |   2    |   6    |

执行该应用程序时的平均 CPI 为 ( \_\_\_\_\_ ); 运算速度用 MIPS 表示，约为 ( \_\_\_\_\_ ).

---

**选项:**

**平均 CPI:**
A. 25
B. 3
C. 3.5
D. 4

**MIPS:**
A. 700
B. 800
C. 930
D. 1100

#### 计算过程与答案

1. 计算平均 CPI
   平均 CPI 的计算公式为：

平均  CPI=∑(指令比例
i
​
×CPI
i
​
)

其中，i 代表不同的指令类型。

根据表格数据：

指令 A 的比例为 35%，CPI 为 4

指令 B 的比例为 45%，CPI 为 2

指令 C 的比例为 20%，CPI 为 6

平均  CPI=(0.35×4)+(0.45×2)+(0.20×6)
平均  CPI=1.4+0.9+1.2
平均  CPI=3.5
所以，执行该应用程序时的平均 CPI 为 3.5。

2. 计算 MIPS
   MIPS (Million Instructions Per Second) 的计算公式为：

MIPS=
平均  CPI
主频  (MHz)
​

首先，将 CPU 主频从 2.8 GHz 转换为 MHz：
2.8
textGHz=2.8
times1000
textMHz=2800
textMHz

然后，代入公式：

MIPS=
2800 MHz/3.5
MIPS=800
所以，运算速度用 MIPS 表示，约为 800。

#### 最终答案

- 执行该应用程序时的平均 CPI 为 3.5。

- 运算速度用 MIPS 表示，约为 800。
