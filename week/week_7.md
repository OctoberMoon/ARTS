1. **合并两个有序链表**

```

 function Merge($pHead1, $pHead2)
{
 if($pHead1 == NULL)
  return $pHead2;
 if($pHead2 == NULL)
  return $pHead1;
 $reHead = new ListNode();
 if($pHead1->val < $pHead2->val){
  $reHead = $pHead1;
  $pHead1 = $pHead1->next;
 }else{
  $reHead = $pHead2;
  $pHead2 = $pHead2->next;
 }
 $p = $reHead;
 while($pHead1&&$pHead2){
  if($pHead1->val <= $pHead2->val){
   $p->next = $pHead1;
   $pHead1 = $pHead1->next;
   $p = $p->next;
  }
  else{
   $p->next = $pHead2;
   $pHead2 = $pHead2->next;
   $p = $p->next;
  }
 }
 if($pHead1 != NULL){
  $p->next = $pHead1;
 }
 if($pHead2 != NULL)
  $p->next = $pHead2;
 return $reHead;
}

```
2. Review
    让您的数据对黑客毫无用处
. [原文](https://www.ibm.com/developerworks/cn/analytics/library/infuse-your-app-with-data-encryption-and-key-management/index.html)
3. Tips
```
总结下高并发 相关的知识点 [地址](https://wujianan.github.io/2019/05/19/%E9%AB%98%E5%B9%B6%E5%8F%91%E4%BC%98%E5%8C%96/)

```
4. Share
每天记几个 提升效率

    1. alias ga='git add'
    2. alias gaa='git add --all'
    3. alias gapa='git add --patch'
    4. alias gau='git add --update'
    5. alias gav='git add --verbose'
    6. alias gap='git apply'
    8. alias gb='git branch'
    9. alias gba='git branch -a'
    10. alias gbd='git branch -d'
    11. alias gbda='git branch --no-color --merged | command grep -vE "^(\*|\s*(master|develop|dev)\s*$)" | command xargs -n 1 git branch -d'
    12. alias gbD='git branch -D'
    13. alias gbl='git blame -b -w'
    14. alias gbnm='git branch --no-merged'
    15. alias gbr='git branch --remote'
    16. alias gbs='git bisect'
    17. alias gbsb='git bisect bad'
    18. alias gbsg='git bisect good'
    19. alias gbsr='git bisect reset'
    20. alias gbss='git bisect start'

   