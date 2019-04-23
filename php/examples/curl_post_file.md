### curl post 方法发送字段为file的文件

```
    $url = "url address";
    $post_data = array(
            "foo" => "bar",
            //要上传的本地文件地址
            "upload" => new \CURLFile(public_path()."/1.jpeg"),//php>5.5的情况下
    //           "upload" => "@".public_path()."/1.jpeg"//php<5.5的情况
     );
    $ch = curl_init();
    curl_setopt($ch , CURLOPT_URL , $url);
    curl_setopt($ch , CURLOPT_RETURNTRANSFER, 1);
    curl_setopt($ch , CURLOPT_POST, 1);
    curl_setopt($ch , CURLOPT_POSTFIELDS, $post_data);
    $output = curl_exec($ch);
    curl_close($ch);
    echo $output;
```