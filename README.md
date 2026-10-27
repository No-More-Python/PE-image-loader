# PE Image Loader

An educational x64 PE loader written in C. It explores parts of the Windows PE loading process and is not intended to replace the Windows loader.

## Features

- PE header parsing
- Section mapping
- Base relocations
- Import resolution using `LoadLibraryA` and `GetProcAddress`
- Section memory protections
- TLS callback invocation

## Architecture Support

**x64 (PE32+) only.** x86 (PE32) files are not supported.

## Tested On

- Windows 11
- GCC x64 (MinGW-w64)

## Build

```powershell
gcc PeLoader.c -o PeLoader.exe
```

## Usage

```powershell
.\PeLoader.exe .\TestFile\hello64.exe
```

## Limitations

- C++ exception handling (try / catch), including nested exceptions and stack unwinding.

- Windows Structured Exception Handling (SEH), using __try / __except.
