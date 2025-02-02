# HTTP Status Codes Cheat Sheet

## 1xx: HTTP Informational Codes

| Code | Status            | Description                               |
|------|-------------------|-------------------------------------------|
| 100  | Continue          |                                          |
| 101  | Switching Protocols |                                        |
| 102  | Processing (WebDAV) |                                       |
| 103  | Checkpoint (draft POST PUT) |                              |
| 122  | Request-URI too long (IE7) |                              |

## 2xx: HTTP Successful Codes

| Code | Status                         | Description                                 |
|------|--------------------------------|---------------------------------------------|
| 200  | OK                             |                                           |
| 201  | Created                        |                                           |
| 202  | Accepted                       |                                           |
| 203  | Non-Authoritative Information (1.1) |                                  |
| 204  | No Content                     |                                           |
| 205  | Reset Content                  |                                           |
| 206  | Partial Content                |                                           |
| 207  | Multi-Status (WebDAV 4918)     |                                           |
| 208  | Already Reported (WebDAV 5842) |                                           |
| 226  | IM Used (3229 GET)             |                                           |

## 3xx: HTTP Redirection Codes

| Code | Status                         | Description                                 |
|------|--------------------------------|---------------------------------------------|
| 300  | Multiple Choices               |                                           |
| 301  | Moved Permanently              |                                           |
| 302  | Found                          |                                           |
| 303  | See Other (1.1)                |                                           |
| 304  | Not Modified                   |                                           |
| 305  | Use Proxy (1.1)                |                                           |
| 306  | Switch Proxy (unused)          |                                           |
| 307  | Temporary Redirect (1.1)       |                                           |
| 308  | Permanent Redirect (7538)      |                                           |

## 4xx: HTTP Client Error Codes

| Code | Status                         | Description                                 |
|------|--------------------------------|---------------------------------------------|
| 400  | Bad Request                    |                                           |
| 401  | Unauthorized                   |                                           |
| 402  | Payment Required (res)         |                                           |
| 403  | Forbidden                      |                                           |
| 404  | Not Found                      |                                           |
| 405  | Method Not Allowed             |                                           |
| 406  | Not Acceptable                 |                                           |
| 407  | Proxy Authentication Required  |                                           |
| 408  | Request Timeout                |                                           |
| 409  | Conflict                       |                                           |
| 410  | Gone                           |                                           |
| 411  | Length Required                |                                           |
| 412  | Precondition Failed            |                                           |
| 413  | Request Entity Too Large       |                                           |
| 414  | Request-URI Too Long           |                                           |
| 415  | Unsupported Media Type         |                                           |
| 416  | Requested Range Not Satisfiable |                                           |
| 417  | Expectation Failed             |                                           |
| 418  | I'm a teapot (2324)            |                                           |
| 422  | Unprocessable Entity (WebDAV 4918) |                                      |
| 423  | Locked (WebDAV 4918)           |                                           |
| 424  | Failed Dependency (WebDAV 4918) |                                      |
| 425  | Unordered Collection (3648)    |                                           |
| 426  | Upgrade Required (2817)        |                                           |
| 428  | Precondition Required (draft)  |                                           |
| 429  | Too Many Requests (draft)      |                                           |
| 431  | Request Header Fields Too Large (draft) |                                 |
| 444  | No Response (nginx)            |                                           |
| 449  | Retry With (MS)                |                                           |
| 450  | Blocked By Windows Parental Controls (MS) |                                |
| 451  | Unavailable For Legal Reasons (draft) |                                 |
| 499  | Client Closed Request (nginx)  |                                           |

## 5xx: HTTP Server Error Codes

| Code | Status                         | Description                                 |
|------|--------------------------------|---------------------------------------------|
| 500  | Internal Server Error          |                                           |
| 501  | Not Implemented                |                                           |
| 502  | Bad Gateway                    |                                           |
| 503  | Service Unavailable            |                                           |
| 504  | Gateway Timeout                |                                           |
| 505  | HTTP Version Not Supported     |                                           |
| 506  | Variant Also Negotiates (2295) |                                           |
| 507  | Insufficient Storage (WebDAV 4918) |                                       |
| 508  | Loop Detected (WebDAV 5842)    |                                           |
| 509  | Bandwidth Limit Exceeded (nostd) |                                       |
| 510  | Not Extended (2774)            |                                           |
| 511  | Network Authentication Required (draft) |                               |
| 598  | Network Read Timeout Error (nostd) |                                       |
| 599  | Network Connect Timeout Error (nostd) |                                    |

## HTTP Code Comments

- **WebDAV**: WebDAV extension
- **1.1**: HTTP/1.1
- **GET, POST, PUT, POST**: For these methods only
- **IE**: IE extension
- **MS**: MS extension
- **nginx**: nginx extension
- **2518, 2817, 2295, 2774, 3229, 4918, 5842**: RFC number
- **draft**: Proposed draft
- **nostd**: Non standard extension
- **res**: Reserved for future use
- **unused**: No longer in use, deprecated

*Wikipedia was used to produce all HTTP codes content: [HTTP Status](http://en.wikipedia.org/wiki/HTTP_status)*
