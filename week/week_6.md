1. **有效的括号**
```
 class Solution {

    /**
     * @param String $s
     * @return Boolean
     */
    function isValid($s)
{
    static $map = [
        '('=>')',
        '['=>']',
        '{'=>'}',
    ];
    $arr = str_split($s);
    foreach ($arr as $v) {
        if (!empty(end($stack))) {
            if ($map[end($stack)]==$v) {
                array_pop($stack);
            } else {
                $stack[]=$v;
            }
        } else {
            $stack[]=$v;
        }
    }
    // var_dump($stack);
    // die;
 
    if ($stack===[]) {
        return true;
    }
    return false;
}
}

```
2. Review
    Deep Learning Could Reveal Why the World Works the Way It Does
At a major AI research conference, one researcher laid out how existing AI techniques might be used to analyze causal relationships in data
. [原文](https://medium.com/mit-technology-review/deep-learning-could-reveal-why-the-world-works-the-way-it-does-9be8b5fbfe4f)
3. Tips
js swal 使用
$script = <<<SCRIPT     $('button[type=submit]').on('click',function(e){
            event.preventDefault();
            swal({
                title: '请妥善保存好助记词!',
                text: '遗失后不能恢复!',
                type: 'warning',
                showCancelButton: true,
                confirmButtonColor: '#3085d6',
                cancelButtonColor: '#d33',
                confirmButtonText: '确认提交',
                cancelButtonText: "取消",
            }).then(function (isConfirm) {
                if (isConfirm.value == true ){
                     $("form").submit();
                }else{
                    event.preventDefault();
                    return false;
                }
            }).catch(swal.noop);
        });
SCRIPT;
                Admin::script($script);

```
4. Share
   Git 和 GitHub 基础简介[原文](https://www.ibm.com/developerworks/cn/opensource/os-cn-git-and-github-1/index.html)
   Git 是目前业界最流行的版本控制系统（Version Control System），而 GitHub 是开源代码托管平台的翘楚。越来越多的从业者、从业团队以及开源贡献者首选二者用于管理项目代码。本文首先从概念的角度介绍版本控制系统、Git 和 GitHub，并着重通过一些实验来演示 Git 的基础特性，使您能够对 Git 和 GitHub 有更清晰的认识。

   