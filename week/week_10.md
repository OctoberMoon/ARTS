1. **搜索插入位置**
```
 class Solution {

    /**
     * @param Integer[] $nums
     * @param Integer $target
     * @return Integer
     * 普通方法，时间复杂度是O(n)。顺序遍历数组，如果i索引的元素小于等于$target，那么i+1或者i就是位置
     *
     */
    function searchInsert($nums, $target) {
        $res = 0;
        for ($i=0; $i < count($nums); $i++) { 
          if($nums[$i] <= $target){
            $res = $nums[$i]==$target?$i:$i+1;
          }
        }
        return $res;
    }
    
    /**
     * @param Integer[] $nums
     * @param Integer $target
     * @return Integer
     * 二分查找
     *
     */
    function searchInsert($nums, $target) {
      $length=count($nums);
      $start=0;
      $end=$length;
      while ($start <= $end) {
        $middle=floor(($start+$end)/2);
        if($nums[$middle] == $target){
          return $middle;
        }else{
            if($nums[$middle] < $target) {
              $start = $middle + 1;
            } else {
                $end = $middle - 1;
            }
        }

      }
      return $start;    
}
}

```
2. Review
   How to Deploy a Resilient Go Application to DigitalOcean Kubernetes
. [原文](https://www.digitalocean.com/community/tutorials/how-to-deploy-resilient-go-app-digitalocean-kubernetes)
3. Tips
[区块 学习](https://wujianan.github.io/2019/06/20/1/#more)

4. Share
[Centos GCC升级6.0](https://wujianan.github.io/2019/06/11/1/)

   