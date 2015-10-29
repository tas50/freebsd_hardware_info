# freebsd_hardware_info
I'm currently working on improving the CPU detection support for FreeBSD users in Chef. Chef's hardware detection tool Ohai parses the output of /var/run/dmesg.boot to determine CPU information like vendor, family ID, and stepping.  In order to make sure we have the regex right for parsing that data I'd love to get more examples.

You can help by creating a PR with the output of the CPU section of your dmesg.boot log.  Here's an example from my laptop:

```
CPU: Intel(R) Core(TM) i7-4980HQ CPU @ 2.80GHz (2793.59-MHz K8-class CPU)
  Origin="GenuineIntel"  Id=0x40661  Family=0x6  Model=0x46  Stepping=1
  Features=0x783fbff<FPU,VME,DE,PSE,TSC,MSR,PAE,MCE,CX8,APIC,SEP,MTRR,PGE,MCA,CMOV,PAT,PSE36,MMX,FXSR,SSE,SSE2>
  Features2=0x5ed8220b<SSE3,PCLMULQDQ,MON,SSSE3,CX16,SSE4.1,SSE4.2,MOVBE,POPCNT,AESNI,XSAVE,OSXSAVE,AVX,RDRAND>
  AMD Features=0x28100800<SYSCALL,NX,RDTSCP,LM>
  AMD Features2=0x21<LAHF,ABM>
  Structured Extended Features=0x2000<NFPUSG>
  TSC: P-state invariant
```

Thanks,
Tim
