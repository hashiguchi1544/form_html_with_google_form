# googleフォームを自分のオリジナルページで使う方法

htmlファイルに必要最低限を記述しています。


# やるべきこと

google form のソースコードから、**form actionの値**と**各entry値**を取得します。

entryは、分かりにくいので画像で説明します。

ここでは、「お名前」のentryの値を取得するとします。


<img width="674" alt="Screenshot 2023-04-07 9 45 31" src="https://user-images.githubusercontent.com/69481175/230518281-a3ef0775-1b9f-47e2-9979-d886acfc8605.png">


ここでは、一番目のお名前の右側にある数字が該当します。

```
[[623811063,"お名前",null,0,[[401220032,null,1]],
```

お名前のentryは、**401220032**になります。


また、radio buttonの選択項目は、1つ値を、各entryに共有します。
(サンプルでは、「希望職種」に、看護師・介護士・薬剤師...としてますが、
各entryの値は、同じです。)

<img width="606" alt="Screenshot 2023-04-07 9 55 24" src="https://user-images.githubusercontent.com/69481175/230519050-09f2552c-580b-4ce6-9056-1d0118c4dea2.png">



```
<h5>希望する職種</h5>
<input type="radio" name="entry.2108173496" value="看護師">看護師
<input type="radio" name="entry.2108173496" value="介護士・看護助手">介護士・看護助手
<input type="radio" name="entry.2108173496" value="薬剤師">薬剤師
<input type="radio" name="entry.2108173496" value="理学療法士">理学療法士
<input type="radio" name="entry.2108173496" value="作業療法士">作業療法士
<input type="radio" name="entry.2108173496" value="事務職員">事務職員

```

参考になれば幸いです。
