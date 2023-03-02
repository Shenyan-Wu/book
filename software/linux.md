---
description: 通过阅读鸟哥的Linux私房菜这本书
---

# Linux

## 1. Linux是什么与如何学习

* 作業系統(Operating System)主要在管理與驅動硬體，因此必須要能夠管理記憶體、管理裝置、 負責行程管理以及系統呼叫等等。因此，只要能夠讓硬體準備妥當(Ready)的情況， 就是一個陽春的作業系統了。
* Unix的前身是由貝爾實驗室(Bell lab.)的Ken Thompson利用組合語言寫成的， 後來在1971-1973年間由Dennis Ritchie以C程式語言進行改寫，才稱為Unix。
* 1977年由Bill Joy釋出BSD (Berkeley Software Distribution)，這些稱為Unix-like的作業系統。
* 1984年由Andrew Tanenbaum開始製作Minix作業系統，該系統可以提供原始碼以及軟體；
* 1984年由Richard Stallman提倡GNU計畫，倡導自由軟體(Free software)， 強調其軟體可以『自由的取得、複製、修改與再發行』，並規範出GPL授權模式， 任何GPL(General Public License)軟體均不可單純僅販賣其軟體，也不可修改軟體授權。
* 1991年由芬蘭人Linus Torvalds開發出Linux作業系統。簡而言之，Linux成功的地方主要在於： Minix(Unix), GNU, Internet, POSIX 及虛擬團隊的產生。
* 符合 Open source 理念的授權相當多，比較知名的如 Apache / BSD / GPL / MIT 等。
* Linux本身就是個最陽春的作業系統，其開發網站設立在[http://www.kernel.org](http://www.kernel.org/)，我們亦稱Linux作業系統最底層的資料為『核心(Kernel)』。
* 從 Linux kernel 3.0 開始，已經捨棄奇數、偶數的核心版本規劃，新的規劃使用主線版本 (MainLine) 為依據， 並提供長期支援版本 (longterm) 來加強某些功能的持續維護。
* Linux distributions的組成含有：『Linux Kernel + Free Software + Documentations(Tools) + 可完整安裝的程序』所製成的一套完整的系統。
* 常見的 Linux distributions 分類有『商業、社群』分類法，或『RPM、DPKG』分類法
* 學習 Linux 最好從頭由基礎開始學習，找到一本適合自己的書籍，加強實作才能學會

## 2. 主机规划与磁盘分类

* 新添購電腦硬體配備時，需要考量的角度有『遊戲機/工作機』、『效能/價格比』、『效能/消耗瓦數』、『支援度』等；
* 舊的硬體配備可能由於保存的問題或者是電子零件老化的問題，導致電腦系統非常容易在運作過程中出現不明的當機情況
* Red Hat的硬體支援：https://hardware.redhat.com/?pagename=hcl
* 在Linux系統中，每個裝置都被當成一個檔案來對待，每個裝置都會有裝置檔名。
* 磁碟裝置檔名通常分為兩種，實際SATA/USB裝置檔名為/dev/sd\[a-p]，而虛擬機的裝置可能為/dev/vd\[a-p]
* 磁碟的第一個磁區主要記錄了兩個重要的資訊，分別是： (1)主要開機記錄區(Master Boot Record, MBR)：可以安裝開機管理程式的地方，有446 bytes (1)分割表(partition table)：記錄整顆硬碟分割的狀態，有64 bytes；
* 磁碟的 MBR 分割方式中，主要與延伸分割最多可以有四個，邏輯分割的裝置檔名號碼，一定由5號開始；
* 如果磁碟容量大於 2TB 以上時，系統會自動使用 GPT 分割方式來處理磁碟分割。
* GPT 分割已經沒有延伸與邏輯分割槽的概念，你可以想像成所有的分割都是主分割！
* 某些作業系統要使用 GPT 分割時，必須要搭配 UEFI 的新型 BIOS 格式才可安裝使用。
* 開機的流程由：BIOS-->MBR-->-->boot loader-->核心檔案；
* boot loader的功能主要有：提供選單、載入核心、轉交控制權給其他loader
* boot loader可以安裝的地點有兩個，分別是 MBR 與 boot sector
* Linux作業系統的檔案使用目錄樹系統，與磁碟的對應需要有『掛載』的動作才行；
* 新手的簡單分割，建議只要有/及swap兩個分割槽即可

## 3.&#x20;
