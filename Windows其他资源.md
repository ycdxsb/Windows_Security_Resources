# Windows其他资源

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
- 【Static Detection of File Access Control Vulnerabilities on Windows System】

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
- 【Windows-API-Fuzzer】
  - [download](https://github.com/jackullrich/Windows-API-Fuzzer)
- 【KernelFuzzer】
  - [download](https://github.com/FSecureLABS/KernelFuzzer)
- 【kDriverFuzzer】
  - [中文博客](https://paper.seebug.org/523/)
  - [download](https://github.com/k0keoyo/kDriver-Fuzzer)
- 【wtf】
  - [download](https://github.com/0vercl0k/wtf)
- 【对 Windows 的 RDP 客户端和服务器进行模糊测试】
  - [English Blog](https://www.cyberark.com/resources/threat-research-blog/fuzzing-rdp-holding-the-stick-at-both-ends)
- 【Fuzzing RDP: Holding the Stick at Both Ends】：利用 AFL Fuzz Windows RDP 协议
  - [English Blog](https://www.cyberark.com/resources/threat-research-blog/fuzzing-rdp-holding-the-stick-at-both-ends)
- 【kernel-fuzzer-for-xen-project】：基于 Xen 和 AFL 实现的内核 Fuzzer
  - [download](https://github.com/intel/kernel-fuzzer-for-xen-project)
- 【KCon 2021:一枚字体crash到fuzzing】
  - [中文pdf](https://github.com/knownsec/KCon/blob/master/2021/%E4%B8%80%E6%9E%9A%E5%AD%97%E4%BD%93crash%E5%88%B0fuzzing.pdf)

## Misc

- 【关于深入理解 Windows 的一些逆向代码笔记】
  - [download](https://github.com/vxcute/WindowsReversed)
- 【利用 Windows Defender ASR 规则的漏洞执行 Shellcode】
  - [Github](https://github.com/optiv/Dent)
- 【magnumdb】：可以用来搜索一些magic number
  - [index](https://www.magnumdb.com/)
- 【APT-Hunter】:利用ETW机制检测apt
  - [Github](https://github.com/ahmedkhlief/APT-Hunter)

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
- https://github.com/TCM-Course-Resources/Windows-Privilege-Escalation-Resources
- https://github.com/alphaSeclab/windows-security