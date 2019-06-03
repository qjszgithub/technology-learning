###代码生成器生成的文件(以user为例)

- controller:app/Http/UserController控制器
- models:app/Models/UserModels该类对应的模型
- views模型视图:
    - create_and_edit.blade.php
    - index.blade.php
    - show.blade.php
- request:app/Http/UserRequest 请求类（验证逻辑
- Observers：UserObserver代码观察器（用户观察用户的模型操作）
- Policies：UserPolicy用户权限类
- 数据迁移相关：
    - UserFactory.php 模型工厂
    - 2014_10_12_000000_create_users_table.php 数据迁移文件
    - UsersTableSeeder.php 数据填充文件
- 路由文件修改web.php Route::resource('user', 'UserController', ['only' => ['index', 'show', 'create', 'store', 'update', 'edit', 'destroy']]);