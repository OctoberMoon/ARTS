1. **最长公共前缀**
```
 class Solution {

    /**
     * @param String[] $strs
     * @return String
     */
    function longestCommonPrefix($strs) {
        if(empty($strs)){
            return '';
        }

        if(count($strs)==1){
            return $strs[0];
        }
        $res = $strs[0];
        foreach ($strs as $v){
            $str = '';
            for ($i = 0;$i<min(strlen($str1),strlen($str2));$i++){
                if($str1[$i]==$str2[$i]){
                    $str.=$str1[$i];
                }else{
                    break;
                }
            }

            if(empty($res)){
                return '';
            }
        }
    
    }
}

```
2. Review
    Where Do I Start? A Tech Career Journey
. [原文](https://medium.com/@EllenTwomey/where-do-i-start-a-tech-career-journey-e8b8e7ae2d69)
3. Tips
Mac 增加开发效率的神器
```
Alfred
几乎所有搜索功能都可设置  已代替 Mac 默认的搜索
再加上 它的复制功能 极大的增加了开发效率
```
4. Share
   基于 Docker 快速部署多需求 Spark 自动化测试环境 [原文](https://www.ibm.com/developerworks/cn/linux/l-lo-docker-quickly-deploy-multiple-demands-spark/index.html)
   最近 一直在 使用 Docker 周末尝试下 自动化测试

   