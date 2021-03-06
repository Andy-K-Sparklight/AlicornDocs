*LC-1*

# 启动

?> **本页面介绍的是：用于启动游戏的界面**  
有关 Alicorn 启动游戏的机理和特性，请参见 [TEC-1 启动机理](/TEC-1.md)

启动游戏。

## 概述

启动页面是 Alicorn 中最重要的页面，它用于直接启动游戏。此页面也包含启动游戏时的即时选项，例如在启动前选定 Java 运行时。

![.](https://img.gejiba.com/images/3379a66907153fb19da2ee791abd9e58.png)

## 范例

### 启动游戏

从启动台单击任何核心卡片后，来到的就是启动游戏界面。

1. 单击中央的启动按钮，游戏就会启动。

2. 如果你从未使用此核心，Alicorn 将要求你选择帐户。
   
   对于 Microsoft 帐户，**它是即时可用的**。也就是说，就算你从未在 Alicorn 上使用过 Microsoft 帐户，也可以选择它并直接单击「继续」而无需额外的配置。稍后 Alicorn 将完成验证。
   
   若使用本地帐户，还可在此键入玩家名（默认是 Player）。
   
   若使用 Yggdrasil 帐户（这包括老版本 Mojang 帐户以及第三方验证），需要转到**帐户管理器**中先行配置，请参见 [AM-1 帐户管理器](/AM-1.md)

![.](https://img.gejiba.com/images/f3e6023810b8881a397f922ed08c5758.png)

3. 启动继续。如果帐户凭据仍然有效，Alicorn 不需要任何交互，启动将仍然继续。
   
   如果你的 Microsoft 帐户尚未登录，或者登录凭据已经过期，Alicorn 将弹出一个浏览器窗口让你完成 Microsoft 登录。通常情况下，登录完成后，启动将继续。如果出现了一些异常情况，可以跟随 Alicorn 的提示继续操作。有关异常登录的处理方法，请参见 [LG-1 登录遇到问题](/LG-1.md)
   
   对于 Yggdrasil 帐户，如果凭据已经过期，帐户验证将失败。游戏仍然会继续启动，但你的帐户将不可用，你需要转到**帐户管理器**中重新进行验证。

4. Alicorn 检查和补全文件。如果这是你第一次启动某个核心，那么很可能需要下载一些文件，请稍安勿躁。不定长进度条下方会显示剩余文件数，由于设计原因，有时候这个数字可能会在一个地方等很久（例如，持续一分钟都显示「剩余 6 个文件」），这是正常的，请耐心等待下载完成。如果这个时间看上去已经远远超过了正常时间，请重新启动 Alicorn，再试一次。有时这是由一些比较复杂的原因引起的，请参见 [LC-2 启动遇到问题](/LC-2.md)

5. Alicorn 完成 Mod 的移动，并且生成启动参数，这两步几乎在瞬间完成。然后游戏就启动了。如果正常使用（比如每天都玩一次），总启动时间一般不会超过 10 秒。启动完成后，「完毕」图标会亮起。

![.](https://img.gejiba.com/images/094fbccb8b44f53ecfc8eb27b8503907.png)

---

### 查看系统用量

启动页面下方将显示内存（RAM）用量和中央处理器（CPU）平均负载。如果系统看上去「不是很适合启动游戏」，请关闭一些其它应用程序。Minecraft 通常至少需要 2 GiB 内存流畅运行。如果使用 Mod、资源包或光影，需要的内存会更多。

---

### 高级启动

启动下方有三个选项用于高级启动。

**模拟启动**将执行全部启动操作，但不会创建 Java 进程，可用于排查问题。

**安全启动**将禁用大多数快速启动选项，并重新进行一次标准启动。如果启动遇到问题，使用此选项再试一次。

**选择帐户**要求重新选择帐户。除第一次启动外，Alicorn 将记住你的帐户选择并且不再询问，使用此选项来重选帐户。

高级选项不会被记住，且初始化时总是为未勾选状态。

---

### 选取 Java 运行时

启动前任何时刻都可以选择一个用于启动的 Java 运行时。此选择只对当前核心生效，而且会被记住。

Alicorn 会尝试检查所选 Java 运行时的版本和当前 Minecraft 的兼容性，如果不兼容，选择框的下方将出现一行橙色警告，告知 Java 版本存在的问题。

如果选择「自动」，Alicorn 将尝试选择一个合适的 Java 运行时，但如果她找不到合适的，则将使用 **Java 选择器**页面中的默认设置，警告依然会显示。通常当这种情况出现时，无法通过选择其它的 Java 来使警告消失，相反，应当再安装一个合适的 Java，请参见 [JV-1 Java 选择器](/JV-1.md)

如果你知道你在做什么（比如你使用一个深度修改后的 Minecraft 客户端），可以忽略本警告。

---

### 强制结束游戏

在 Alicorn 启动游戏完成后，启动按钮将变为**强制结束**按钮，它通过操作系统**强制立即结束** Minecraft 的进程。

如果游戏看上去已经不太正常了，并且无法通过常规方法退出游戏，可以使用本按钮，但同样，它只应当被作为最后手段。在大多数平台上，这样结束游戏也会触发崩溃检查。

---

### 检查游戏崩溃

当游戏崩溃时，如果 Alicorn 仍然开启，Alicorn 会捕获这一信号并报告崩溃。

如果游戏没有正常运行，点击「是的，为我分析问题」将前往**启动疑难解答**页面。Alicorn 会尽可能多地收集信息，请参见 [CA-1 启动疑难解答](/CA-1.md)

![.](https://img.gejiba.com/images/facde78f4c3c8041551634d0e0df7414.png)

---

### （跨）局域网联机

若在 Minecraft 中使用了「对局域网开放」，Alicorn 将捕获这一信号，并询问你是否需要联机支持。在这里可以使用设置生成**友谊接力代码**（或称 CC 码），更详细的信息请参见 [CC-2 使用友谊接力联机](/CC-2.md)

若你错过了第一次点击的机会，启动按钮会变为**启动联机按钮**，以允许你重新打开此窗口。

![.](https://img.gejiba.com/images/840905fcf5bc4cc4d7c7617daf6836c6.png)

## 描述

此页面有以下功能：

- **启动按钮**：用于启动游戏的主按钮。这个按钮有以下三种状态：
  
  - **启动待命**：在游戏并未完全启动时均为此状态，图标显示为「起飞」。如果启动任务当前不在执行（例如，刚刚进入这里），将可以点击，否则会被禁用。单击将开始执行启动任务。
  
  - **强制结束**：游戏进程已经开始运行时为此状态，图标显示为「降落」。单击将发送强制结束信号 9（即 SIGKILL）到游戏进程，从而立即无条件关闭游戏。通常这会进一步触发检查游戏崩溃，这是因为进程退出代码不为 0。
  
  - **启动联机**：游戏进程正在运行，并且当前世界已经对局域网开放时为此状态，图标显示为「广播」。单击将打开联机配置窗口。

- **临时 Java 选择**：用于选择启动本核心的 Java 运行时，所选的值将被记住。可选项包括在 **Java 选择器**中搜索到的 Java（若使用 Alicorn 安装则只会包含所安装的）以及一个额外的「默认/自动」。当选择「默认/自动」时，Alicorn 会尝试选择一个正确的 Java 用于运行。
  
  这一选择框的下方同时也显示 Java 与 Minecraft 的兼容性，并且如果有问题，会给出对应的警告，即使选择「默认/自动」也是如此。如果 Alicorn 找不到合适的 Java，所显示的警告是默认 Java 与 Minecraft 版本的比较；否则（如果兼容），将不会显示任何内容。
  
  若在两次自动选择之间未对 Java 列表进行修改，则对于同一核心，「默认/自动」总是会选择同一个 Java。

- **Tips**：显示于不定长进度条下方~~放飞自我~~的 Tips，可在选项中关闭。

- **MiniWiki**：显示于启动按钮下方的 MiniWiki，可在选项中关闭。点击它可以立即切换一个条目。

- **系统资源状况**：以两条进度条显示，靠上的为内存（RAM）用量，而靠下的为中央处理器（CPU）平均负载。这里的值是通过操作系统接口估算出来的，进度条越长表明占用量越高，即越不适合启动游戏。
  
  内存用量统计时，可用内存空间**不会**包含缓冲和缓存区，尽管它们可以随时被系统释放，因此占用量的计算值总是稍高于实际值。
  
  CPU 平均负载为过去 5 秒内的平均负载，单位是「核」。例如，3.0 的平均负载，对于只装载了双核 CPU 的机器是过载，而对于装载有八核 CPU 的机器，就还有一大半的计算能力没有被使用。

- **监测崩溃**：当游戏进程结束，并且退出代码不为 0 时，Alicorn 将认为游戏已经崩溃，并弹出窗口询问是否需要进一步分析。如果单击继续，Alicorn 会截取自启动以来的所有日志，并转到**启动疑难解答**页面。

- **联机辅助**：当一个世界对局域网开放时，Alicorn 会检测到这一变化，可在选项中禁止这一行为。当启用时，Alicorn 会弹出窗口并辅助你进行联机。

## 注意事项

- **系统用量统计并非 100% 准确**。此功能依赖操作系统提供的数据，因而数据可能有延迟或误差。若要精准测量用量，请使用 `top` 或者「任务管理器」。

- **模拟启动仅用于调试**。它不会创建进程，因而也并不能游玩 Minecraft。

- **避免使用强制退出**。强制退出时，操作系统将立即无条件地结束掉游戏进程（SIGKILL），而不会让它有保存数据或清理的机会。这意味着如果你正在游玩一个世界，然后 Minecraft 卡住了，假使你这时强制退出，那么自上次保存（通常是单人游戏中按 Esc）以来，你对世界的修改会丢失。更糟糕的是，存档可能会损坏。如果有可能，尝试使用常规的方法关闭 Minecraft。

- **关闭 Alicorn 不能关闭 Minecraft**。反之亦然。尽管 Minecraft 是 Alicorn 的子进程，但它已被设为单独运行，因此即使 Alicorn 关闭，Minecraft 也将继续运行，而且你将无法在它崩溃的时候再收到 Alicorn 的提示信息了！——所以，不要这样做。

- **启动操作开始后无法暂停或取消**。Alicorn 会将启动任务一并提交到总线以求更好的性能，但这样部署的任务正如泼出去的水，是不能回收的。如果一定要强制中止启动，请使用关闭按钮关闭 Alicorn。否则，即使切换页面（并且忽略警告），启动过程依然会继续。

- **Java 兼容性为与原版 Minecraft 的兼容性**。这意味着 Mod 加载器的兼容性不会被考虑。事实上，对于 Forge，其出现错误的情况十分复杂而且随机（例如，原版 1.16 完全可以使用 Java 16 来启动，而如果安装了 Forge 再使用 Java 16，就会出现错误）；而对于 Fabric，通常与原版兼容时，与该版本下的 Fabric 也同样兼容。
  
  这一特性也说明，如果 Alicorn 报告不兼容，则很大概率是真的不兼容，但反过来则不是这样。

## 参见

- [TEC-1 启动机理](/TEC-1.md)
- [AM-1 帐户管理器](/AM-1.md)
- [LG-1 登录遇到问题](/LG-1.md)
- [LC-2 启动遇到问题](/LC-2.md)
- [JV-1 Java 选择器](/JV-1.md)
- [CA-1 启动疑难解答](/CA-1.md)
- [CC-2 使用友谊接力联机](/CC-2.md)
- [MX-1 Mod 动态加载](/MX-1.md)

## 跋

ThatRarityEG 编写于 2022/02/04
