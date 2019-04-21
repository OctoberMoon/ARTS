1. **回文数**
```
function ishuiwen($str){   
   $len=strlen($str);   
   $l=1;   
   $k=intval($len/2)+1;   
     for($j=0;$j<$k;$j++){   
       if (substr($str,$j,1)!=substr($str,$len-$j-1,1))   
          {   
   $l=0;   
   break;   
     }   
         }   
  if ($l==1)  {   
  return 1;     
}  else  {    
 return -1;      
 }     
}       
```
2. Review
    The First DDoS Attack Was 20 Years Ago. This Is What We’ve Learned Since. [原文地址](https://medium.com/mit-technology-review/the-first-ddos-attack-was-20-years-ago-this-is-what-weve-learned-since-94a0b6e7f5fc)
3. Tips
Laravel 中 关于消息通知
```
在 User 模型类使用了 Notifiable trait, 而 Notifiable 中又引入了 HasDatabaseNotifications trait。
HasDatabaseNotifications 中有 3 个函数，分别是 获取所有通知、获取未读通知 和 已读通知。


trait HasDatabaseNotifications
{
    public function notifications()
    {
        return $this->morphMany(DatabaseNotification::class, 'notifiable')
                            ->orderBy('created_at', 'desc');
    }

    public function readNotifications()
    {
        return $this->notifications()
                            ->whereNotNull('read_at');
    }

    public function unreadNotifications()
    {
        return $this->notifications()
                            ->whereNull('read_at');
    }
}
```
4. Share
   The First DDoS Attack Was 20 Years Ago. This Is What We’ve Learned Since. [原文](https://medium.com/mit-technology-review/the-first-ddos-attack-was-20-years-ago-this-is-what-weve-learned-since-94a0b6e7f5fc)
   关于DDoS攻击的学习,水平有限,不做评论.
   