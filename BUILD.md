## 🏗️ Visual Studio Build System

Visual Studio 2022 com suporte completo para:
- Windows Driver Kit (WDK)
- Kernel-Mode Driver Framework (KMDF)
- .NET 8 SDK

### Projetos

1. **KernelSecDriver** (C/C++)
   - Type: Kernel-Mode Driver (KMDF)
   - Platform: x64
   - Output: `KernelSecDriver.sys`

2. **KernelSecService** (C#)
   - Type: Windows Service (.NET 8)
   - Platform: AnyCPU (x64 preferred)
   - Output: `KernelSecService.exe`

### Build

```powershell
# Abrir solução
start WindowsKernelSecurityMonitor.sln

# Ou via MSBuild
msbuild WindowsKernelSecurityMonitor.sln /p:Configuration=Debug /p:Platform=x64
```

### Output

```
build/
├── Debug/
│   └── x64/
│       ├── KernelSecDriver.sys
│       ├── service/
│       │   └── KernelSecService.exe
└── Release/
    └── x64/
        ├── KernelSecDriver.sys
        └── service/
            └── KernelSecService.exe
```
