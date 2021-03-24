# Windows_Kernel_Resources

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



### Windows Iso

- https://msdn.itellyou.cn/
- https://next.itellyou.cn/





## CheatSheet

- 查看系统信息和补丁信息：
  - `systeminfo`
  - `wmic qfe list full`
  - 输出html格式：`wmic qfe list full /format:htable >C:\Temp\hotfixes.htm `
- 

## Windows Kernel Exploit

### Learn Exploit

- 【HackSysExtremeVulnerableDriver】：windows内核利用技术学习项目
  - [download](https://github.com/hacksysteam/HackSysExtremeVulnerableDriver)

- 【HackSysExtremeVulnerableDriver HEAD tutorail】：HEAD驱动利用教程
  - [English Blog](https://www.fuzzysecurity.com/tutorials.html)



### Update KB info

- https://msrc.microsoft.com/update-guide/
- 

### Token Use

- 【windows-privilege-abuse-auditing-detection-and-defense】：windows token利用
  - [English Blog](https://medium.com/palantir/windows-privilege-abuse-auditing-detection-and-defense-3078a403d74e)
- 【Abusing Token Privileges For EoP】：windows token 利用文章（含代码）
  - [English Paper](https://github.com/hatRiot/token-priv/blob/master/abusing_token_eop_1.0.txt)
  - [download](https://github.com/hatRiot/token-priv)

### GDI Use

- 【Bitmap轶事：Windows 10纪念版后的GDI对象泄露】
  - [中文博客](https://r00tk1ts.github.io/2018/03/21/Bitmaps%E8%BD%B6%E4%BA%8B%EF%BC%9AWindows%2010%E7%BA%AA%E5%BF%B5%E7%89%88%E5%89%8D%E7%9A%84GDI%E5%AF%B9%E8%B1%A1%E6%B3%84%E9%9C%B2/) 
  - [English Blog](https://labs.mwrinfosecurity.com/blog/a-tale-of-bitmaps/)

### Vulerables and Exploits

- https://github.com/SecWiki/windows-kernel-exploits
- https://github.com/abatchy17/WindowsExploits
- https://github.com/Ascotbe/Kernelhub
- https://github.com/WindowsExploits/Exploits
- https://github.com/Heptagrams/Heptagram/tree/master/Windows/Elevation
- https://bugs.hacking8.com/tiquan/：根据KB补丁号或者systeminfo查找对应的exp

### Conclusion

- 【Windows 提权总结】
  - [中文博客](https://www.cnblogs.com/-mo-/p/12718115.html) 

## Analyse

### Analyse Blogs & Papers

- 【Extracting and Diffing Windows Patches in 2020】： 通过Windows更新提取和分析补丁（含代码）
  -  [English Blog](https://wumb0.in/extracting-and-diffing-ms-patches-in-2020.html)

### Analyse Tools & Docs

- 【Windbg】：windows kernel调试工具
  - [download](https://docs.microsoft.com/zh-cn/windows-hardware/drivers/debugger/debugger-download-tools)
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

## Pentest



## Others Resources

- https://labs.f-secure.com
- https://3gstudent.github.io/3gstudent.github.io:有很多从渗透测试角度审视的Windows下提权方法
- https://github.com/3gstudent/Pentest-and-Development-Tips:列举了Windows下渗透测试的Tips
- https://r00tk1ts.github.io
- https://guide.offsecnewbie.com: 见过的最全面的总结
- https://github.com/ExpLife0011/awesome-windows-kernel-security-development
- https://github.com/sam-b/windows_kernel_resources
- https://github.com/itm4n：itm4n大佬，有很多windows分析工具，博客里也有很多干货

