# CheatSheet

## CMD

- 查看系统信息和补丁信息：
  - `systeminfo`
  - `wmic qfe list full`
  - 输出html格式：`wmic qfe list full /format:htable >C:\Temp\hotfixes.htm `



## WinDbg (Preview)

- 修改寄存器：r @eax=1

- 查看寄存器：r fs

- 查看内存：dd fs:[0x124]

- 查看pcr：!pcr

- 查看KTHREAD：dt _KTHREAD 83f8a380

- 查看KAPC_STATE：dt _KAPC_STATE

- 查看EPROCESS：dt _EPROCESS

- 查看EX_FAST_REF：dt _EX_FAST_REF

- 按进程名查找进程：! process 0 0 smess.exe

- 按pid查看进程：!process 4 0 

- 查看PsInitialSystemProcess：dd nt!PsInitialSystemProcess

- 查看teb：dt _teb

- 查看peb：dt _peb

- 去除无效输出

  ```
  ed nt!Kd_SXS_Mask 0
  ed nt!Kd_FUSION_Mask 0
  ```

- 列出模块：lm m HEVD

- 



