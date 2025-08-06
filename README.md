# LogLInk1K-Win-Tweaks
LogLInk1K-Win-Tweaks 主要用于备份我个人在使用 Windows 11 过程中，为解决一些小问题创建的脚本工具，目前该项目已包括：AMD显卡驱动版本查询修改恢复，右键菜单去除AMD Software、右键菜单添加在终端中打开等功能

**⚠️ 重要提示：**  

> 未经过更多测试，个人系统及版本为 Windows11 Pro 24H2<br>同时该系统已通过 [ExplorerPatcher](https://github.com/valinet/ExplorerPatcher) 禁用 Win11 右键菜单<br>以下有关右键菜单的脚本无法保证在 Win11 右键菜单中同样可用<br>所有脚本均属于我的个人解决方案，若使用即表示您了解相关风险

## 🔧 脚本集

| 脚本名称 | 功能 |
|----------|------|
| [AMD显卡驱动版本查询.bat](/AMD_Tools/AMD显卡驱动版本查询.bat) | 快速检测当前驱动版本号 | 无需打开注册表，即可验证对驱动版本的修改是否生效 |
| [AMD显卡驱动版本修改.reg](/AMD_Tools/AMD显卡驱动版本修改.reg) | 修改显卡驱动版本信息 | 绕过旧游戏，以及新游戏的驱动版本检测 |
| [AMD显卡驱动版本恢复.reg](/AMD_Tools/AMD显卡驱动版本恢复.reg) | 还原显卡驱动版本信息 | 修复因版本修改导致的兼容问题 |
| [AMD-Software移除-方法1.reg](/AMD_Tools/AMD-Software移除-方法1.reg) | 通过注册表移除右键菜单中的 AMD Software:Adrenalin Edition|
| [AMD-Software恢复-方法1.reg](/AMD_Tools/AMD-Software恢复-方法1.reg) | 通过注册表恢复右键菜单中的 AMD Software:Adrenalin Edition|
| [AMD-Software移除-方法2.txt](/AMD_Tools/AMD-Software移除-方法2.txt) | 通过PowerShell命令来彻底移除右键菜单中的 AMD Software:Adrenalin Edition |
| [添加在终端中打开.reg](/Desktop_Tweaks/添加在终端中打开.reg) | 为右键菜单添加"在终端中打开"选项 |
| [移除在终端中打开.reg](/Desktop_Tweaks/移除在终端中打开.reg) | 为右键菜单移除"在终端中打开"选项 |

## 脚本来由

- 对AMD显卡驱动版本的修改，主要是为了绕过一些旧游戏或者新游戏对AMD显卡驱动版本的检测。
- 这些检测通常都很好绕过，修改注册表后一般不用重启电脑即可打开游戏。
- 但如果版本修改成功后未进行恢复就重启电脑，看网上的大伙说会无法打开AMD Software，所以一般我个人使用这个方案来过检测是遇到特定游戏有限制时修改版本，游戏退出后就恢复原来的驱动版本，而这些操作没有必要总是一次次地打开注册表进行修改，于是写成.reg，用以快速切换版本。

---

- 之所以想移除右键菜单中的 AMD Software:Adrenalin Edition ，主要是因为这一串太长了，显得右键菜单的窗口大小很臃肿，右键菜单打开速度缓慢，而且一般我想使用 AMD Software 时，主要的打开方式是通过 Windows 右下角的托盘菜单里的 AMD Software 来打开。
- 两个方法的区别主要是方法2无法恢复，需要重新安装AMD显卡驱动才能恢复右键菜单中的 AMD Software:Adrenalin Edition

---

- 添加在终端中打开.reg的产生，其实与以上的AMD Software移除-方法1有关
- 通过方法1的方式来移除右键菜单中的 AMD Software:Adrenalin Edition 后，会莫名导致系统原本的“在终端中打开”消失（暂不清楚是否会影响更多的右键菜单选项），所以需要自行添加一个作为替代

---