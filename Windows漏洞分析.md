# Windows 漏洞分析

## Windows 补丁分析

- https://msrc.microsoft.com/update-guide：官方KB对应补丁信息
- https://bugs.hacking8.com/tiquan：根据KB补丁号或者systeminfo查找对应的exp
- 【Extracting and Diffing Windows Patches in 2020】： 通过Windows更新提取和分析补丁（含代码）
  -  [English Blog](https://wumb0.in/extracting-and-diffing-ms-patches-in-2020.html)
  -  [PatchExtract.ps1](https://gist.github.com/wumb0/306f97dc8376c6f53b9f9865f60b4fb5#file-patchextract-ps1)
  -  [delta_patch.py](https://gist.github.com/wumb0/9542469e3915953f7ae02d63998d2553#file-delta_patch-py)
- 【Bindiff】：二进制差异分析工具
  - [download](https://www.zynamics.com/bindiff.html)
- 【winbindex】: 用于获取windows 二进制文件的网站
  - [download](https://github.com/m417z/winbindex)

## Windows 漏洞集合

- https://github.com/ycdxsb/WindowsPrivilegeEscalation

- https://github.com/SecWiki/windows-kernel-exploits
- https://github.com/nu11secur1ty/Windows10Exploits
- https://github.com/abatchy17/WindowsExploits
- https://github.com/Ascotbe/Kernelhub
- https://github.com/WindowsExploits/Exploits
- https://github.com/Heptagrams/Heptagram/tree/master/Windows/Elevation
- https://github.com/Al1ex/WindowsElevation
- https://github.com/nomi-sec/PoC-in-GitHub

## CVE漏洞分析

### CVE-2020-1054 堆越界读写

- https://www.anquanke.com/post/id/209329
- https://0xeb-bp.com/blog/2020/06/15/cve-2020-1054-analysis.html
- https://bbs.pediy.com/thread-260884.htm

### CVE-2020-0796 SMB Ghost 整数溢出漏洞

**影响版本**：v1903、v1909

- **Analyse**
  - https://jcxp.github.io/2020/03/31/CVE-2020-0796-SMB%E6%BC%8F%E6%B4%9E%E5%88%86%E6%9E%90/
  - https://paper.seebug.org/1168/
  - https://blog.ycdxsb.cn/6ba048bc.html
- **Exp**: v1903/v1909成功
  -  https://github.com/danigargu/CVE-2020-0796/blob/master/cve-2020-0796-local/exploit.cpp

### CVE-2020-0787 BITS任意文件移动漏洞

- https://docs.microsoft.com/en-us/windows/win32/bits/background-intelligent-transfer-service-portal
- https://xz.aliyun.com/t/7935
- https://itm4n.github.io/cve-2020-0787-windows-bits-eop/
- https://github.com/itm4n/BitsArbitraryFileMove
- https://github.com/cbwang505/CVE-2020-0787-EXP-ALL-WINDOWS-VERSION
- https://packetstormsecurity.com/files/158056/Background-Intelligent-Transfer-Service-Privilege-Escalation.html
- https://blog.ycdxsb.cn/57177eae.html

### MS16-098 堆越界写

- http://repwn.com/archives/26/
- https://sensepost.com/blog/2017/exploiting-ms16-098-rgnobj-integer-overflow-on-windows-8.1-x64-bit-by-abusing-gdi-objects/
- https://xz.aliyun.com/t/2919
- https://security.tencent.com/index.php/blog/msg/117
- https://www.anquanke.com/post/id/85302

### MS15-010 UAF

- https://paper.seebug.org/1439/
- https://paper.seebug.org/873/
- https://xz.aliyun.com/t/4549
- https://xz.aliyun.com/t/8984
- https://0x3f97.github.io/exploit/2018/11/09/windows-kernel-exploit-uaf-cve-2015-0057/
- https://www.blackhat.com/docs/asia-16/materials/asia-16-Wang-A-New-CVE-2015-0057-Exploit-Technology-wp.pdf
- https://research.nccgroup.com/wp-content/uploads/2020/12/Exploiting-CVE-2015.pdf
- https://github.com/0x3f97/windows-kernel-exploit/blob/master/cve-2015-0057/poc/main.cpp