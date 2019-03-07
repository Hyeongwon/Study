## Chunk vs Cursor


### Performance Test

- 데이터 Laravel 기본 User 사용 (5000건)

* get 결과

* chunk 결과

* cursor 결과

10,000 records:

|           |Time(sec) |Memory(MB) |
|-------------|-----------|------------|
| get()       |      0.17 |         22 |
| chunk(100)  |      0.38 |         10 |
| chunk(1000) |      0.17 |         12 |
| cursor()    |      0.16 |         14 |


100,000 records:

|           |Time(sec) |Memory(MB) |
|--------------|-------------|-----------|
|get()         |        0.8  |     132   |
| chunk(100)   |       19.9  |      10   |
| chunk(1000)  |        2.3  |      12   |
| chunk(10000) |        1.1  |      34   |
| cursor()     |        0.5  |      45   |
