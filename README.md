# homework
维吉尼亚密码解码和失败的跑项目经历
正常的凯撒密码加密性很差，理论上试25次即可，维吉尼亚加密使得每个字母的加密方法有所不同，成了一种理论上不给密钥不可能破解的密码。解码方式很简单，对应密钥进行相应位次变换即可，举例如下（假设只有这几个字母）
| A | B | C | D | E | F | G | H |
|---|---|---|---|---|---|---|---|
| B | C | D | E  |F | G | H | A |
|C|D|E|F|G|H|A|B|
|D|E|F|G|H|A|B|C|
|E|F|G|H|A|B|C|D|
|F|G|H|A|B|C|D|E|
|G|H|A|B|C|D|E|F|
|H|A|B|C|D|E|F|G|
横着为密文，竖着为密钥，对应密钥，密文的交点即为明文，密钥以轮转的方式对应密文直至全部对应，比如密码ABCD，密钥EFG，明文就是EGAH,同理，NEX题凯撒超进化答案为
nex{vlg3nerE_l5_50_E45Y_hahAhahaH4}

PS：原本想搞一个python用遍历的方式解码的代码，失败了，过于菜了(*^_^*)，然后想到C语言指针的对应或许可以，搞不出来。开源项目找不到好的readme，看不懂，下载了配置不好环境，或者不清楚运行成功没，唯一的收获就是下了lively（壁纸软件），以及重温了HELLOGitHub。
