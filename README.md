# Help

## Laravel naming convention


### Naming Controllers

Controllers should be in PascalCase/CapitalCase.

They should be in singular case, no spacing between words, and end with "Controller".

Also, each word should be capitalised (i.e. BlogController, not blogcontroller).

For example: `BlogController`, `AuthController`, `UserController`.

Bad examples: `UsersController` (because it is in plural), `Users` (because it is missing the Controller suffix).


### Naming database tables in Laravel

DB tables should be in lower case, with underscores to separate words (snake_case), and should be in plural form.

For example: `posts`, `project_tasks`, `uploaded_images`.

Bad examples: `all_posts`, `Posts`, `post`, `blogPosts`

#### Pivot tables

Pivot tables should be all lower case, each model in alphabetical order, separated by an underscore (snake_case).

For example: `post_user`, `task_user` etc.

Table column names should be in snake_case (underscores between words) - in lower case. You shouldn't reference the table name.

For example: `post_body`, `id`, `created_at`.

Foreign keys should be the model name (singular), with '\_id' appended to it (assuming the PK in the other table is 'id').

For example: `comment_id`, `user_id`.

Normal variables should typically be in camelCase, with the first character lower case.

For example: `$users = ...`, `$bannedUsers = ...`.

If the variable contains an array or collection of multiple items then the variable name should be in plural. Otherwise, it should be in singular form.

For example: `$users = User::all();` (as this will be a collection of multiple User objects), but `$user = User::first()` (as this is just one object)


### Naming Conventions for models

A model should be in PascalCase/CapitalCase. They should be in singular, no spacing between words, and capitalised.

For example: `User` (`\App\User` or `\App\Models\User`, etc), `ForumThread`, `Comment`.

I recommend that you create models and migrations at the same time by running `php artisan make:model -m ForumPost`. This will auto-generate the migration file (in this case, for a DB table name of 'forum_posts').

These should be lower case, snake_case. They should also follow the same conventions as the table column names.

For example: `$this->updated_at`, `$this->title`.

Bad examples: `$this->UpdatedAt`, `$this->blogTitle`.

Methods in your models in Laravel projects, like all methods in your Laravel projects, should be camelCase with the first character lower case.

For example: `public function get()`, `public function getAll()`.

### Method naming conventions in controllers

These should follow the same rules as model methods. I.e. camelCase (first character lowercase).

In addition, for normal CRUD operations, they should use one of the following method names.

| Verb      | URI                    | Typical Method Name | Route Name     |
| --------- | ---------------------- | ------------------- | -------------- |
| GET       | `/photos`              | `index()`           | photos.index   |
| GET       | `/photos/create`       | `create()`          | photos.create  |
| POST      | `/photos`              | `store()`           | photos.store   |
| GET       | `/photos/{photo}`      | `show()`            | photos.show    |
| GET       | `/photos/{photo}/edit` | `edit()`            | photos.edit    |
| PUT/PATCH | `/photos/{photo}`      | `update()`          | photos.update  |
| DELETE    | `/photos/{photo}`      | `destroy()`         | photos.destroy |


## DDD IN LARAVEL

[**Domain-driven design**](https://growthbranch.gumroad.com/l/jretq) (DDD) is a popular software development methodology based on separating your application’s domain into small, well-defined parts.


![pic1](https://github.com/rivara/Help/assets/3527499/140b6412-1595-4c37-93d1-2004ad8bfc5e)
<br>
<h5>DDD adapting to Laravel</h5>


![pic2_](https://github.com/rivara/Help/assets/3527499/18f9b5f4-872e-455c-a773-a3dd863058ed)





