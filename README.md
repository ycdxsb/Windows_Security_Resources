# Windows_Kernel_Resources

> 在学习Windows kernel时搜集到的资源列表
- [Windows_Kernel_Resources](#windows_kernel_resources)
  - [Windows基础知识](#windows基础知识)
    - [Windows相关书籍](#windows相关书籍)
    - [Windows相关源代码](#windows相关源代码)
    - [Windows API编程](#windows-api编程)
    - [Windows镜像下载](#windows镜像下载)
  - [Windows 内核漏洞利用技术](#windows-内核漏洞利用技术)
    - [内核利用基础知识](#内核利用基础知识)
    - [内核调试工具](#内核调试工具)
    - [HEVD 内核利用教程](#hevd-内核利用教程)
    - [token 权限滥用](#token-权限滥用)
    - [GDI 滥用提权](#gdi-滥用提权)
      - [BitMap  RS1(v1607)前](#bitmap--rs1v1607前)
      - [Accelerator Table RS1(v1607)](#accelerator-table-rs1v1607)
      - [lpszMenuName RS2(v1703)](#lpszmenuname-rs2v1703)
      - [Palette RS3 (v1709)](#palette-rs3-v1709)
      - [综述](#综述)
    - [堆利用](#堆利用)
    - [保护绕过](#保护绕过)
    - [Payload](#payload)
    - [综述](#综述-1)
  - [Windows 服务漏洞](#windows-服务漏洞)
    - [任意文件移动/dll劫持](#任意文件移动dll劫持)
    - [分析工具](#分析工具)
  - [Windows 漏洞分析](#windows-漏洞分析)
    - [Windows 补丁分析](#windows-补丁分析)
    - [Windows 漏洞集合](#windows-漏洞集合)
    - [CVE漏洞分析](#cve漏洞分析)
      - [CVE-2020-1054 堆越界读写](#cve-2020-1054-堆越界读写)
      - [CVE-2020-0796 SMB Ghost 整数溢出漏洞](#cve-2020-0796-smb-ghost-整数溢出漏洞)
      - [CVE-2020-0787 BITS任意文件移动漏洞](#cve-2020-0787-bits任意文件移动漏洞)
      - [MS16-098 堆越界写](#ms16-098-堆越界写)
      - [MS15-010 UAF](#ms15-010-uaf)
    - [Windows 分析工具](#windows-分析工具)
  - [Windows 渗透测试](#windows-渗透测试)
    - [攻击面分析](#攻击面分析)
    - [渗透测试工具](#渗透测试工具)
    - [本地提权工具](#本地提权工具)
    - [渗透测试常用漏洞](#渗透测试常用漏洞)
      - [MS17-010 永恒之蓝](#ms17-010-永恒之蓝)
    - [综述](#综述-2)
  - [Paper](#paper)
  - [Fuzz](#fuzz)
  - [Misc](#misc)
  - [综合性资源](#综合性资源)
## Windows基础知识

### Windows相关书籍
- 《寒江独钓——Windows内核安全编程》
- 《天书夜读——从汇编语言到Windows内核编程》
- 《Windows内核情景分析》上下册
- 《Windows驱动开发技术详解》
- 《深入解析Windows操作系统(第6版)》上下册
- 《COM技术内幕》

### Windows相关源代码
- 【The Windows Research Kernel AKA WRK】
  - [download](https://github.com/zhuhuibeishadiao/ntoskrnl)
- 【ReactOS：A free Windows-compatible Operating System】
  - [download](https://github.com/reactos/reactos)
- 【泄露的Windows内核源码 NT5】
  - [download](https://github.com/cryptoAlgorithm/nt5src)
  - [download](https://github.com/travismills82/nt5src)
- 【泄露的windows server 2003源代码】
  - [download](https://github.com/PubDom/Windows-Server-2003)

### Windows API编程

- 【pywin32】
  - [download](https://github.com/mhammond/pywin32)
- 【pythonforwindows】
  - [download](https://github.com/hakril/PythonForWindows)

- 【WinAPI-Tricks】
  - [download](https://github.com/vxunderground/WinAPI-Tricks)
- 【windows_kernel_address_leaks】
  - [download](https://github.com/sam-b/windows_kernel_address_leaks)

### Windows镜像下载
- https://msdn.itellyou.cn/
- https://next.itellyou.cn/
- Win10版本关系：https://en.wikipedia.org/wiki/Windows_10_version_history
- Win 7 sp1
  - `ed2k://|file|cn_windows_7_professional_with_sp1_vl_build_x64_dvd_u_677816.iso|3266004992|5A52F4CCEFA71797D58389B397038B2F|/`
  - `ed2k://|file|cn_windows_7_professional_with_sp1_vl_build_x86_dvd_u_677939.iso|2502909952|935E5B4B754527BE3C238FA6ABDD9B86|/`
- Win8
  - `ed2k://|file|cn_windows_8_x64_dvd_915407.iso|3652950016|5C7F8C212BD3A1827866563773A431C2|/`
  - `ed2k://|file|cn_windows_8_x86_dvd_915414.iso|2679801856|9AF10141BFD61BC66D9D6459758D7749|/`
- Win10 1507
  - `ed2k://|file|cn_windows_10_education_x64_dvd_6847843.iso|4159854592|50A2126871A73D48FAE49D7D928D5343|/`
  - `ed2k://|file|cn_windows_10_education_x86_dvd_6847858.iso|3097344000|E65D0B95FC75EC17FA6E72DC7433B46F|/`
- Win10 1511
  - `ed2k://|file|cn_windows_10_education_version_1511_x64_dvd_7223792.iso|4051984384|C02180B4599239E5F7B9A7FE18B1C89E|/`
  - `ed2k://|file|cn_windows_10_education_version_1511_x86_dvd_7223795.iso|3057567744|3A9BE18EEFCE9A31B6C93AA710DE5B49|/`
- Win10 1607
  - `ed2k://|file|cn_windows_10_education_version_1607_updated_jul_2016_x64_dvd_9056220.iso|4150953984|AD0737D5F182082C37E6D1DB7CCDBB77|/`
  - `ed2k://|file|cn_windows_10_education_version_1607_updated_jul_2016_x86_dvd_9056381.iso|3103516672|BA95618BB3D14C0B91A7D6D2518DCCFC|/`
- Win10 1703
  - `ed2k://|file|cn_windows_10_education_version_1703_updated_march_2017_x64_dvd_10194187.iso|4470315008|BA9D2AB8865B80C2227E6E08BB2DD2AE|/`
  - `ed2k://|file|cn_windows_10_education_version_1703_updated_march_2017_x86_dvd_10189568.iso|3401973760|5DD08371AF9B6E953F879E574D593607|/`
- Win10 1709
  - `ed2k://|file|cn_windows_10_multi-edition_version_1709_updated_sept_2017_x64_dvd_100090804.iso|4740610048|37051C54894776826823DAEBDD03F1DC|/`
  - `ed2k://|file|cn_windows_10_multi-edition_version_1709_updated_sept_2017_x86_dvd_100090805.iso|3551899648|6C24A796B66CDA6D909508A16C74B406|/`
- Win10 1803
  - `ed2k://|file|cn_windows_10_consumer_editions_version_1803_updated_march_2018_x64_dvd_12063766.iso|4714162176|FB8C05DE594CD7E58D88993652DD2102|/`
  - `ed2k://|file|cn_windows_10_consumer_editions_version_1803_updated_march_2018_x86_dvd_12063452.iso|3480692736|0EC3C40EF13D772798209981F18B6A5D|/`
- Win10 1809
  - `ed2k://|file|cn_windows_10_consumer_edition_version_1809_updated_sept_2018_x64_dvd_f7b9c8a9.iso|5085956096|226AB51B290C3C0393A6A17096CB7497|/`
  - `ed2k://|file|cn_windows_10_consumer_edition_version_1809_updated_sept_2018_x86_dvd_8c32ac6a.iso|3709065216|645A85A963F007C58B67A4FB32DE0925|/`
- Win10 1903
  - `ed2k://|file|cn_windows_10_consumer_editions_version_1903_x64_dvd_8f05241d.iso|4905476096|F28FDC23DA34D55BA466BFD6E91DD311|/`
  - `ed2k://|file|cn_windows_10_consumer_editions_version_1903_x86_dvd_44b77216.iso|3557466112|926D3E6D2503D0E8CB4C8599C8DEC58F|/`
- Win10 1909
  - `ed2k://|file|cn_windows_10_consumer_editions_version_1909_x64_dvd_76365bf8.iso|5381154816|6A56DE112B164EC054D1104C53F8F10B|/`
  - `ed2k://|file|cn_windows_10_consumer_editions_version_1909_x86_dvd_08dd0d3c.iso|3859558400|40991568D016CCBAEE1E67CD38FAABE8|/`
- Win10 2004
  - `ed2k://|file|cn_windows_10_consumer_editions_version_2004_updated_sep_2020_x64_dvd_049d70ee.iso|5424910336|9100F2CD41FED19B3314FFCF182DF026|/`
  - `ed2k://|file|cn_windows_10_consumer_editions_version_2004_updated_sep_2020_x86_dvd_8a8fe8c0.iso|3893041152|B6C95CA453EE875C0C4A6F19125FC5D2|/`

## Windows 内核漏洞利用技术
### 内核利用基础知识
- Windows架构设计
  - 【Windows架构设计】
    - [中文博客](https://r00tk1ts.github.io/2017/12/19/Windows%E6%9E%B6%E6%9E%84%E8%AE%BE%E8%AE%A1/)
- Windows权限管理
  - 【浅析Windows的访问权限检查机制】
    - [中文博客](http://drops.xmd5.com/static/drops/tips-11803.html)
- Windows相关结构体
  - 【terminus】：很好的Windows结构搜索网页
    - [page link](http://terminus.rewolf.pl/terminus/)
  - 【深入研究 Windows PEB】
    - [English Blog](https://mohamed-fakroud.gitbook.io/t3nb3w/peb)
  - 【关键的windows内核数据结构一览(上)】
    - [中文博客](https://r00tk1ts.github.io/2018/01/08/%E5%85%B3%E9%94%AE%E7%9A%84Windows%E5%86%85%E6%A0%B8%E6%95%B0%E6%8D%AE%E7%BB%93%E6%9E%84%E4%B8%80%E8%A7%88%EF%BC%88%E4%B8%8A%EF%BC%89/)
  - 【关键的windows内核数据结构一览(下)】
    - [中文博客](https://r00tk1ts.github.io/2018/01/14/%E5%85%B3%E9%94%AE%E7%9A%84Windows%E5%86%85%E6%A0%B8%E6%95%B0%E6%8D%AE%E7%BB%93%E6%9E%84%E4%B8%80%E8%A7%88%EF%BC%88%E4%B8%8B%EF%BC%89/)
  - 【Catalog of key Windows kernel data structures】
    - [English Blog](https://codemachine.com/articles/kernel_structures.html)
  - 【Windows 对象】
    - [object categories](https://docs.microsoft.com/zh-cn/windows/win32/sysinfo/object-categories)
    - [user Object](https://docs.microsoft.com/zh-cn/windows/win32/sysinfo/user-objects)
    - [gdi Object](https://docs.microsoft.com/zh-cn/windows/win32/sysinfo/gdi-objects)
    - [kernel Object](https://docs.microsoft.com/zh-cn/windows/win32/sysinfo/kernel-objects?redirectedfrom=MSDN)
    - [Windows Object Header](https://codemachine.com/articles/object_headers.html)
    - [Windows Desktop Heap](https://docs.microsoft.com/zh-cn/archive/blogs/ntdebugging/desktop-heap-overview)

### 内核调试工具
- 【Windbg】：windows kernel调试工具
  - [download](https://docs.microsoft.com/zh-cn/windows-hardware/drivers/debugger/debugger-download-tools)
  - [getting-started-with-windows-debugging](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/getting-started-with-windows-debugging)
  - [Getting Started with WinDbg (User-Mode)](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/getting-started-with-windbg)
  - [Getting Started with WinDbg (Kernel-Mode)](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/getting-started-with-windbg--kernel-mode-)
  - [my-personal-cheat-sheet-for-using-windbg-for-kernel-debugging](https://laptrinhx.com/my-personal-cheat-sheet-for-using-windbg-for-kernel-debugging-1997973673/)
  - [Windbg加载用户层、内核层pdb文件](https://blog.csdn.net/forchoosen/article/details/107441660)
- 【Windbg Preview】：windows kernel调试工具(美观)
  - [download](https://www.microsoft.com/en-us/p/windbg-preview/)
  - [Debugging Using WinDbg Preview](https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/debugging-using-windbg-preview)
- 【dbgview】：windows调试工具，捕获调试信息，用于Guest
  - [download](https://docs.microsoft.com/en-us/sysinternals/downloads/debugview)
  - [Document help DebugView](https://documentation.help/DebugView/)
  - [Using DbgView To Capture Debug Traces From An Application](http://nutsaboutnets.com/faqs/dbgview/)
  - [Using DebugView to see debug output in real-time](https://tedgustaf.com/blog/2011/use-debugview-to-view-debug-output-from-asp-net-web-application/)
- 【OSRLoader】：驱动管理工具（安装，启动，暂停，卸载）
  - [download](https://www.osronline.com/article.cfm%5earticle=157.htm)
- 【VirtualKD】：双机调试工具，较老，不支持最新版VMWare
  - [download](https://sysprogs.com/legacy/virtualkd/)
- 【VirtualKD-Redux】：双机调试工具，支持最新版本VMWare
  - [download](https://github.com/4d61726b/VirtualKD-Redux)

### HEVD 内核利用教程
- 【HackSysExtremeVulnerableDriver】：windows内核利用技术学习项目
  - [download](https://github.com/hacksysteam/HackSysExtremeVulnerableDriver)
- 【HEVD StackOverflow】：
  - [HEVD内核漏洞之栈溢出](https://bbs.pediy.com/thread-252775.htm)
  - [HEVD栈溢出](https://50u1w4y.github.io/site/HEVD/stackoverflow/)
  - [Windows Kernel Exploitation Tutorial Part 2: Stack Overflow](https://rootkits.xyz/blog/2017/08/kernel-stack-overflow/)
- 【HEVD ArbitraryWrite】：
  - [HEVD内核漏洞之任意地址覆盖](https://bbs.pediy.com/thread-253848.htm)
  - [HEVD 任意地址覆盖](https://50u1w4y.github.io/site/HEVD/arbitraryWrite/)
  - [Windows Kernel Exploit 内核漏洞学习(3)-任意内存覆盖漏洞](https://bbs.pediy.com/thread-252506.htm)
  - [Windows Kernel Exploitation Tutorial Part 3: Arbitrary Memory Overwrite (Write-What-Where)](https://rootkits.xyz/blog/2017/09/kernel-write-what-where/)
- 【HEVD ArbitrayWrite BitMap】:
  - [bitmap 任意地址写漏洞利用](https://50u1w4y.github.io/site/HEVD/bitmap)
  - [Windows Kernel Exploit Part 5](https://paper.seebug.org/876/)
- 【HEVD BufferOverflow NonPagedPool】
  - [HEVD 非换页池溢出](https://50u1w4y.github.io/site/HEVD/nonPagedpooloverflow)
  - [HEVD内核漏洞学习(4)池溢出 ](https://bbs.pediy.com/thread-263097.htm)
  - [Windows Kernel Exploitation Tutorial Part 4: Pool Feng-Shui –> Pool Overflow](https://rootkits.xyz/blog/2017/11/kernel-pool-overflow/)
- 【Writeup综合】
  - [www漏洞从win7-win10](https://thunderjie.github.io/2019/08/19/www%E6%BC%8F%E6%B4%9E%E4%BB%8Ewin7-win10/)
  - [thunderjie 的 writeup](https://thunderjie.github.io/2019/06/28/Windows-Kernel-Exploit/)
  - [50u1w4y 的 writeup](https://50u1w4y.github.io/site/HEVD/homePage/)
  - [Saturn35 的 writeup](https://bbs.pediy.com/user-831334.htm)
  - [rootkit 的 writeup](https://rootkits.xyz/blog/)
  - [Thunder J 的 writeup](https://bbs.pediy.com/user-home-825245.htm)
  - [fuzzing security 的 writeup](https://www.fuzzysecurity.com/tutorials.html)
- 【Exp综合】
  - https://github.com/h0mbre/Windows-Exploits/tree/162dfd45d284556b47739835116a962177b243b0/Exploit-Code/HEVD
  - https://github.com/GradiusX/HEVD-Python-Solutions
  - https://github.com/dhn/OSEE/tree/master/Kernel_Exploitation/HEVD
  - https://github.com/ThunderJie/Windows-Kernel-Exploit

### token 权限滥用
- 【windows-privilege-abuse-auditing-detection-and-defense】：windows token利用
  - [English Blog](https://medium.com/palantir/windows-privilege-abuse-auditing-detection-and-defense-3078a403d74e)
- 【Abusing Token Privileges For EoP】：windows token权限滥用利用文章（含代码）
  - [Paper](https://github.com/hatRiot/token-priv/blob/master/abusing_token_eop_1.0.txt)
  - [Code](https://github.com/hatRiot/token-priv)
- 【windows-privileges】
  - [English pdf](https://speakerdeck.com/fr0gger/windows-privileges)
- 【NTLM-RELAY】
  - [English Blog](https://en.hackndo.com/ntlm-relay/)
- 【Priv2Admin：在 Windows 中利用漏洞提权】
  - [download](https://github.com/gtworek/Priv2Admin)
- 【The Rise of Potatoes Privilege Escalations in Windows Services】
  - [PDF](http://i.blackhat.com/asia-21/Thursday-Handouts/as21-Cocomazzi-The-Rise-of-Potatoes-Privilege-Escalations-in-Windows-Services.pdf)
- 【Potato家族本地提权细节】
  - [中文博客](https://xz.aliyun.com/t/7776)

### GDI 滥用提权

>  内核利用从任意地址写 转换为 任意地址读写

#### BitMap  RS1(v1607)前
- 【Windows GDI BitMap】
  - [中文博客](https://kernel32.org/posts/windows-gdi-bitmap/)
  - [English Blog](https://www.fuzzysecurity.com/tutorials/expDev/21.html)
- 【Bitmap轶事：Windows 10纪念版后的GDI对象泄露】
  - [中文博客](https://r00tk1ts.github.io/2018/03/21/Bitmaps%E8%BD%B6%E4%BA%8B%EF%BC%9AWindows%2010%E7%BA%AA%E5%BF%B5%E7%89%88%E5%89%8D%E7%9A%84GDI%E5%AF%B9%E8%B1%A1%E6%B3%84%E9%9C%B2/) 
  - [English Blog](https://labs.mwrinfosecurity.com/blog/a-tale-of-bitmaps/)
- 【Abusing GDI objects: Bitmap object’s size in the kernel pool】
  - [English Blog](http://theevilbit.blogspot.com/2017/10/abusing-gdi-objects-bitmap-objects-size.html)
- 【ring0层exp原语之滥用GDI】
  - [中文博客](https://r00tk1ts.github.io/2018/01/15/ring0%E5%B1%82exp%E5%8E%9F%E8%AF%AD%E4%B9%8B%E6%BB%A5%E7%94%A8GDI/)

#### Accelerator Table RS1(v1607)
- 【RS1 下 bitmap 的替代方法】
  - [中文博客](https://50u1w4y.github.io/site/HEVD/bitmapReplace_RS1/)
- 【Windows10 v1607内核提权技术的发展——利用AcceleratorTable】
  - [中文博客](https://www.anquanke.com/post/id/168356)

#### lpszMenuName RS2(v1703)
- 【Windows10 v1703基于桌面堆泄露的内核提权技术】
  - [中文博客](https://www.anquanke.com/post/id/168441)
- 【Part 18: Kernel Exploitation -> RS2 Bitmap Necromancy】
  - [English Blog](http://fuzzysecurity.com/tutorials/expDev/22.html)
  - [中文博客](https://bbs.pediy.com/thread-225296.htm)

#### Palette RS3 (v1709)
- 【Windows10 v1709特权提升：GDI Palette滥用】
  - [中文博客](https://www.anquanke.com/post/id/168572)

#### 综述
- 【GDI魔术:漏洞利用中的利器】
  - [中文pdf](http://www.vxjump.net/files/seccon/exp-in-gdi.pdf)
- 【Abusing GDI for ring0 exploit primitives:Reloaded】
  - [English pdf](https://www.coresecurity.com/sites/default/files/private-files/publications/2016/10/Abusing-GDI-Reloaded-ekoparty-2016_0.pdf)
- 【Abusing GDI for ring0 exploit primitives: Evolution】
  - [English Blog](https://labs.bluefrostsecurity.de/files/Abusing_GDI_for_ring0_exploit_primitives_Evolution_Slides.pdf)
- 【滥用GDI对象】
  - [中文博客](https://saturn35.com/2019/07/25/20190725-1/)
- 【www漏洞从win7-win10】
  - [中文博客](https://thunderjie.github.io/2019/08/19/www%E6%BC%8F%E6%B4%9E%E4%BB%8Ewin7-win10/)
- 【Taking-Windows-10-Kernel-Exploitation-To-The-Next-Level–Leveraging-Write-What-Where-Vulnerabilities-In-Creators-Update-wp】
  - [English pdf](https://www.blackhat.com/docs/us-17/wednesday/us-17-Schenk-Taking-Windows-10-Kernel-Exploitation-To-The-Next-Level%E2%80%93Leveraging-Write-What-Where-Vulnerabilities-In-Creators-Update-wp.pdf)
  - [中文 pdf](https://bbs.pediy.com/thread-227102.htm)

### 堆利用
- 【Windows内核池喷射的乐趣】
  - [中文博客](https://www.anquanke.com/post/id/86896)
  - [English Blog](https://theevilbit.blogspot.com/2017/09/pool-spraying-fun-part-1.html)
- 【Windows kernel pool spraying fun - Part 1 - Determine kernel object size】
  - [English Blog](https://theevilbit.blogspot.com/2017/09/pool-spraying-fun-part-1.html)
- 【Windows kernel pool spraying fun - Part 2 - More objects】
  - [English Blog](https://theevilbit.blogspot.com/2017/09/windows-kernel-pool-spraying-fun-part-2.html)
- 【Windows kernel pool spraying fun - Part 3 - Let's make holes】
  - [English Blog](https://theevilbit.blogspot.com/2017/09/windows-kernel-pool-spraying-fun-part-3.html)
- 【Windows kernel pool spraying fun - Part 4 - object & pool headers, kex & putting it all together】
  - [English Blog](https://theevilbit.blogspot.com/2017/09/windows-kernel-pool-spraying-fun-part-4.html)
- 【Kernel Pool Exploitation on Windows 7】
  - [English paper](https://www.exploit-db.com/docs/english/16032-kernel-pool-exploitation-on-windows-7.pdf)

### 保护绕过
- 【SMEP和SMAP绕过】
  - [中文博客](https://bbs.pediy.com/thread-261744.htm)
- 【Windows 10 x64上令牌窃取有效载荷问题，并绕过SMEP 上】
  - [中文博客](https://www.4hou.com/posts/21y1)
- 【Windows 10 x64上令牌窃取有效载荷问题，并绕过SMEP 下】
  - [中文博客](https://www.4hou.com/posts/4YAV)
- 【Windows SMEP Bypass U=S】
  - [English pdf](https://www.coresecurity.com/sites/default/files/2020-06/Windows%20SMEP%20bypass%20U%20equals%20S_0.pdf)

### Payload
- 【Attack Detection Fundamentals 2021 Windows Lab #1：构建一个可以绕过最常见保护机制的原始 payload】
  - [English Blog](https://labs.f-secure.com/blog/attack-detection-fundamentals-2021-windows-lab-1/)
- 【Attack Detection Fundamentals 2021 Windows Lab #2 ：引入其它绕过防御的技术优化 payload】
  - [English Blog](https://labs.f-secure.com/blog/attack-detection-fundamentals-2021-windows-lab-2/)
- 【Attack Detection Fundamentals 2021 Windows Lab #3：借助 API HOOK 针对使用远程桌面连接的用户劫持纯文本凭据】
  - [English Blog](https://labs.f-secure.com/blog/attack-detection-fundamentals-2021-windows-lab-3/)
- 【Attack Detection Fundamentals 2021 Windows Lab #4：窃取目标用户的 Chrome 浏览器中的 cookie，并探索如何检测这类可疑的劫持行为】
  - [English Blog](https://labs.f-secure.com/blog/attack-detection-fundamentals-2021-windows-lab-4/)

### 综述
- 【猫鼠游戏：Windows内核提权样本狩猎思路分享】
  - [中文博客](https://www.anquanke.com/post/id/235716)
- 【Windows Kernel Address Leaks】
  - [Code](https://github.com/sam-b/windows_kernel_address_leaks)
- 【通过内核地址保护措施，回顾Windows安全加固技术】
  - [中文博客](https://www.anquanke.com/post/id/85614)
- 【Windows Security Hardening Through Kernel Address Protection】
  - [English pdf](https://j00ru.vexillium.org/papers/2011/address_protection.pdf)
- 【关于内核漏洞的原理分析】
  - [中文博客](https://www.yuque.com/posec/public/sp9bs1)
- 【Level Up! Practical Windows Privilege Escalation - Andrew Smith】
  - [Youtube](https://www.youtube.com/watch?v=PC_iMqiuIRQ)
- 【I Got 99 Problem But a Kernel Pointer Ain’t One】
  - [English pdf](https://recon.cx/2013/slides/Recon2013-Alex%20Ionescu-I%20got%2099%20problems%20but%20a%20kernel%20pointer%20ain't%20one.pdf)
- 【The Life And Death of Kernel Object Abuse】
  - [English pdf](https://conference.hitb.org/hitbsecconf2018ams/materials/D1%20COMMSEC%20-%20Saif%20Elsherei%20and%20Ian%20Kronquist%20-%20The%20Life%20&%20Death%20of%20Kernel%20Object%20Abuse.pdf)
- 【A Window into Ring0】
  - [English pdf](https://labs.f-secure.com/assets/BlogFiles/mwri-steelcon-2017-samdb-a-window-into-ring0.pdf)
- 【Easy local Windows Kernel exploitation】
  - [English pdf](https://paper.bobylive.com/Meeting_Papers/BlackHat/USA-2012/BH_US_12_Cerrudo_Windows_Kernel_WP.pdf)
- 【20-Han-Discovery-20-Yeas-Old-Vulnerabilities-In-Modern-Windows-Kernel】
  - [English pdf](https://github.com/singularseclab/Slides/blob/main/2020/eu-20-Han-Discovery-20-Yeas-Old-Vulnerabilities-In-Modern-Windows-Kernel.pdf)
- 【内核漏洞攻防】
  - [中文博客](https://zhuanlan.zhihu.com/p/364188890)
- 【基于用户模式回调函数的内核漏洞分析、利用与防范】
  - [中文博客](https://translation-zh-cn.readthedocs.io/zh_CN/latest/)

## Windows 服务漏洞
### 任意文件移动/dll劫持
- 【An introduction to privileged file operation abuse on Windows】
  - [English Blog](https://offsec.almond.consulting/intro-to-file-operation-abuse-on-Windows.html)
  - [中文博客](https://www.freebuf.com/vuls/242472.html)
- 【Windows Exploitation Tricks: Exploiting Arbitrary File Writes for Local Elevation of Privilege】
  - [English Blog](https://googleprojectzero.blogspot.com/2018/04/windows-exploitation-tricks-exploiting.html)
- 【symboliclink-testing-tools】
  - [download](https://github.com/googleprojectzero/symboliclink-testing-tools)
- 【NtApiDotNet】
  - [download](https://github.com/googleprojectzero/sandbox-attacksurface-analysis-tools/tree/master/NtApiDotNet)
- 【Diving in to Spooler: Discovering LPE and RCE Vulnerabilities in Windows Printer】
  - [Topic](https://www.blackhat.com/us-21/briefings/schedule/index.html?fbclid=IwAR3TWHTC1UXsa54x9VcdpG82Jdgd0QWgFYgAc5LWqUNxd6CWR6Hp9Dcpvqs#diving-in-to-spooler-discovering-lpe-and-rce-vulnerabilities-in-windows-printer-23315)
- 【Exploiting Windows COM/WinRT Services】
  - [Topic](https://www.blackhat.com/us-21/briefings/schedule/#exploiting-windows-comwinrt-services-23653)

### 分析工具
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

## Windows 漏洞分析

### Windows 补丁分析
- https://msrc.microsoft.com/update-guide：官方KB对应补丁信息
- https://bugs.hacking8.com/tiquan：根据KB补丁号或者systeminfo查找对应的exp
- 【Extracting and Diffing Windows Patches in 2020】： 通过Windows更新提取和分析补丁（含代码）
  -  [English Blog](https://wumb0.in/extracting-and-diffing-ms-patches-in-2020.html)
  -  [PatchExtract.ps1](https://gist.github.com/wumb0/306f97dc8376c6f53b9f9865f60b4fb5#file-patchextract-ps1)
  -  [delta_patch.py](https://gist.github.com/wumb0/9542469e3915953f7ae02d63998d2553#file-delta_patch-py)
- 【Bindiff】：二进制差异分析工具
  - [download](https://www.zynamics.com/bindiff.html)

### Windows 漏洞集合
- https://github.com/SecWiki/windows-kernel-exploits
- https://github.com/nu11secur1ty/Windows10Exploits
- https://github.com/abatchy17/WindowsExploits
- https://github.com/Ascotbe/Kernelhub
- https://github.com/WindowsExploits/Exploits
- https://github.com/Heptagrams/Heptagram/tree/master/Windows/Elevation
- https://github.com/Al1ex/WindowsElevation
- https://github.com/nomi-sec/PoC-in-GitHub

### CVE漏洞分析

#### CVE-2020-1054 堆越界读写
- https://www.anquanke.com/post/id/209329
- https://0xeb-bp.com/blog/2020/06/15/cve-2020-1054-analysis.html
- https://bbs.pediy.com/thread-260884.htm

#### CVE-2020-0796 SMB Ghost 整数溢出漏洞
**影响版本**：v1903、v1909
- **Analyse**
  - https://jcxp.github.io/2020/03/31/CVE-2020-0796-SMB%E6%BC%8F%E6%B4%9E%E5%88%86%E6%9E%90/
  - https://paper.seebug.org/1168/
  - https://blog.ycdxsb.cn/6ba048bc.html
- **Exp**: v1903/v1909成功
  -  https://github.com/danigargu/CVE-2020-0796/blob/master/cve-2020-0796-local/exploit.cpp

#### CVE-2020-0787 BITS任意文件移动漏洞
- https://docs.microsoft.com/en-us/windows/win32/bits/background-intelligent-transfer-service-portal
- https://xz.aliyun.com/t/7935
- https://itm4n.github.io/cve-2020-0787-windows-bits-eop/
- https://github.com/itm4n/BitsArbitraryFileMove
- https://github.com/cbwang505/CVE-2020-0787-EXP-ALL-WINDOWS-VERSION
- https://packetstormsecurity.com/files/158056/Background-Intelligent-Transfer-Service-Privilege-Escalation.html
- https://blog.ycdxsb.cn/57177eae.html

#### MS16-098 堆越界写
- http://repwn.com/archives/26/
- https://sensepost.com/blog/2017/exploiting-ms16-098-rgnobj-integer-overflow-on-windows-8.1-x64-bit-by-abusing-gdi-objects/
- https://xz.aliyun.com/t/2919
- https://security.tencent.com/index.php/blog/msg/117
- https://www.anquanke.com/post/id/85302

#### MS15-010 UAF
- https://paper.seebug.org/1439/
- https://paper.seebug.org/873/
- https://xz.aliyun.com/t/4549
- https://xz.aliyun.com/t/8984
- https://0x3f97.github.io/exploit/2018/11/09/windows-kernel-exploit-uaf-cve-2015-0057/
- https://www.blackhat.com/docs/asia-16/materials/asia-16-Wang-A-New-CVE-2015-0057-Exploit-Technology-wp.pdf
- https://research.nccgroup.com/wp-content/uploads/2020/12/Exploiting-CVE-2015.pdf
- https://github.com/0x3f97/windows-kernel-exploit/blob/master/cve-2015-0057/poc/main.cpp

### Windows 分析工具
- 【drmemory】
  - [download](https://github.com/DynamoRIO/drmemory)

## Windows 渗透测试

### 攻击面分析
- 【揭秘 Windows 减少攻击面（ASR：attack surface reduction）的细节】
  - [English Blog](https://github.com/commial/experiments/tree/master/windows-defender/ASR)
### 渗透测试工具
- 【Sysmon】
  - [download](https://docs.microsoft.com/en-us/sysinternals/downloads/sysmon)
  - [使用Sysmon工具分析已知的DLL劫持和命名管道令牌模拟攻击测试](https://labs.jumpsec.com/detecting-known-dll-hijacking-and-named-pipe-token-impersonation-attacks-with-sysmon/)
- 【PrivescCheck】：Windows 提权攻击面分析工具，来自itm4n
  - [download](https://github.com/itm4n/PrivescCheck)
- 【WADComs】：一个CheatSheet工具，包含精选的攻击性安全工具及其各自的命令列表
  - [download](https://github.com/WADComs/WADComs.github.io)
- 【openark】：一款Windows平台上的开源Ark工具. Ark是Anti-Rootkit（对抗恶意程序）的简写, OpenArk目标成为逆向工程师、编程人员的工具，同时也能为那些希望清理恶意软件的用户服务
  - [download](https://github.com/BlackINT3/OpenArk)
- 【FourEye】：exe、shellcode免杀
  - [download](https://github.com/lengjibo/FourEye)
- 【nishang】
  - [download](https://github.com/samratashok/nishang)

### 本地提权工具
- 【Metasploit Windows最全的漏洞利用列表】
  - [English Blog](https://www.infosecmatter.com/list-of-metasploit-windows-exploits-detailed-spreadsheet/)
- 【Perfusion】：利用RpcEptMapper注册表项权限漏洞（Windows 7 / 2088R2 / 8/2012）
  - [download](https://github.com/itm4n/Perfusion)

### 渗透测试常用漏洞
#### MS17-010 永恒之蓝
- http://oddboy.cn/2017/ms17-010-python%E8%84%9A%E6%9C%ACexploit/
- https://blackwolfsec.cc/2017/05/12/Eternalblue_ms17-010/
- https://github.com/SEC-GO/Red-vs-Blue/blob/master/%E6%B0%B8%E6%81%92%E4%B9%8B%E8%93%9Dms17-010%E7%9A%84%E5%88%A9%E7%94%A8.md
- https://blog.ycdxsb.cn/24e83041.html

### 综述
- 【Windows 提权总结】
  - [中文博客](https://www.cnblogs.com/-mo-/p/12718115.html) 
- 【Windows渗透基础大全】
  - [中文博客](https://www.anquanke.com/post/id/236522)

## Paper
- 【Bugs on the Windshield: Fuzzing the Windows Kernel】：Windows kernel fuzz
  - [English Blog](https://research.checkpoint.com/2020/bugs-on-the-windshield-fuzzing-the-windows-kernel/)
  - [Paper](https://github.com/yoava333/presentations/blob/master/Fuzzing%20the%20Windows%20Kernel%20-%20OffensiveCon%202020.pdf)
- 【NTFUZZ: Enabling Type-Aware Kernel Fuzzing on Windows with Static Binary Analysis(S& P 2021)】：Windows kernel Fuzz
  - [Paper](https://softsec.kaist.ac.kr/~jschoi/data/oakland2021.pdf)
- 【Meltdown: Reading Kernel Memory from User Space】
  - [Paper](https://www.usenix.org/system/files/conference/usenixsecurity18/sec18-lipp.pdf)
- 【Different is Good: Detecting the Use of Uninitialized Variables through Differential Replay(CCS 2019)】
  - [Paper](http://malgenomeproject.org/papers/ccs19_timeplayer.pdf)

## Fuzz
- 【NtCall64】：一个windows 系统调用Fuzz工具
  - [download](https://github.com/hfiref0x/NtCall64)
- 【NTFuzz】：基于类型推断的windows系统调用Fuzz
  - [Paper](https://softsec.kaist.ac.kr/~jschoi/data/oakland2021.pdf)
- 【IOCTLFuzzer】：通过IOCTL 接口Fuzz驱动的工具
  - [download](https://github.com/Cr4sh/ioctlfuzzer)
- 【IOCTLBF】：通过IOCTL 接口Fuzz驱动的工具
  - [download](https://github.com/koutto/ioctlbf)
- 【BrokenType】：Fuzz windows 字体
  - [download](https://github.com/googleprojectzero/BrokenType)

## Misc
- 【关于深入理解 Windows 的一些逆向代码笔记】
  - [download](https://github.com/vxcute/WindowsReversed)
- 【利用 Windows Defender ASR 规则的漏洞执行 Shellcode】
  - [Github](https://github.com/optiv/Dent)

## 综合性资源
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
- http://www.fuzzysecurity.com
- https://021w.github.io/