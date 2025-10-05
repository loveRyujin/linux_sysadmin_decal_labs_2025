## part1
### question3
pwd -> prints the current working directory

### question4
ll -> lists the files in the current directory, including hidden files
cat .secret -> output: hunter2

### question5
cat nosense/* -> output: stanford > berkeley

### question6
rm nosense/* -> removes the files in the nosense directory

### question7
grep xxx big_data.txt

less big_data.txt
:/https -> search for the string https in the file

answer: THE SOLUTION IS MORE COFFEE

### question8
chmod +x a_script.sh -> makes the script executable

### question9
echo "lee" > hello_world

## part2
### question1
 Linux 和 macOS（基于 BSD/Unix）与 Windows 之间最常见的差异主要体现在以下几个方面：

  - 内核与系统架构：Linux 和 macOS 都是 Unix 家族的一员，使用 POSIX 兼容的内核与 API；Windows 使用 NT 内核，系统调用与内
    部结构完全不同。
  - 文件系统与路径语义：类 Unix 系统使用 / 作为路径分隔符、区分大小写、将设备视为文件，权限模型基于所有者/组/其它；
    Windows 以 \ 分隔路径，通常不区分大小写（NTFS 可选），权限体系以 ACL 为主，盘符与设备管理方式不同。
  - 软件生态与包管理：Linux 发行版和 macOS 倾向于通过包管理器（APT、DNF、Homebrew 等）统一安装/升级软件；Windows 传统上
    依赖可执行安装包，近年来才引入 winget、WSL 等工具。
  - 默认 Shell 与 CLI 文化：Linux/macOS 默认提供 POSIX shell（bash/zsh），系统管理大量依赖终端；Windows 主要是
    PowerShell/CMD，功能、语法、脚本生态完全不同。
  - 开源与授权模式：大多数 Linux 发行版是开源的，macOS 内核部分开源但上层闭源，Windows 为商业闭源，开放程度影响系统可定
    制性与社区支持方式。
  - 系统管理与配置：类 Unix 系统广泛使用文本配置、日志文件、systemd/launchd 等服务管理工具；Windows 则依赖注册表、图形化
    管理工具、服务控制管理器等。

  这些差异导致开发、部署、系统维护的思路与工具链有显著不同，也解释了为何许多跨平台工具需要针对两类体系做适配。

### question2
 - 交互方式：命令行靠键盘输入指令，输出文本；图形界面主要通过鼠标/触摸操作窗口、按钮、菜单。
  - 效率与脚本化：命令行可批量执行、写脚本、自动化任务，重复操作效率高；图形界面更直观易上手，但自动化能力较弱。
  - 功能覆盖：部分系统管理、开发工具只提供 CLI 接口；相反，一些图形应用（如设计软件）只能通过 GUI 使用。
  - 资源占用：命令行环境轻量、适合远程连接和低资源场景；图形界面消耗更多内存和 GPU，适合需要视觉反馈的任务。
  - 学习曲线：命令行对新手不够友好，需记忆命令；图形界面直观、反馈及时，易于初学者上手。

### question3
在 Linux 文件系统里，“根目录”（/）是整个层级结构的起点，也是所有路径解析的参考框架。可以从几个层面理解：

  - 单一入口的树状结构：类 Unix 系统采用统一的目录树，全局只有一个 / 作为根节点。所有分区、设备、用户目录、系统文件都在
    这棵树上“挂载”，没有 Windows 式的盘符。
  - 路径解析基准：以 / 开头的绝对路径，从根目录依次向下查找；当前工作目录与 .、.. 等相对路径都借助这棵树来定位。
  - 命名空间聚合点：设备节点（/dev）、进程信息（/proc）、可挂载的虚拟文件系统（/sys）都被挂在 / 下的相应目录，对用户呈现
    出统一命名空间。
  - 权限与访问控制起点：/ 本身通常归 root 用户所有，只有管理员才可修改其直接结构；其他用户的目录权限在此基础上层层继承。
  - 运行环境依赖：引导流程、动态链接器、守护进程等关键组件的默认位置都以 / 为基准（如 /bin, /etc, /lib, /sbin 等）。

  概念上，可以把根目录视作整个系统文件命名空间的“世界坐标原点”：所有文件、目录、挂载点都会通过它组织成一棵结构化、统一
  的树。

### question4
  - -l：长格式，显示权限、所有者、所属组、大小、最后修改时间。
  - -t：按最后修改时间排序（默认最新在前）。
  - -r：反转排序，因而最旧的文件排在最上面。
  - -h：以人类可读的单位显示大小（KB/MB 等）。
ls -ltrh

### question5
head -n 4 big_data.txt

### question6
- cat foo > out.txt 会把 foo 的内容写入 out.txt，在写入之前会先清空/覆盖 out.txt 原有的内容；
- cat foo >> out.txt 则会把 foo 的内容追加到 out.txt 末尾，不会清空原内容。

### question7
  - Permissive 许可证（如 MIT、BSD、Apache）：只要保留版权和许可证声明，就允许自由使用、修改、再分发，甚至可以闭源发布，
    限制极少。
  - Copyleft 许可证（如 GPL、AGPL）：允许使用和修改，但要求任何分发的衍生作品继续以相同的 copyleft 许可证开源，从而强制
    保持自由性。

### question8
MIT License

### question9
  - 开源软件：VS Code（它的源代码在 MIT 许可证下公开）。
  - 免费但闭源的软件：Google Chrome（可以免费使用，不过源代码并不公开）。