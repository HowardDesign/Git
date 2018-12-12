# git config

git 設定檔分三個階層, System、Global、Local

* System: 整台電腦共用的設定(C:\ProgramData\Git\config)
* Global: 個人帳號共用的設定 (%userprofile%\\.gitconfig)
* Local: Git專案資料夾的設定 (.git\config\)

# 語法

```
git config [<file-option>] [type] [--show-origin] [-z|--null] name [value [value_regex]]
git config [<file-option>] [type] --add name value
git config [<file-option>] [type] --replace-all name value [value_regex]
git config [<file-option>] [type] [--show-origin] [-z|--null] --get name [value_regex]
git config [<file-option>] [type] [--show-origin] [-z|--null] --get-all name [value_regex]
git config [<file-option>] [type] [--show-origin] [-z|--null] [--name-only] --get-regexp name_regex [value_regex]
git config [<file-option>] [type] [-z|--null] --get-urlmatch name URL
git config [<file-option>] --unset name [value_regex]
git config [<file-option>] --unset-all name [value_regex]
git config [<file-option>] --rename-section old_name new_name
git config [<file-option>] --remove-section name
git config [<file-option>] [--show-origin] [-z|--null] [--name-only] -l | --list
git config [<file-option>] --get-color name [default]
git config [<file-option>] --get-colorbool name [stdout-is-tty]
git config [<file-option>] -e | --edit
```

# 範例

```
git config --list --show-origin
git config --system --list --show-origin
git config --global --list --show-origin
git config --local --list --show-origin

git config --global http."https://www.git.xsg/".sslCAInfo M:\gosmio.cer
git config --global core.editor "\"C:\Program Files\Sublime Text 3\sublime_text.exe\"" -n -w
git config --global core.autocrlf true 
```

# gosmio.cer
```
-----BEGIN CERTIFICATE-----
MIIDgjCCAmqgAwIBAgIQDsJUsG80eI9ENIrVJnanRjANBgkqhkiG9w0BAQsFADBI
MRMwEQYKCZImiZPyLGQBGRYDYml6MRYwFAYKCZImiZPyLGQBGRYGZ29zbWlvMRkw
FwYDVQQDExBnb3NtaW8tQ0FTUlYyLUNBMCAXDTE1MTEwNDAxNDYwM1oYDzIxMTUx
MTA0MDE1NjAyWjBIMRMwEQYKCZImiZPyLGQBGRYDYml6MRYwFAYKCZImiZPyLGQB
GRYGZ29zbWlvMRkwFwYDVQQDExBnb3NtaW8tQ0FTUlYyLUNBMIIBIjANBgkqhkiG
9w0BAQEFAAOCAQ8AMIIBCgKCAQEAx1X6k3RVZT15M+S68U732+simQJDY8UdpNpP
Bj0P6TNxyNwnBJpbJwKd9ys/a+rCIwuHzbMfxf23jj23CykdCHnQJOt2/tqO91/5
Tc/WjggfzCO0mb2nBRe9tqLT0mqZW78Ohg2XXbFdvRJxADpuOJcCbbLCuBuIVw4U
fOdgsLfQ+6DdqQiLuFdUR1qW5IQNcA4KjQYFwJL52y/oeMM2SAoODqBZpU+o3T5I
x9GRDH1SVtHkacJfhDyGVV8O/dW1SNH868jFKsRBZjHnABXXw5IJU6gV7wSBwLwU
tZoXYCCtsSI6gDfyyLcKPdeUmRChgKVqNsr2SCMwW6YYzxYReQIDAQABo2YwZDAT
BgkrBgEEAYI3FAIEBh4EAEMAQTALBgNVHQ8EBAMCAYYwDwYDVR0TAQH/BAUwAwEB
/zAdBgNVHQ4EFgQUbzSVENF9DBIBa0HBr/MhL5u2sv8wEAYJKwYBBAGCNxUBBAMC
AQAwDQYJKoZIhvcNAQELBQADggEBADAoOx7Q7S3DEZZModnbElD4DXGGPHDfCtvG
9Vg/I+TkXOMgveAbMRCyNSvs05x9EiJ98r1qq6f5XiXdQAjPn4V59zaqm8gvTrfn
B4Rg4Fa7caY5y1Rpo6XtFj1PmK+3oqEQ2K42lyhTwZaAT1dLNZWN7pU47BmXi08K
z9UQUFgXRexHFHtcosAl/Y5fTqIjQZ4WBE87itVlIlOpn7HTU3C/tIM7SIFWP/PD
H50MD66YQorEidylZCePa1OahXT15glu2FaOjaLl8AKpsw8QBHFJ8iqSnojuxsCs
JpIv/CHG/IQ1gx8Rj2EeVuC3tjp1GnLTvZ3mOqq5OVOckAnCyiA=
-----END CERTIFICATE-----
```