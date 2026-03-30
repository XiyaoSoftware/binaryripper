# binaryripper
Binary Ripper™ 是一款支持 HarmonyOS Ark 和 Android Dalvik 字节码反编译的商业反编译工具。本仓库用于发布免费、非商业版Binary Ripper，跟踪公开问题和缺陷报告。商业用途与授权请联系：sales@binaryripper.com。

[English](README.md)

## 关键特性

### 扁平异常结构化模式
将**正常执行流**与**异常处理流**分离，使分析更专注于主执行路径，该模式可显著提升涉及异常控制流代码的可读性与理解效率。
<details>
  <summary><strong>观看演示</strong></summary>
  <br/>
  <img src="docs/demo/ExceptionStructuringMode.gif"/>
</details>

### 图形 CFG 边交互模式
采用一种新的 CFG 边交互模型，支持在基本块间快速、确定性的双向导航。

- **点击边** 可将箭头端点移动到光标位置
- **点击箭头** 可将反向端点移动到光标位置

<details>
  <summary><strong>观看演示</strong></summary>
  <br/>
  <img src="docs/demo/EdgeInteraction.gif"/>
</details>

### 高级图形 CFG 总览模式

#### 循环信息
展示**嵌套循环结构**，包含循环入口与循环成员。

#### 区域信息
展示**嵌套 SESE 区域结构**，包含区域入口、成员与出口。

#### 基本块导航图
将所有**基本块**可视化为**单元格**，用于：
- 快速定位特定基本块
- 评估函数整体规模
- 通过高亮循环与区域成员评估其规模

<details>
  <summary><strong>观看演示</strong></summary>
  <br/>
  <img src="docs/demo/BlockMap.gif"/>
</details>

---

### 图形 CFG 自动分组（折叠）
支持将选定的**循环与区域**折叠为单个节点，降低 CFG 复杂度并提升图形可读性。

<details>
  <summary><strong>区域信息与折叠</strong></summary>
  <br/>
  <img src="docs/demo/RegionFolding.gif"/>
</details>

<details>
  <summary><strong>循环信息与折叠</strong></summary>
  <br/>
  <img src="docs/demo/LoopFolding.gif"/>
</details>


## 功能矩阵

| 功能 | 免费版 |
|--------|:----:|
| Ark，Dalvik字节码反汇编 | ✓ |
| Ark，Dalvik字节码反编译 | — |
| &nbsp;&nbsp;- 反编译单个方法 | ✓ |
| &nbsp;&nbsp;- 反编译整个类 | — |
| 跨过程词法变量恢复 | — |
| 异常处理结构化模式 | — |
| &nbsp;&nbsp;- 层级化结构化 | ✓ |
| &nbsp;&nbsp;- 扁平结构化 | — |
| &nbsp;&nbsp;- 禁用异常处理 | — |
| 图形 CFG 视图 | — |
| &nbsp;&nbsp;- 边交互模式 | ✓ |
| &nbsp;&nbsp;- 自动分组（折叠）| — |
| 图形 CFG 总览视图 | — |
| &nbsp;&nbsp;- 迷你图（Mini Graph） | ✓ |
| &nbsp;&nbsp;- 循环信息 | — |
| &nbsp;&nbsp;- 区域信息 | — |
| &nbsp;&nbsp;- 基本块导航图 | — |
| 反汇编与伪代码视图同步 | — |
| 解码安卓AndroidManifest.xml和ARSC资源文件 | ✓ |

## 支持与联系

- **问题反馈与功能请求**：GitHub Issues 或 support@binaryripper.com
- **商业授权与销售**：sales@binaryripper.com
- **其他咨询**：contact@binaryripper.com

## 免责声明

Binary Ripper 是**闭源商业产品**，本仓库**不包含源代码**。
