1. **移除元素**
```
 class Solution {

    /**
     * @param Integer[] $nums
     * @param Integer $val
     * @return Integer
     */
    function removeElement(&$nums, $val) {
        $j = 0;
        for ($i=0;$i< count($nums);$i++){
            if($nums[$i] != $val){
                $nums[$j] = $nums[$i];
                $j++;
            }
        }
        return $j;
    }
}

```
2. Review
   The Cashless Economy 
. [原文](https://northwesternbusinessreview.org/the-cashless-economy-74b2624d9357)
3. Tips
[docker 学习](https://docs.docker.com/engine/reference/builder/)

4. Share
[Docker Contos 搭建 PHP 环境](https://wujianan.github.io/2019/05/30/3/)

   
