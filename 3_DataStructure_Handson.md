## 列表List

### 列表取值

建立三維列表結構並實現特定元素存取，原始列表為：

```python
matrix_3d = [
    [[1,2], [3,4]],
    [[5,6], [7,8]],
    [[9,10], [11,12]]
]
```

要求：

1. 使用三重索引取出數值7
2. 取出第二維度的所有偶數元素


### 列表生成

結合`range()`，建立符合以下條件的列表：

1. 生成1到100中能被3或5整除的數字列表
2. 將上述列表按整除3和5分類為二維列表

## mapping & 字典

### 字典合併

使用兩個字典`dict1 = {'a': 1, 'b': 2}`和`dict2 = {'b': 3, 'c': 4}`，實作以下功能：

1. 使用`update()`合併字典並保留最大value值
2. 建立反向字典(變成value到key的映射)

### 字典取值

根據教材中的學生資料：

```python
id = [1, 2, 3, 4]
name = ['Ryan', 'Tom', 'Emma', 'Amy', 'Morgan']
school = ['NYCU','NTU','NTU','NYCU','NYCU']
```

建立字典映射後，統計名字**長度**分佈，並記得使用`get()`方法安全存取不存在的鍵值


## NumPy矩陣

### 多維矩陣操作

建立3D陣列並實作以下操作：

1. 使用`np.full()`建立3x3x3全1陣列
2. 沿著第三軸進行累加計算(`cumsum()`)

## Pandas資料框

### 人口統計分析系統

根據教材中的州人口資料：

```python
population_dict = {'California': 38332521, 'Texas': 26448193, 
                  'New York': 19651127, 'Florida': 19552860, 
                  'Illinois': 12882135}
area_dict = {'California': 423967, 'Texas': 695662, 
            'New York': 141297, 'Florida': 170312, 
            'Illinois': 149995}
```

實作以下分析：

1. 計算人口密度並新增欄位
2. 找出面積最大與人口最多的州



### 時間序列處理

建立日期範圍索引的銷售資料並計算滾動月平均成長率（月平均成長率計算講義沒有教，可以參考網路資源）

```python
# 日期範圍索引的銷售資料生成
dates = pd.date_range('2025-01-01', periods=365)
sales = pd.Series(np.random.randint(100, 500, 365), index=dates)
```


