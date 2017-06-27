# Life with posh

How did I get to live in posh?

Created by <a target="_blank" href="http://github.com/takekazuomi">takekazuomi</a> / <a target="_blank" href="http://twitter.com/takekazuomi">@takekazuomi</a>

---

## About 7 years ago

I switched from cygwin to PowerShell(posh). I changed my mind.

Real Programmers Don't Use cygwin.


(#｀Д´)ﾉﾉ┻┻;:'､･ﾞ


---

## A hard life began

Posh is too bad for interactive shell compare to bash.

- No emacs like keybinding.
- Too much poor completion.
- Long command name
- Broken alias. Example: curl, diff

---

## And more

Following problem is not cause by Posh, cause by Windows. But critical for consoler.

- Many many application append own path into PATH environment.

---

### For ten years since then, I survived. Because ..

- PSReadLine
- psenv
- remove-alias -force
- ConEmu
- cd bookmark

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

For ex. In my default console don't include any VisualStudio PATH. After start posh, execute following command for set VS environment.

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

## [ConEmu](https://conemu.github.io/)

Windows console emulator with tabs. I use evryday. I love it.

---

## [cd bookmark](https://github.com/takekazuomi/cdbookmark/)

I made directory bookmark cmdlet for save my time. 

Easy to install from [PowerShell Gallery](https://www.powershellgallery.com/packages/Cdbookmark/0.0.4)

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

# End

World is not so easy to live. But we can change by code.
Let's PR.
