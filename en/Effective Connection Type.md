TOPIC: Effective Connection Type

# Effective Connection Type

**Effective connection type** (ECT) refers to the measured network performance, returning a  cellular
connection type, like 3G, even if the actual connection is tethered broadband or WiFi, based on the
time between the browser requesting a page and effective type of the connection.

The values of  '`slow-2g`', '`2g`', '`3g`', or '`4g`' is determined using observed round-trip times
and downlink values.

## Table Of Effective Connection Types

| ECT | Minimum RTT | Maximum downlink | Explanation |
| -- | -- | -- | --|
|`slow-2g`|2000ms|50 Kbps|The network is suited for small transfers only such as text-only pages.|
| `2g` | 1400ms | 70 Kbps | The network is suited for transfers of small images. |
|`3g`|270ms|700 Kbps|The network is suited for transfers of large assets such as high resolution images, audio, and SD video. |
| `4g` | 0ms | ∞ | The network is suited for HD video, real-time video, etc. |

effectiveType is a property of the Network Information API, exposed to JavaScript via
the navigator.connection object. To see your effective connection type, in the console of the
developer tools of a supporing browser, enter the following:

```javascript
navigator.connection.effectiveType;
```

## See Also

### General Knowledge

- [Network Information API](https://developer.mozilla.org/en-US/docs/Web/API/Network_Information_API)
- [`NetworkInformation`](https://developer.mozilla.org/en-US/docs/Web/API/NetworkInformation)
- [`NetworkInformation.effectiveType`](https://developer.mozilla.org/en-US/docs/Web/API/NetworkInformation/effectiveType)
