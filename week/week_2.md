1. **整数反转**
```
class Solution {

    /**
     * @param Integer $x
     * @return Integer
     */
    function reverse($x) {
        $up_limit = pow(2,31)-1;        //上限
        $down_limt = -pow(2,31);        //下限
        $remainder = 0;//余数
        $res = 0;
            //范围判断
        if (($x > $down_limt ) && ($x < $up_limit)) {
            while($x > 9){
                $remainder = $x%10; //获取余数 3
                $x = ($x-$remainder)/10;//初始化传进来的变量 12
                $res = $res*10+$remainder;//3
            }
            return $res*10+$x;
        }
    }
}
```
2. Review
    Design pattern: singleton, prototype and builder ：[原文地址](http://coding-geek.com/design-pattern-singleton-prototype-and-builder/)
    
3. Tips
**iterm的部分快捷方式:**
*     open . 在当前目录下打开finder
*     ⌘ + return 全屏
*     ⌘ + f 所查找的内容会被自动复制
*     ⌘ + d 横着分屏 / ⌘ + shift + d 竖着分屏令
*     ⌘ + / 光标位置
*     ⌘ + r 只是换到新一屏，不会像 clear 一样创建一个空屏
*     ctrl + u 清除当前行
*     ctrl + a 到行首
*     ctrl + e 到行尾
*     ctrl + w 删除光标之前的单词
*     ctrl + k 删除到文本末尾
*     ⌘ + alt + 方向键 切换屏幕(用于hotkey window)
*     ⌘ + ⌥ 切换窗口
     
4. Share
    Design pattern: singleton, prototype and builder:  关于单例的使用及思考,以前只会写,通过学习知道更多的使用场景
    [http://coding-geek.com/design-pattern-singleton-prototype-and-builder/](http://coding-geek.com/design-pattern-singleton-prototype-and-builder/)
