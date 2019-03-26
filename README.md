![](https://img.shields.io/badge/style-Welcome-blue.svg?style=for-the-badge&label=Pull%20Requests) ![](https://img.shields.io/badge/style-Aftar%20Fadilah-blue.svg?logo=github&style=for-the-badge&label=Author) ![alt text](http://www.wtfpl.net/wp-content/uploads/2012/12/wtfpl-badge-1.png "WTFPL License")
# Wordpress Checklist 
My Personal Wordpress Theme Development Checklist

# Table of Content
1. [Head](#head)
2. [Function](#function)
3. [Body](#body)
4. ~~[Footer]()~~ *Coming Soon*
5. ~~[Plug-ins]()~~ *Coming Soon*

# Head
- [ ] **DOCTYPE:** ![alt text](img/high-label.svg "High") Reference the browser to use HTML5
```html
<!doctype html> <!-- HTML5 -->
```

- [ ] **Charset:** ![alt text](img/high-label.svg "High") Declare charset. Reccomended charset: UTF-8
```html
<meta charset="utf-8">
```

- [ ] **Viewport:** ![alt text](img/high-label.svg "High") Declare viewport and responsive support
```html
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
```

# Function
- [ ] **title-tag:** ![alt text](img/high-label.svg "High") Theme support function to add `<title>` in `wp_head()`
```php
add_theme_support( 'title-tag' );
```
> * :book: https://codex.wordpress.org/Title_Tag

- [ ] **featured-thumbnail:** ![alt text](img/medium-label.svg "Medium") Theme support function to add post thumbnail
```php
add_theme_support( 'post-thumbnails' ); 
```
> * :book: https://codex.wordpress.org/Post_Thumbnails

# Body
- [ ] **body_class():** ![alt text](img/high-label.svg "High") Add class at `<body>` tag at corresponding pages / posts
```php
<body <?php body_class(); ?> >
```
> * :book: https://developer.wordpress.org/reference/functions/body_class/
