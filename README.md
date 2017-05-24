# Forum
Following along with the Laracast's series "Let's Build A Forum with Laravel and TDD"

## Local Development

### Seed Data
You may quickly create seed data for local testing using the bundled factories through Tinker:

```
php artisan migrate
```

```
php artisan tinker

>>> $threads = factory('App\Thread', 50)->create();
>>> $threads->each(function ($thread) { factory('App\Reply', 10)->create(['thread_id' => $thread->id]); });
```
