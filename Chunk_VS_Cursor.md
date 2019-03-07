## Chunk vs Cursor

### 실제 쿼리
Chunk
```mysql
select * from `users` where `users` limit 100 offset 0"
...
```
cursor


### Performance Test

- 데이터 Laravel 기본 User 사용 (5000건)

* get 쿼리
```php
$users = User::get();
```

* get 결과
![5000get](https://user-images.githubusercontent.com/14510347/53956666-97517380-411f-11e9-871a-64d11bbbdb99.png)

* chunk(100) 쿼리
```php
User::chunk(100, function ($users) {
    foreach ($users as $user) {
        // TODO
    }
});
```

* chunk(100) 결과
![5000cursor](https://user-images.githubusercontent.com/14510347/53956698-a9cbad00-411f-11e9-9728-1cf5994ad842.png)

* cursor 쿼리
```php
foreach (User::cursor() as $user) {
    // TODO
}
```

* cursor 결과
![5000chunk](https://user-images.githubusercontent.com/14510347/53956712-b2bc7e80-411f-11e9-962a-3f49967bfab2.png)

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
