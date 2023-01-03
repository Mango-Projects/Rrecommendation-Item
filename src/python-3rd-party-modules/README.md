# Python 3rd Party Modules

## Intro

分享一些我常用的第三方模組  
平台：`Windows 10, Python 3.11.x`

## Index

- [Python 3rd Party Modules](#python-3rd-party-modules)
  - [Intro](#intro)
  - [Index](#index)
  - [Table](#table)
  - [Modules Introduction](#modules-introduction)
    - [Rich](#rich)
    - [Pretty Errors](#pretty-errors)
    - [Requests](#requests)
    - [Pycord](#pycord)

## Table

| Module Name     | Description                  | Introduction Index               | PyPI                                | Github                                            | Tags                    |
| --------------- | ---------------------------- | -------------------------------- | ----------------------------------- | ------------------------------------------------- | ----------------------- |
| `Rich`          | 提供豐富的文字效果及格式輸出 | [#rich](#rich)                   | [rich][rich-pypi]                   | [Textualize/rich][rich-github]                    | `#pretty-print #output` |
| `Pretty Errors` | 優化錯誤訊息                 | [#pretty-errors](#pretty-errors) | [pretty-errors][pretty-errors-pypi] | [onelivesleft/PrettyErrors][pretty-errors-github] | `#errors`               |
| `Requests`      | 請求網路上的資源，用於爬蟲   | [#requests](#requests)           | [requests][requests-pypi]           | [psf/requests][requests-github]                   | `#request #HTTP`        |
| `Pycord`        | 用於編寫Discord Bot          | [#pycord](#pycord)               | [py-cord][pycord-pypi]              | [Pycord-Development/pycord][pycord-github]        | `#discord-bot`          |
|                 |                              |                                  |                                     |                                                   |                         |


## Modules Introduction

### Rich
> Rich 是一款提供終端機介面中 *豐富的* 文字效果及精美的格式設定的 Python 函式庫。
> [Rich API](https://rich.readthedocs.io/en/latest/) 讓終端機介面加上色彩及樣式變得易如反掌。Rich 也可以繪製漂亮的表格、進度條、Markdown、語法醒目標示的程式碼、Traceback（追溯）……。
> 
> ![rich-features][rich-features]

### Pretty Errors
> Pretty Errors 能將錯誤訊息美化，使開發者更好的追蹤錯誤
>
> ![pretty-errors-features][pretty-errors-features]

### Requests
> Requests 是一個簡單且優雅的HTTP模組
>
> ```python
> >>> import requests
> >>> r = requests.get('https://httpbin.org/basic-auth/user/pass', auth=('user', 'pass'))
> >>> r.status_code
> 200
> >>> r.headers['content-type']
> 'application/json; charset=utf8'
> >>> r.encoding
> 'utf-8'
> >>> r.text
> '{"authenticated": true, ...'
> >>> r.json()
> {'authenticated': True, ...}
> ```

### Pycord
> Pycord 是一個基於 discord.py 編寫的 Discord 機器人模組
>
> ```python
> import discord
> 
> bot = discord.Bot()
> 
> @bot.slash_command()
> async def hello(ctx, name: str = None):
>     name = name or ctx.author.name
>     await ctx.respond(f"Hello {name}!")
> 
> @bot.user_command(name="Say Hello")
> async def hi(ctx, user):
>     await ctx.respond(f"{ctx.author.mention} says hello to {user.name}!")
> 
> bot.run("token")
> ```

---

<!-- Table Links -->
[rich-pypi]: https://pypi.org/project/rich
[rich-github]: https://github.com/Textualize/rich

[pretty-errors-pypi]: https://pypi.org/project/pretty-errors
[pretty-errors-github]: https://github.com/onelivesleft/PrettyErrors

[requests-pypi]: https://pypi.org/project/requests/
[requests-github]: https://github.com/psf/requests

[pycord-pypi]: https://pypi.org/project/py-cord/
[pycord-github]: https://github.com/Pycord-Development/pycord


<!-- Introduction Links -->
[rich-features]: https://raw.githubusercontent.com/textualize/rich/master/imgs/features.png
[pretty-errors-features]: https://raw.githubusercontent.com/onelivesleft/PrettyErrors/master/example.png