1. **两数之和**
   
```
class Solution {
       function twoSum($nums,$target) {
           foreach($nums as $k=>$v){
               $mu = $target-$v;
               $res = array_search($mu,$nums);
               if($res){
                   return [$k,$res];
               }else{
                   array_diff($nums, [$v]);
               }
           }
       }
   } 
```
2. **Review**
    Laravel 翻译：[https://learnku.com/laravel/t/26375](https://learnku.com/laravel/t/26375)
    在 Laravel 项目中，我们收到很多希望能够为构建多语言 Web 应用提供更好支持的请求。
3. **Tips**
    Yii2 使用图片上传
    Model 定义：
        ![model.png](https://github.com/wujianan/ARTS/blob/master/week_1/model.png)
        
    控制器使用：
   
    
```
private function upload()
{
   if ($_FILES['Product']['error']['cover'] > 0) {
                return false;
   }
            $zone = 'south_china';
            $qiniu = new Qiniu(Product::AK,Product::SK,Product::DOMAIN, Product::BUCKET,$zone);
            $key = uniqid();
            $qiniu->uploadFile($_FILES['Product']['tmp_name']['cover'],$key);
            $cover = $qiniu->getLink($key);
            $pics =[];
            foreach ($_FILES['Product']['tmp_name']['pics'] as $k=>$file) {
                if ($_FILES['Product']['error']['pics'][$k] > 0) {
                    continue;
                }
                $key = uniqid();
                $qiniu->uploadFile($file,$key);
                $pics[$key] = $qiniu->getLink($key);
            }
            $pics = json_encode($pics);
            return compact('cover','pics');
        }    
```
4. Share
    Docker 宿主机连接Docker数据库

*     docker-compose exec mysql bash
*     mysql -uroot -proot
*     ALTER USER ‘root’@’%’ IDENTIFIED WITH mysql_native_password BY ‘root’;



