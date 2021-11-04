# Weather_Prediction_Tokyo

### ファイル
- data.csv

  気象庁データ : 2018/1/1~2021/10/25 内の東京都の平均気温データ
  
- Weather_Prediction.ipynb

  テーマ設定〜学習結果&評価〜考察〜Pythonコード

### フォルダ（案①〜④）：モデルの学習結果

- 案①
```
Model(
  (lstm): LSTM(365, 180, batch_first=True)
  (lstm_): Sequential(
    (0): Dropout(p=0.2, inplace=False)
    (1): ReLU()
  )
  (dense): Linear(in_features=180, out_features=1, bias=True)
)
```

- 案②
```
Model(
  (lstm): LSTM(365, 128, batch_first=True)
  (lstm_): Sequential(
    (0): Dropout(p=0.2, inplace=False)
    (1): ReLU()
  )
  (dense1): Sequential(
    (0): Linear(in_features=128, out_features=64, bias=True)
    (1): ReLU()
    (2): Dropout(p=0.2, inplace=False)
  )
  (dense2): Sequential(
    (0): Linear(in_features=64, out_features=32, bias=True)
    (1): ReLU()
    (2): Dropout(p=0.1, inplace=False)
  )
  (dense3): Sequential(
    (0): Linear(in_features=32, out_features=16, bias=True)
    (1): ReLU()
    (2): Dropout(p=0.1, inplace=False)
  )
  (dense4): Linear(in_features=16, out_features=1, bias=True)
)
```

- 案③
```
Model(
  (lstm): LSTM(365, 180, batch_first=True)
  (lstm_): Sequential(
    (0): Dropout(p=0.2, inplace=False)
    (1): ReLU()
  )
  (dense1): Sequential(
    (0): Linear(in_features=180, out_features=90, bias=True)
    (1): ReLU()
    (2): Dropout(p=0.2, inplace=False)
  )
  (dense2): Sequential(
    (0): Linear(in_features=90, out_features=30, bias=True)
    (1): ReLU()
    (2): Dropout(p=0.1, inplace=False)
  )
  (dense3): Sequential(
    (0): Linear(in_features=30, out_features=7, bias=True)
    (1): ReLU()
    (2): Dropout(p=0.1, inplace=False)
  )
  (dense4): Linear(in_features=7, out_features=1, bias=True)
)
```

- 案④
```
Model(
  (lstm): LSTM(365, 52, batch_first=True)
  (lstm_): Sequential(
    (0): Dropout(p=0.2, inplace=False)
    (1): ReLU()
  )
  (dense1): Sequential(
    (0): Linear(in_features=52, out_features=24, bias=True)
    (1): ReLU()
    (2): Dropout(p=0.2, inplace=False)
  )
  (dense2): Sequential(
    (0): Linear(in_features=24, out_features=12, bias=True)
    (1): ReLU()
    (2): Dropout(p=0.1, inplace=False)
  )
  (dense3): Sequential(
    (0): Linear(in_features=12, out_features=4, bias=True)
    (1): ReLU()
    (2): Dropout(p=0.1, inplace=False)
  )
  (dense4): Linear(in_features=4, out_features=1, bias=True)
)
```


