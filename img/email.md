# Верстка Email писем

- [CSS Support for Email clients](https://www.campaignmonitor.com/css/media-queries/media/)
- [Responsive Email CSS Inliner](https://www.campaignmonitor.com/css/media-queries/media/)

HTML письма не являются веб-страницами, потому что количество поддерживаемых тегов HTML и CSS свойств в каждом почтовом клиенте меняется. В некоторых случаях использования медиа-запросов будут иметь отрицательный эффект, поэтому мы будем применять принцип постоянного улучшения, более современные клиенты будут иметь улучшенную версию дизайна, а устаревшие клиенты - упрощённую.

Некоторые Email клиенты будут рекомендовать не использовать `DOCTYPE`, другие будут рекомендовать `XHTML 1.0 Transitional` или `HTML 4.0`. Наш стартовый шаблон будет выглядеть следующим образом:

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
    <head>
        <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
        <title>Our Vineyard</title>
        <style type="text/css">

        </style>
    </head>
    <body>

    </body>
</html>
```

Мы должны использовать таблицы вместо `div`, чтобы поддерживать большинсво клиентов, при этом у нас возникает проблема при создании адаптивного макета, потому что мы не можем перемещать `td` относительно друг друга, поэтому чтобы обойти это ограничение нам нужно нам нужно вставлять отдельное содержимое в таблицу с единственной ячейкой и при изменение, мы будем изменять уже положение таблиц относительно друг друга.

У нас будет основная таблица с фоном, внутри таблица с контейнером, а внури этой таблицы мы создадим несколько рядков для наших разделов, куда положим отдельные таблицы с контентом. Где возможно используем стилизацию с помощью HTML атрибутов.

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
    <head>
        <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
        <title>Our Vineyard</title>
        <style type="text/css">

        </style>
    </head>
    <body bgcolor="#efe1b0">
        <table width="100%" border="0" bgcolor="#efe1b0" cellspacin="0" cellpadding="0">
            <tr>
                <td>
                    <table class="container" width="640px" align="center" border="0" cellspacin="0" cellpadding="0">
                        <tr>
                            <td></td>
                        </tr>
                        <tr>
                            <td></td>
                        </tr>
                        <tr>
                            <td></td>
                        </tr>
                        <tr>
                            <td></td>
                        </tr>
                        <tr>
                            <td></td>
                        </tr>
                        <tr>
                            <td></td>
                        </tr>
                        <tr>
                            <td></td>
                        </tr>
                    </table>
                </td>
            </tr>
        </table>
    </body>
</html>
```