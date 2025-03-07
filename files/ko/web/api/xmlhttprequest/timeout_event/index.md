---
title: timeout
slug: Web/API/XMLHttpRequest/timeout_event
translation_of: Web/API/XMLHttpRequest/timeout_event
original_slug: Web/API/XMLHttpRequest/timeout
---
**`timeout`** 이벤트는 미리 설정한 시간이 만료되어 진행이 종료되면 시작합니다.

| Bubbles        | No                                       |
| -------------- | ---------------------------------------- |
| Cancelable     | No                                       |
| Target objects | {{domxref("XMLHttpRequest")}} |
| Interface      | {{domxref("ProgressEvent")}}     |

## Examples

```js
var client = new XMLHttpRequest();
client.open("GET", "http://www.example.org/example.txt");
client.ontimeout = function(e) {
  console.error("Timeout!!");
}
client.send();
```

## Inheritance

`timeout` 이벤트는 {{domxref("Event")}}에서 상속받은 {{domxref("ProgressEvent")}} 인터페이스를 구현합니다. 이 인터페이스에 선언된 속성(property)과 메서드를 사용할 수 있습니다.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{domxref("XMLHttpRequest")}}
