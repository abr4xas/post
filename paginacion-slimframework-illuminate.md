Title: Paginación con Slimframework e illuminate
Date: 2016-02-16 23:40
Category: php
Tags: php, slim, framework, illuminate
Slug: paginacion-slimframework-illuminate
Author: abr4xas
twitter: abr4xas
Summary: Una facil implementación de una paginación usando slimframework e illuminate y twig
image: /img/pagination.png

Desde hace unas semanas he estado trabajando en proyectos que estan utilizando  slimframework, twig e illuminate y hoy me encontre con un "*pequeño*" problema al realizar una paginación y esta fue la forma en que lo solucione:

```php
$app->get('/user', function() use ($app) {

        $users = $app->user->where('active', true)->get();

        $user = $app->user
                ->where('active', true)
                ->orderBy('username', 'desc')
                ->take(5)
                ->get();

        $app->render('admin/templates/userlist.html', [
            'users' => $user,
            'userAll' => $users,
        ]);

    })->name('user.list');

    $app->get('/users/:number', function($number) use ($app) {

        $users = $app->user->where('active', true)
                    ->orderBy('username', 'desc')
                    ->skip(5 * ($number - 1))
                    ->take(5)
                    ->get();

        $AllUser = $app->user->where('active', true)->get();

        $pages = intval(ceil(count($AllUser) / 5));
        $app->render('admin/templates/user_list.html', [
            'users' => $users,
            'pages'    => $pages,
            'number'   => $number,
        ]);
    })->name('user_list');
```
### userlist template

```html
% if users is empty %}
{% if users is empty %}
                    <p>No registered users</p>
                    {% else %}
                    <div class="content table-responsive table-full-width">
                        <table class="table table-hover table-striped">
                            <thead>
                                <th>Name</th>
                                <th>Username</th>
                            </thead>
                            <tbody>
                                    {% for user in users %}
                                <tr>
                                    <td>{{ user.getFullName }}</td>
                                    <td>{{ user.username }}</td>
                                </tr>
                                    {% endfor %}
                            </tbody>
                        </table>
                    </div>
                    {% endif %}
                      <nav>
                        <ul class="pager">
                            <li class="previous {% if userAll|length <= 5 %}disabled{% endif %}">
                                <a {% if userAll|length > 5 %}href="{{ urlFor('user_list', {'number': 2}) }}"{% endif %}>
                                    <span aria-hidden="true">←</span> Older
                                </a>
                            </li>
                            <li class="next disabled">
                                <a>Newer <span aria-hidden="true">→</span></a>
                            </li>
                        </ul>
                      </nav>
```
### user_list template

```html
% if users is empty %}
                    <p>No registered users</p>
                    {% else %}
                    <div class="content table-responsive table-full-width">
                        <table class="table table-hover table-striped">
                            <thead>
                                <th>Name</th>
                                <th>Username</th>
                            </thead>
                            <tbody>
                                    {% for user in users %}
                                <tr>
                                    <td>{{ user.getFullName }}</td>
                                    <td>{{ user.username }}</td>
                                </tr>
                                    {% endfor %}
                            </tbody>
                        </table>
                    </div>
                    {% endif %}
                    <nav>
                        <ul class="pager">
                            <li class="previous {% if number >= pages or number < 1 %}disabled{% endif %}">
                                <a {% if number < pages and number >= 1 %}href="{{ urlFor('user_list', {'number': number + 1}) }}"{% endif %}>
                                    <span aria-hidden="true">←</span> Older
                                </a>
                            </li>
                            <li class="next {% if number <= 1 or number > pages %}disabled{% endif %}">
                                <a {% if number > 1 and number <= pages %}href="{{ urlFor('user_list', {'number': number - 1}) }}"{% endif %}>Newer 
                                    <span aria-hidden="true">→</span>
                                </a>
                            </li>
                        </ul>
                    </nav>
```
Espero que esto le ayude a alguien y pues si, con `illuminate/pagination` se puede hacer pero no encontre forma que me funcionara correctamente xD