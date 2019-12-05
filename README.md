# Brogue 2

## Usage

HTML:

```html
<script src="https://sgalal.github.io/Brogue2/brogue2.js"></script>
```

JavaScript:

```javascript
let 小韻號 = 1919;  // 選擇第 1919 小韻（拯小韻）
console.log(equal母(小韻號, '章'));  // true, 拯小韻是章母
console.log(in母(小韻號, ['曉', '匣']));  // false, 拯小韻不是曉匣母
```

## High-Level API

Not implemented

## Low-Level API

* function `equal韻`
* function `in韻`
* function `equal母`
* function `in母`
* function `equal組`
* function `in組`
* function `equal開合`
* function `equal等`
* function `in等`
* function `equal韻賅上去`
* function `in韻賅上去`
* function `equal韻賅上去入`
* function `in韻賅上去入`
* function `equal攝`
* function `in攝`
* function `equal聲`
* function `in聲`

Property Name | Chinese Name | English Name | Possible Values
:- | :- | :- | :-
韻 | 韻母 | rhyme | 東冬鍾江…；董湩腫講…；送宋用絳…；屋沃燭覺…
韻賅上去 | 韻母（舉平以賅上去） | rhyme (舉平以賅上去) | 東冬鍾江…；祭泰夬廢；屋沃燭覺…
韻賅上去入 | 韻母（舉平以賅上去入） | rhyme (舉平以賅上去入) | 東冬鍾江…；祭泰夬廢
攝 | 攝 | class | 通江止遇蟹臻山效果假宕梗曾流深咸
母 | 聲母 | initial | 幫滂並明端透定泥知徹澄孃精清從心邪莊初崇生俟章昌船書常見溪羣疑影曉匣云以來日
組 | 組 | group | 幫端知精莊章見（未涵蓋「影曉匣云以來日」）
開合 | 開合 | rounding | 開合
等 | 等 | division | 一二三四；1234
聲 | 聲調 | tone | 平上去入；<del>仄</del>；<del>舒</del>

* function `is重紐A類`
* function `is重紐B類`

<del>Not implemented</del>

對重紐的處理：韻賅上去入的「支」就包括了「支、支A、支B」三種情況。

重紐四等（A類）是三等韻。

元韻放在臻攝而不是山攝。

## Internal APIs

`small_rhymes`

二維數組。低維中的每一維：小韻, 韻母, 聲母, 開合, 等。

`char_entities`

Dict

Key: Chinese Character

Value: `Int` or `Array Int`. Corresponding small rhymes.

## Build

```sh
$ wget -P build https://github.com/sgalal/Guangyun/releases/download/v2.1/data.sqlite3
$ python build/build.py
```

## License

BSD 3-Clause License

Codes from CodeMirror project (`docs/index.files/codemirror`) is distributed under MIT license.
