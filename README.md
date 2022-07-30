# Windows Error Codes as JSON

[![build](https://github.com/Henkru/windows-lasterror-json/actions/workflows/generate.yml/badge.svg)](https://github.com/Henkru/windows-lasterror-json/actions/workflows/generate.yml)

This [automated](https://github.com/Henkru/windows-lasterror-json/actions) repository
pulls Windows' [error code](https://docs.microsoft.com/en-us/windows/win32/debug/system-error-codes)
messages to JSON files, which can be easily queried like:

```bash
$ jq '.[]|select(.code == 14)' all.json
{
  "title": "ERROR_OUTOFMEMORY",
  "code": 14,
  "msg": "Not enough storage is available to complete this operation."
}

```
