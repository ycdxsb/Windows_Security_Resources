# Windows_Kernel_Resources

> 在学习Windows kernel时搜集到的资源列表

## Learn Windows

### Books

- 《寒江独钓——Windows内核安全编程》
- 《天书夜读——从汇编语言到Windows内核编程》
- 《Windows内核情景分析》上下册
- 《Windows驱动开发技术详解》
- 《深入解析Windows操作系统(第6版)》上下册

### Source Code

- 【The Windows Research Kernel AKA WRK】
  - [download](https://github.com/zhuhuibeishadiao/ntoskrnl)
- 【ReactOS：A free Windows-compatible Operating System】
  - [download](https://github.com/reactos/reactos)

### Windows iso

- https://msdn.itellyou.cn/
- https://next.itellyou.cn/

### Windows Structure

- 【关键的windows内核数据结构一览(上)】
  - [中文博客](https://r00tk1ts.github.io/2018/01/08/%E5%85%B3%E9%94%AE%E7%9A%84Windows%E5%86%85%E6%A0%B8%E6%95%B0%E6%8D%AE%E7%BB%93%E6%9E%84%E4%B8%80%E8%A7%88%EF%BC%88%E4%B8%8A%EF%BC%89/)

- 【关键的windows内核数据结构一览(下)】
  - [中文博客](https://r00tk1ts.github.io/2018/01/14/%E5%85%B3%E9%94%AE%E7%9A%84Windows%E5%86%85%E6%A0%B8%E6%95%B0%E6%8D%AE%E7%BB%93%E6%9E%84%E4%B8%80%E8%A7%88%EF%BC%88%E4%B8%8B%EF%BC%89/)
- 【Catalog of key Windows kernel data structures】
  - [English Blog](https://codemachine.com/articles/kernel_structures.html)

## Windows Kernel Exploit

### KB and Patch

- https://msrc.microsoft.com/update-guide/：官方KB对应补丁信息
- https://bugs.hacking8.com/tiquan/：根据KB补丁号或者systeminfo查找对应的exp
- 【Extracting and Diffing Windows Patches in 2020】： 通过Windows更新提取和分析补丁（含代码）
  -  [English Blog](https://wumb0.in/extracting-and-diffing-ms-patches-in-2020.html)



### Exploits

- https://github.com/SecWiki/windows-kernel-exploits
- https://github.com/nu11secur1ty/Windows10Exploits
- https://github.com/abatchy17/WindowsExploits
- https://github.com/Ascotbe/Kernelhub
- https://github.com/WindowsExploits/Exploits
- https://github.com/Heptagrams/Heptagram/tree/master/Windows/Elevation



### Tools & Docs

- 【Windbg】：windows kernel调试工具
  - [download](https://docs.microsoft.com/zh-cn/windows-hardware/drivers/debugger/debugger-download-tools)
- 【Windbg Preview】：windows kernel调试工具(美观)
  - [download](https://www.microsoft.com/en-us/p/windbg-preview/)
- 【dbgview】：windows调试工具，捕获调试信息，用于Guest
  - [download](https://docs.microsoft.com/en-us/sysinternals/downloads/debugview)
- 【OSRLoader】：驱动管理工具（安装，启动，暂停，卸载）
  - [download](https://www.osronline.com/article.cfm%5earticle=157.htm)
- 【VirtualKD】：双机调试工具，较老，不支持最新版VMWare
  - [download](https://sysprogs.com/legacy/virtualkd/)
- 【VirtualKD-Redux】：双机调试工具，支持最新版本VMWare
  - [download](https://github.com/4d61726b/VirtualKD-Redux)
- 【accesschk】
  - [download](https://docs.microsoft.com/en-us/sysinternals/downloads/accesschk)
- 【oleview】
  - [download](https://github.com/tyranid/oleviewdotnet)
- 【process monitor】
  - [download](https://docs.microsoft.com/en-us/sysinternals/downloads/procmon)
- 【Windows-Kernel-Explorer】
  - [download](https://github.com/AxtMueller/Windows-Kernel-Explorer/)
- 【sandbox-attacksurface-analysis-tools】
  - [download](https://github.com/googleprojectzero/sandbox-attacksurface-analysis-tools)
- 【SystemExplorer】
  - [download](https://github.com/zodiacon/SystemExplorer)
- 【ProcessHacker】
  - [download](https://processhacker.sourceforge.io/downloads.php)

### Blogs && Talks && Workstation

- 【Windows 提权总结】
  - [中文博客](https://www.cnblogs.com/-mo-/p/12718115.html) 

- 【Level Up! Practical Windows Privilege Escalation - Andrew Smith】
  - [Youtube](https://www.youtube.com/watch?v=PC_iMqiuIRQ)

## Learn Exploit

### HEVD

https://bbs.pediy.com/user-831334.htm

https://rootkits.xyz/blog/

https://www.fuzzysecurity.com/tutorials.html

https://github.com/h0mbre/Windows-Exploits/tree/162dfd45d284556b47739835116a962177b243b0/Exploit-Code/HEVD

- 【HackSysExtremeVulnerableDriver】：windows内核利用技术学习项目
  - [download](https://github.com/hacksysteam/HackSysExtremeVulnerableDriver)
- 【HEVD StackOverflow】：

  - [win7sp1 x86 python2.7 exp](https://github.com/h0mbre/Windows-Exploits/blob/162dfd45d284556b47739835116a962177b243b0/Exploit-Code/HEVD/x86_StackOverflow.py)
  - [HEVD内核漏洞之栈溢出writeup](https://bbs.pediy.com/thread-252775.htm)
  - [HEVD栈溢出writeup](https://50u1w4y.github.io/site/HEVD/stackoverflow/)



### Token Abuse

- 【windows-privilege-abuse-auditing-detection-and-defense】：windows token利用
  - [English Blog](https://medium.com/palantir/windows-privilege-abuse-auditing-detection-and-defense-3078a403d74e)

### GDI Abuse

- 【Bitmap轶事：Windows 10纪念版后的GDI对象泄露】
  - [中文博客](https://r00tk1ts.github.io/2018/03/21/Bitmaps%E8%BD%B6%E4%BA%8B%EF%BC%9AWindows%2010%E7%BA%AA%E5%BF%B5%E7%89%88%E5%89%8D%E7%9A%84GDI%E5%AF%B9%E8%B1%A1%E6%B3%84%E9%9C%B2/) 
  - [English Blog](https://labs.mwrinfosecurity.com/blog/a-tale-of-bitmaps/)

- 【exp in GDI】
  - [中文pdf](http://www.vxjump.net/files/seccon/exp-in-gdi.pdf)



### Paper

- 【Abusing Token Privileges For EoP】：windows token 利用文章（含代码）
  - [Paper](https://github.com/hatRiot/token-priv/blob/master/abusing_token_eop_1.0.txt)
  - [Code](https://github.com/hatRiot/token-priv)



## Other Resources

- https://labs.f-secure.com
- https://3gstudent.github.io/3gstudent.github.io:有很多从渗透测试角度审视的Windows下提权方法
- https://github.com/3gstudent/Pentest-and-Development-Tips:列举了Windows下渗透测试的Tips
- https://r00tk1ts.github.io/tags/windows-kernel/
- https://guide.offsecnewbie.com: 见过的最全面的总结
- https://github.com/ExpLife0011/awesome-windows-kernel-security-development
- https://github.com/sam-b/windows_kernel_resources
- https://github.com/itm4n：itm4n大佬，有很多windows分析工具，博客里也有很多干货
- https://github.com/sailay1996/awesome_windows_logical_bugs
- https://github.com/topics/windows-privilege-escalation
- http://www.fuzzysecurity.com/tutorials/16.html

