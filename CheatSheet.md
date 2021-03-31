# CheatSheet

## CMD

- 查看系统信息和补丁信息：
  - `systeminfo`
  - `wmic qfe list full`
  - 输出html格式：`wmic qfe list full /format:htable >C:\Temp\hotfixes.htm `



## WinDbg (Preview)

- 修改寄存器：r @eax=1

- 去除无效输出

  ```
  ed nt!Kd_SXS_Mask 0
  ed nt!Kd_FUSION_Mask 0
  ```

  



