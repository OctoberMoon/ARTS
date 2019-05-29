1. **删除排序数组中的重复项**
```
 class Solution {

    /**
     * @param Integer[] $nums
     * @return Integer
     */
    function removeDuplicates(&$nums) {
        $len = count($nums);
        for ($i=0;$i<$len;$i++) {
            if (!isset($nums[$i]))  {
                continue;
            }
            for ($j=$i+1;$j<$len;$j++) {
                if ($nums[$i]==$nums[$j]) {
                    unset($nums[$j]);
                } else {
                    break;
                }
            }
        }
        return count($nums);
    }
}

```
2. Review
    How To Use SSH to Connect to a Remote Server in Ubuntu
. [原文](https://www.digitalocean.com/community/tutorials/how-to-use-ssh-to-connect-to-a-remote-server-in-ubuntu)
3. Tips
```
总结下高并发 相关的知识点 [地址](https://wujianan.github.io/2019/05/28/1/)

```
4. Share
[Centos防火墙操作](https://wujianan.github.io/2019/05/29/1/)
