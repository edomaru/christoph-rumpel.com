```php
public function calculateScore(User $user): int
{
    // ✅ Edge-cases are checked first
    if ($user->inactive) {
        return 0;
    }

    // ✅ Every case has its own section which makes them easy to follow step by step
    if ($user->hasBonus) {
        return $user->score + $this->bonus;
    }

    return $user->score;
}
```
