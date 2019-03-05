## 트랜잭션이란?
- 데이터베이스의 상태를 변화시키기 해서 수행하는 작업의 단위를 뜻한다.

- SELECT
- INSERT
- DELETE
- UPDATE

### 작업의 단위
- ex) 은행에서 돈을 송금
- 내 계좌 돈 마이너스 상대방 계좌 돈 플러스

### 트랜잭션의 특징

- 원자성 (Atomicity)
- 일관성 (Consistency)
- 독립성 (Isolation)
- 지속성 (Durability)


### 트랜잭션의 Commit, Rollback


### 예제

* DB 스키마
![2019-03-05 4 10 09](https://user-images.githubusercontent.com/14510347/53787363-fbc6d400-3f61-11e9-9726-fcf88fe3210b.png)

* 작업단위 (A가 B에게 1000원 계좌이체)
```php
    $userA->account->amount -= 1000;
    $userB->account->amount += 1000;

    $userA->account->save();
    $userB->account->save();
```

* 트렌잭션 없이 계좌이체 도중 문제 발생
```php
    $userA->account->amount -= 1000;
    $userB->account->amount += 1000;

    $userA->account->save();
    throw new \Exception();
    $userB->account->save();
```
![2019-03-05 8 36 40](https://user-images.githubusercontent.com/14510347/53804170-2593f100-3f8a-11e9-8f8a-ceb552e2acb7.png)




* 트랜젹션이 걸린 상황에서 문제 발생

```php
$userA->account->amount -= 1000;
$userB->account->amount += 1000;

DB::transaction(function () use ($userA, $userB){
    try {
        $userA->account->save();
        throw new \Exception();
        $userB->account->save();
    } catch (QueryException $e) {
        throw $e;
    }
});
```
![2019-03-05 8 27 05](https://user-images.githubusercontent.com/14510347/53804196-393f5780-3f8a-11e9-96c8-a4daa7ed6a97.png)


### Laravel 트랜잭션
```php
public function transaction(Closure $callback, $attempts = 1)
{
    for ($currentAttempt = 1; $currentAttempt <= $attempts; $currentAttempt++) {
        $this->beginTransaction();

        // We'll simply execute the given callback within a try / catch block and if we
        // catch any exception we can rollback this transaction so that none of this
        // gets actually persisted to a database or stored in a permanent fashion.
        try {
            return tap($callback($this), function ($result) {
                $this->commit();
            });
        }

        // If we catch an exception we'll rollback this transaction and try again if we
        // are not out of attempts. If we are out of attempts we will just throw the
        // exception back out and let the developer handle an uncaught exceptions.
        catch (Exception $e) {
            $this->handleTransactionException(
                $e, $currentAttempt, $attempts
            );
        } catch (Throwable $e) {
            $this->rollBack();

            throw $e;
        }
    }
}
```

### Commit 중 실패하면??
![helloworld-407507-6](https://user-images.githubusercontent.com/14510347/53804278-73a8f480-3f8a-11e9-9755-5d87d4972c2c.png)

