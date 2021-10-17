 Obfuscated CTF
 This CTF involved deobfuscating a javscript file to find a key.
- [1.1. Source Code](#11-source-code)
- [1.2. De-Obfuscation using jsNice](#12-de-obfuscation-using-jsnice)
- [1.3 Algorithm to Solve key](#13-algorithm-to-solve-key)

## 1.1. Source Code
```
(function(_0x5aa67e, _0x1999ca) {
    var _0x5b137a = _0x2789,
        _0x4a18fb = _0x5aa67e();
    while (!![]) {
        try {
            var _0x3bba1b = parseInt(_0x5b137a(0xa5)) / 0x1 * (-parseInt(_0x5b137a(0xb1)) / 0x2) + parseInt(_0x5b137a(0xb2)) / 0x3 + parseInt(_0x5b137a(0xb0)) / 0x4 + parseInt(_0x5b137a(0xb4)) / 0x5 * (-parseInt(_0x5b137a(0xae)) / 0x6) + parseInt(_0x5b137a(0xaf)) / 0x7 * (parseInt(_0x5b137a(0xb3)) / 0x8) + -parseInt(_0x5b137a(0xaa)) / 0x9 * (parseInt(_0x5b137a(0xa7)) / 0xa) + -parseInt(_0x5b137a(0xac)) / 0xb * (-parseInt(_0x5b137a(0xab)) / 0xc);
            if (_0x3bba1b === _0x1999ca) break;
            else _0x4a18fb['push'](_0x4a18fb['shift']());
        } catch (_0x51d6e8) {
            _0x4a18fb['push'](_0x4a18fb['shift']());
        }
    }
}(_0x52e3, 0x917a5));

function _0x2789(_0x36b0c4, _0x45825c) {
    var _0x52e398 = _0x52e3();
    return _0x2789 = function(_0x2789aa, _0xb6bcf0) {
        _0x2789aa = _0x2789aa - 0xa5;
        var _0x268993 = _0x52e398[_0x2789aa];
        return _0x268993;
    }, _0x2789(_0x36b0c4, _0x45825c);
}

function _0x52e3() {
    var _0x1438d1 = ['11qxyyxT', 'push', '85698NfzGeA', '1673kGumbN', '4716144ykaPgN', '770StBfBH', '686346mTvDDX', '11896HItGjA', '210NUAYJp', 'getElementById', '1135vxeHtr', 'length', '50yqyKtd', 'flag_input', 'value', '1721529LbeKYu', '9911184DKPAwn'];
    _0x52e3 = function() {
        return _0x1438d1;
    };
    return _0x52e3();
}

function submit_flag() {
    var _0x2e5dda = _0x2789,
        _0x28bac2 = document[_0x2e5dda(0xb5)](_0x2e5dda(0xa8)),
        _0x53b8b6 = _0x28bac2[_0x2e5dda(0xa9)],
        _0x19c111 = [0x34, 0xc7, 0xc1, 0xd0, 0x1c, 0x6a, 0xe2, 0xe2, 0xca, 0x1f, 0x64, 0x64, 0xd, 0x22, 0x61, 0xbb, 0xb8, 0xbe, 0xd, 0x1f, 0x73, 0x8b, 0x73, 0x67, 0x13, 0x88, 0x13, 0x28],
        _0x36ac03 = [];
    for (var _0x3e323d = 0x0; _0x3e323d < _0x53b8b6[_0x2e5dda(0xa6)]; _0x3e323d++) {
        _0x36ac03[_0x2e5dda(0xad)](_0x53b8b6['charCodeAt'](_0x3e323d));
    }
    for (var _0x3e323d = 0x0; _0x3e323d < _0x36ac03[_0x2e5dda(0xa6)]; _0x3e323d++) {
        for (var _0x26e237 = 0x1; _0x26e237 < 0xd; _0x26e237++) {
            _0x36ac03[_0x3e323d] = (_0x36ac03[_0x3e323d] * 0x21 - 0xb) % 0xff;
        }
    }
    compare_arrays(_0x19c111, _0x36ac03) ? input_colors(!![]) : input_colors(![]);
}

function compare_arrays(_0x529793, _0x52c598) {
    var _0x588143 = _0x2789,
        _0x6d3c97 = _0x529793[_0x588143(0xa6)];
    if (_0x52c598['length'] != _0x6d3c97) return ![];
    else {
        for (var _0x264d89 = 0x0; _0x264d89 < _0x6d3c97; _0x264d89++)
            if (_0x529793[_0x264d89] != _0x52c598[_0x264d89]) return ![];
        return !![];
    }
}
```

## 1.2. De-Obfuscation using jsNice
We can easily de-obfuscate some of this code using a tool such as [jsNice](http://jsnice.org/). After putting the code through this tool we are given the following:

```
'use strict';
(function(groupingFunction, data) {
  /** @type {function(number, ?): ?} */
  var toMonths = _0x2789;
  var data = groupingFunction();
  for (; !![];) {
    try {
      /** @type {number} */
      var lastScriptData = parseInt(toMonths(165)) / 1 * (-parseInt(toMonths(177)) / 2) + parseInt(toMonths(178)) / 3 + parseInt(toMonths(176)) / 4 + parseInt(toMonths(180)) / 5 * (-parseInt(toMonths(174)) / 6) + parseInt(toMonths(175)) / 7 * (parseInt(toMonths(179)) / 8) + -parseInt(toMonths(170)) / 9 * (parseInt(toMonths(167)) / 10) + -parseInt(toMonths(172)) / 11 * (-parseInt(toMonths(171)) / 12);
      if (lastScriptData === data) {
        break;
      } else {
        data["push"](data["shift"]());
      }
    } catch (_0x51d6e8) {
      data["push"](data["shift"]());
    }
  }
})(_0x52e3, 595877);
/**
 * @param {number} indentLevel
 * @param {?} parent
 * @return {?}
 */
function _0x2789(indentLevel, parent) {
  var params = _0x52e3();
  return _0x2789 = function(level, tileSize) {
    /** @type {number} */
    level = level - 165;
    var val = params[level];
    return val;
  }, _0x2789(indentLevel, parent);
}
/**
 * @return {?}
 */
function _0x52e3() {
  /** @type {!Array} */
  var compiledVars = ["11qxyyxT", "push", "85698NfzGeA", "1673kGumbN", "4716144ykaPgN", "770StBfBH", "686346mTvDDX", "11896HItGjA", "210NUAYJp", "getElementById", "1135vxeHtr", "length", "50yqyKtd", "flag_input", "value", "1721529LbeKYu", "9911184DKPAwn"];
  /**
   * @return {?}
   */
  _0x52e3 = function() {
    return compiledVars;
  };
  return _0x52e3();
}
/**
 * @return {undefined}
 */
function submit_flag() {
  /** @type {function(number, ?): ?} */
  var prefixed = _0x2789;
  var conditions = document[prefixed(181)](prefixed(168));
  var PL$83 = conditions[prefixed(169)];
  /** @type {!Array} */
  var possibleBom = [52, 199, 193, 208, 28, 106, 226, 226, 202, 31, 100, 100, 13, 34, 97, 187, 184, 190, 13, 31, 115, 139, 115, 103, 19, 136, 19, 40];
  /** @type {!Array} */
  var PL$49 = [];
  /** @type {number} */
  var PL$40 = 0;
  for (; PL$40 < PL$83[prefixed(166)]; PL$40++) {
    PL$49[prefixed(173)](PL$83["charCodeAt"](PL$40));
  }
  /** @type {number} */
  PL$40 = 0;
  for (; PL$40 < PL$49[prefixed(166)]; PL$40++) {
    /** @type {number} */
    var _0x26e237 = 1;
    for (; _0x26e237 < 13; _0x26e237++) {
      /** @type {number} */
      PL$49[PL$40] = (PL$49[PL$40] * 33 - 11) % 255;
    }
  }
  if (compare_arrays(possibleBom, PL$49)) {
    input_colors(!![]);
  } else {
    input_colors(![]);
  }
}
/**
 * @param {!Array} a1
 * @param {!Object} a2
 * @return {?}
 */
function compare_arrays(a1, a2) {
  /** @type {function(number, ?): ?} */
  var gotoNewOfflinePage = _0x2789;
  var o = a1[gotoNewOfflinePage(166)];
  if (a2["length"] != o) {
    return ![];
  } else {
    /** @type {number} */
    var i = 0;
    for (; i < o; i++) {
      if (a1[i] != a2[i]) {
        return ![];
      }
    }
    return !![];
  }
}
;
```
## 1.3 De-Obfuscated Code Explanation


#### To Be Continued





## 1.4 Algorithm to Solve key

```
var possibleBom = [52, 199, 193, 208, 28, 106, 226, 226, 202, 31, 100, 100, 13, 34, 97, 187, 184, 190, 13, 31, 115, 139, 115, 103, 19, 136, 19, 40];
var keyCharList = [];
z = 0;

for (; z < possibleBom.length; z++) {
  i = 41;

  for (; true;) {  
    y = i;
    x = 1;

    for (; x < 13; x++) {
      y = (y * 33 - 11) % 255;
    }

    if (y == possibleBom[z]) {
      keyCharList.push(i);
      break;
    }

    i++;
  }
}
console.log(String.fromCharCode(...keyCharList));

```
