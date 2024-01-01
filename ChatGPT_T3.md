### ChatGPT 應用

#### 類別3: 學習程式語言
##### 情境: 寫程式

模板:
> 你現在是一位**程式語言**專家。請幫我用**程式語言**寫一個函式，它需要做到**某個功能**。

範例:
> 你現在是一位**Python**專家。請幫我用**Python**寫一個函式，它需要做到**輸入一維陣列，把這個一維陣列轉換城二維陣列，同時我要能作到自由地決定二維陣列中的子陣列長度是多少**。
---

模板:
> 你現在是一位**程式語言**專家。請告訴我以下的程式再做什麼。**附上程式碼**

範例:
> 你現在是一位**Python**專家。請告訴我以下的程式再做什麼。
```Python
def convert_to_2d_array(arr, subarray_length):
    # 使用列表生成式將一維陣列分割為指定長度的子陣列
    # 這裡假設 arr 的長度是 subarray_length 的整數倍
    return [arr[i:i+subarray_length] for i in range(0, len(arr), subarray_length)]

# 測試函式
input_array = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11]
subarray_length = 3

result = convert_to_2d_array(input_array, subarray_length)
print(result)
```
---
