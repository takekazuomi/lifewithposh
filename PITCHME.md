# Life with posh

- How did I get to live in posh?
- Posh as an interactive shell.

Created by <a target="_blank" href="http://github.com/takekazuomi">takekazuomi</a> / <a target="_blank" href="http://twitter.com/takekazuomi">@takekazuomi</a>

---

## Who am I?

Takekazu Omi

Developer @kyrt, inc. (own company)

Microsoft MVP for Azure.

---

## About 7 years ago. 
(in 2010)

I switched from cygwin to PowerShell (posh). 

I changed my mind.

Real Programmers DON'T USE cygwin.


(#｀Д´)ﾉﾉ┻┻;:'､･ﾞ

---

## Why not cygwin.

- broken fork
- peer performance
- native exe compatibility

and more 

---

## Why not Bash On Windows?
(WSL)

At that time, it was not there.

orz....

---

## A hard life began

Posh is too bad for interactive shell comparison to bash.

- No emacs-like key bindings.
- Too much poor completion.
- Long command name
- Broken alias. Example: curl, diff

---
## and more
## PATH HELL

- Many many applications append own path into PATH environment.

The Problem is not caused by Posh, it's by Windows. 

However it is critical for console favorite people.

I call this "PATH Hell". It is something like [DLL Hell](https://en.wikipedia.org/wiki/DLL_Hell)

---

### For seven years, I has been survive. Because ... 

- PSReadLine
- psenv
- remove-alias -force
- ConEmu
- cd bookmark (homemade)
- ps envdir (homemade)

---

### <a target="_blank" href="https://github.com/lzybkr/PSReadLine">PSReadLine</a>

A bash inspired readline implementation for PowerShell.

```
Set-PSReadlineOption -EditMode Emacs
```

Extreamly superb cmdlet. I have no life without this. Something like beer. 🍻

Now PowerShell 5.0 bundle PSReadLine. Good Job!

---

## <a target="_blank" href="https://github.com/DuFace">PsEnv</a>

Environment variables management cmdlet. For avoid conflict.

For ex. In my default console dosen't include any VisualStudio PATH. After start posh, execute following command for set VS environment.

```
use vs140
```

When I want vs 2017.

```
use vs150
```

---

## <a target="_blank" href="https://github.com/DuFace">PsEnv</a> + Tab completion

I made PR for Tab completion in Feb. 

```
use vs<tab>
vs110  vs120  vs140  vs150  vs90

```

In this case, I use posh <a target="_blank" href="https://msdn.microsoft.com/en-us/powershell/scripting/core-powershell/console/using-tab-expansion">TabExpansion</a>.
TabExpansion is powerfull. 🍣

---

## remove-alias -force

Just remove broken alias in Microsoft.PowerShell_profile.ps1. 

```
Remove-Item -Path alias:curl -ErrorAction SilentlyContinue -Force
Remove-Item -Path alias:diff -ErrorAction SilentlyContinue -Force
```

Make my life happy. 😆😆😆😆

---

## <a target="_blank" href="https://conemu.github.io/">ConEmu</a>

Windows console emulator with tabs. 

I use evryday. I love it. <3 <3 <3

---

## <a target="_blank" href="https://github.com/takekazuomi/cdbookmark/">cd bookmark</a>

I made directory bookmark cmdlet to save my time. 

Easy to install from <a target="_blank" href="https://www.powershellgallery.com/packages/posh-cdbookmark/0.0.5">PowerShell Gallery</a>

```
Install-Module cdbookmark
```

bookmark directory.

```
add-cdbookmark -name foo -value c:\home\foo
```

change bookmarked directory. cdb is alias of set-cdbookmark

```
cdb foo
```

---

## [posh direnv](https://github.com/takekazuomi/posh-direnv)

I made environment switcher for the PowerShell. It's add environment variable which depend on directory.

Easy to install from PowerShell Gallery [posh-direnv](https://www.powershellgallery.com/packages/posh-direnv/0.0.2)

```
cd demo
Edit-DirEnvRc
```

Start new posh session and cd demo then execute ".psenvrc"

---

# End

World is not so easy to live. However we can change by code.
Let's OSS and PR.
