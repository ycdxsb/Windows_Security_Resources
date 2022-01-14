# Windows内核漏洞利用技术

## 内核利用基础知识

- Windows架构设计
  - 【Windows架构设计】
    - [中文博客](https://r00tk1ts.github.io/2017/12/19/Windows%E6%9E%B6%E6%9E%84%E8%AE%BE%E8%AE%A1/)
- Windows权限管理
  - 【浅析Windows的访问权限检查机制】
    - [中文博客](http://drops.xmd5.com/static/drops/tips-11803.html)
- Windows相关结构
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
  - 【Peb结构及利用】
    - [English Blog](https://malwareandstuff.com/peb-where-magic-is-stored/)
  - 【xntsv】：一款展示windows数据结构的工具
    - [download](https://github.com/horsicq/xntsv)

## 内核调试工具

- 【pdbparse】:windows pdb解析工具
  - [download](https://github.com/moyix/pdbparse)
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
- 【HyperDbg】：一款开源调试器，利用 Hypervisor 特性，支持用户态和内核态调试，主要为逆向分析、调试、Fuzz 设计使用
  - [download](https://github.com/HyperDbg/HyperDbg)

## HEVD 内核利用教程

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

## Token 权限滥用

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
- 【Potato家族提权分析】
  - [中文博客](https://www.geekby.site/2020/08/potato%E5%AE%B6%E6%97%8F%E6%8F%90%E6%9D%83%E5%88%86%E6%9E%90/)
- 【Potato家族本地提权细节】
  - [中文博客](https://xz.aliyun.com/t/7776)
- 【Potato家族本地提权】
  - [中文博客](http://iv4n.cc/potato-family-local-priv-elevate/)
- 【NamedPipePTH】
  - [download](https://github.com/S3cur3Th1sSh1t/NamedPipePTH)
- 【SharpImpersonation】
  - [English Blog](https://s3cur3th1ssh1t.github.io/SharpImpersonation-Introduction/)
  - [download](https://github.com/S3cur3Th1sSh1t/SharpImpersonation)
- 【lowbox token permissive learning mode】：James Forshaw 对 Windows LowBox Token Permissive Learning Mode 的分析
  - [English Blog](https://www.tiraniddo.dev/2021/09/lowbox-token-permissive-learning-mode.html)

## GDI 滥用提权

>  内核利用从任意地址写 转换为 任意地址读写

### BitMap  RS1(v1607)前

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

### Accelerator Table RS1(v1607)

- 【RS1 下 bitmap 的替代方法】
  - [中文博客](https://50u1w4y.github.io/site/HEVD/bitmapReplace_RS1/)
- 【Windows10 v1607内核提权技术的发展——利用AcceleratorTable】
  - [中文博客](https://www.anquanke.com/post/id/168356)

### lpszMenuName RS2(v1703)

- 【Windows10 v1703基于桌面堆泄露的内核提权技术】
  - [中文博客](https://www.anquanke.com/post/id/168441)
- 【Part 18: Kernel Exploitation -> RS2 Bitmap Necromancy】
  - [English Blog](http://fuzzysecurity.com/tutorials/expDev/22.html)
  - [中文博客](https://bbs.pediy.com/thread-225296.htm)

### Palette RS3 (v1709)

- 【Windows10 v1709特权提升：GDI Palette滥用】
  - [中文博客](https://www.anquanke.com/post/id/168572)

### 综述

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

## 堆利用

- 【Windows内核池喷射的乐趣】
  - [中文博客](https://www.anquanke.com/post/id/86896)
  - [English Blog](https://theevilbit.blogspot.com/2017/09/pool-spraying-fun-part-1.html)
- 【Windows kernel pool spraying fun】
  - [ Part 1 - Determine kernel object size](https://theevilbit.blogspot.com/2017/09/pool-spraying-fun-part-1.html)
  - [Part 2 - More objects](https://theevilbit.blogspot.com/2017/09/windows-kernel-pool-spraying-fun-part-2.html)
  - [Part 3 - Let's make holes](https://theevilbit.blogspot.com/2017/09/windows-kernel-pool-spraying-fun-part-3.html)
  - [Part 4 - object & pool headers, kex & putting it all together](https://theevilbit.blogspot.com/2017/09/windows-kernel-pool-spraying-fun-part-4.html)
- 【Kernel Pool Exploitation on Windows 7】
  - [English paper](https://www.exploit-db.com/docs/english/16032-kernel-pool-exploitation-on-windows-7.pdf) 
- 【PoolViewer】：查看和转储 Win10RS5+ 转储文件的池
  - [download](https://github.com/yardenshafir/PoolViewer)
- 【Windows Pool OverFlow漏洞利用】
  - [中文博客](https://vul.360.net/archives/83)
- 【Windows-Non-Paged-Pool-Overflow-Exploitation】
  - [English Blog](https://github.com/vp777/Windows-Non-Paged-Pool-Overflow-Exploitation)
- 【SSTIC2020-Article-pool_overflow_exploitation_since_windows_10_19h1-bayet_fariello】：Windows 10 版本内核堆管理的细节以及 Heap Overflow 漏洞的利用
  - [pdf](https://www.sstic.org/media/SSTIC2020/SSTIC-actes/pool_overflow_exploitation_since_windows_10_19h1/SSTIC2020-Article-pool_overflow_exploitation_since_windows_10_19h1-bayet_fariello.pdf)

## 保护和绕过

- 【Windows Mitigation】
  - [Github](https://github.com/nccgroup/exploit_mitigations/blob/master/windows_mitigations.md)
- 【SMEP和SMAP绕过】
  - [中文博客](https://bbs.pediy.com/thread-261744.htm)
- 【Windows 10 x64上令牌窃取有效载荷问题，并绕过SMEP 上】
  - [中文博客](https://www.4hou.com/posts/21y1)
- 【Windows 10 x64上令牌窃取有效载荷问题，并绕过SMEP 下】
  - [中文博客](https://www.4hou.com/posts/4YAV)
- 【Windows SMEP Bypass U=S】
  - [English pdf](https://www.coresecurity.com/sites/default/files/2020-06/Windows%20SMEP%20bypass%20U%20equals%20S_0.pdf)
- 【RestrictedKernelLeaks】：可以实现 Windows 10 KASLR Bypass 的 API 列表
  - [Github](https://github.com/waleedassar/RestrictedKernelLeaks)
- 【KCon 2021:剑走偏锋-蓝军实战缓解措施】
  - [中文pdf](https://github.com/knownsec/KCon/blob/master/2021/%E5%89%91%E8%B5%B0%E5%81%8F%E9%94%8B-%E8%93%9D%E5%86%9B%E5%AE%9E%E6%88%98%E7%BC%93%E8%A7%A3%E6%8E%AA%E6%96%BD.pdf)

## Payload

- 【Attack Detection Fundamentals 2021 Windows Lab #1：构建一个可以绕过最常见保护机制的原始 payload】
  - [English Blog](https://labs.f-secure.com/blog/attack-detection-fundamentals-2021-windows-lab-1/)
- 【Attack Detection Fundamentals 2021 Windows Lab #2 ：引入其它绕过防御的技术优化 payload】
  - [English Blog](https://labs.f-secure.com/blog/attack-detection-fundamentals-2021-windows-lab-2/)
- 【Attack Detection Fundamentals 2021 Windows Lab #3：借助 API HOOK 针对使用远程桌面连接的用户劫持纯文本凭据】
  - [English Blog](https://labs.f-secure.com/blog/attack-detection-fundamentals-2021-windows-lab-3/)
- 【Attack Detection Fundamentals 2021 Windows Lab #4：窃取目标用户的 Chrome 浏览器中的 cookie，并探索如何检测这类可疑的劫持行为】
  - [English Blog](https://labs.f-secure.com/blog/attack-detection-fundamentals-2021-windows-lab-4/)

## 综述

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

## 
