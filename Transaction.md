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


### Laravel 트랜잭션

```php
public function transaction(Closure $callback)
{
  try {
    return tap($callback($this), function ($result) {
      $this->commit();
    });
  } catch (Throwable $e) {
      $this->rollBack();
      throw $e;
    }
  }
}
```

