## IPv6標頭

IPv6為標頭引入了一種新格式，使其更簡單。

![IPv6 Header](http://ipv6.br/media/noticias/cabecalho-021.jpg)

此新標頭中的所有字段都具有固定長度，總共64個字節。 具有固定大小的事實極大地加速了路由器對分組的處理，因為不需要計算某些字段的長度和整個報頭的大小。 此外，通過在實踐中幾乎沒有實用性的字段使用的字段數減少了。


#### 版本
- 4位
- 標識所用協議的版本。在這種情況下，該字段的值為6。

#### 交通等級
- 8位
- 按服務類或優先級標識軟件包。它提供與“IPv4服務類型”字段相同的功能和定義。

#### 流標識符
- 20位
- 標識相同通信流的數據包。理想地，該字段由目的地地址配置以將流與每個應用分開，並且網絡中間節點可以將其與源地址和目的地地址一起使用以執行對分組的特定處理。

#### 數據大小
- 16位
- 指示IPv6標頭旁邊發送的數據的大小（以字節為單位）。取代了IPv4中，這表明該標頭的大小加上傳送的數據的大小的字段總大小。但是，擴展標頭的大小也會添加到此新字段中。

#### 下一個標題
- 8位
- 標識當前擴展標頭之後的擴展標頭。它已改名（在IPv4中被稱為協議），以反映IPv6報文的新組織，因為它不再包含其他協議的數字，以表明該類型的擴展報頭。

#### 路由限制
- 8位
- 此字段被遞減每個路由跳和指示通過該分組可以被丟棄之前通過的路由器的最大數目。他標準化的方式生存時間正在使用的IPv4（TTL）字段，它從在秒定義為時間包，如果他們不到達您的目的地被丟棄原始描述顯著不同。

#### 源地址
- 128位
- 表示數據包的源地址。

#### 目的地址
- 128位
- 表示數據包的目標地址。

#### 更多信息

http://ipv6.br/post/cabecalho/

https://tools.ietf.org/html/rfc2460
