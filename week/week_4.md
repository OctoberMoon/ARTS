1. **罗马数字转整数**
```
 function index($s)
    {
        $ss = array(
            'M'=> 1000,
            'CM'=> 900,
            'D'=> 500,
            'CD'=> 400,
            ' C'=> 100,
            'XC'=> 90,
            'L'=> 50,
            'XL'=> 40,
            'X' => 10,
            'IX'=> 9,
            'V'=> 5,
            'IV'=> 4,
            'I'=> 1,
    );
            $result = 0;
        foreach ($ss as $k=>$v) {
            while (strpos($s,$k)===0) {
                $result += $v;
                $s = substr($s,strlen($k));
            }
        }
        echo $result;
   }   
```
2. Review
    Who’s Using Your Face? The Ugly Truth About Facial Recognition
Researchers are scraping our images from social media and CCTV. We may not like the consequences.
. [原文](https://medium.com/financial-times/whos-using-your-face-the-ugly-truth-about-facial-recognition-ad2748c87179)
3. Tips
Laravel-admin 
```
$form->text('')->value()->readOnly();   //只读
$form->saved(function (Form $form) {
            if ($form->status=='on') {  //获取当前提交值
                $form->model()->markAsRead($form);
            }
            return redirect('/admin/user');  更改跳转链接
        });
}
```
4. Share
   How Huawei can beat Apple and Samsung’s ecosystem. [原文](https://hackernoon.com/how-huawei-can-beat-apples-ecosystem-7c3218bd5739)
   华为如何击败苹果和三星的生态系统

   