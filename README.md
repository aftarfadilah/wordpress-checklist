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

- [ ] **WP Head:** ![alt text](img/high-label.svg "High") This is important to be included immidiately before `</head>`
```php
wp_head();
```
> * :book: https://codex.wordpress.org/Function_Reference/wp_head

# Function
- [ ] **title-tag:** ![alt text](img/high-label.svg "High") Theme support function to add `<title>` in `wp_head()`
```php
add_theme_support( 'title-tag' );
```
> * :book: https://codex.wordpress.org/Title_Tag

- [ ]  **custom-logo:** ![alt text](img/high-label.svg "High") Add custom logo option in theme customization
```php
add_theme_support( 'custom-logo' );
```
> * :book: https://codex.wordpress.org/Theme_Logo

- [ ] **register_nav_menu($args):** ![alt text](img/high-label.svg "High") Add a menu location to the back-end
```php
function register_menus() {
  register_nav_menus(
    array(
      'primary-menu' => __( 'Primary Menu' ),
      'footer-menu' => __( 'Footer Menu' )
    )
  );
}
add_action( 'init', 'register_menus' );
```
> * :book: https://codex.wordpress.org/Navigation_Menus

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

- [ ] **wp_nav_menu($args):** ![alt text](img/high-label.svg "High") Add a menu location to the front-end
```php
wp_nav_menu( array('theme_location' => 'primary-menu') );
```
> * :book: https://codex.wordpress.org/Navigation_Menus

- [ ] **Custom Logo:** ![alt text](img/high-label.svg "High") Display custom logo from theme customization
```php
$custom_logo_id = get_theme_mod( 'custom_logo' );
$logo = wp_get_attachment_image_src( $custom_logo_id , 'full' );
if ( has_custom_logo() ) {
  echo '<img src="' . esc_url( $logo[0] ) . '"' . 'alt="' . get_bloginfo( 'name' ) . '">';
} else {
  echo '<h1>;'. get_bloginfo( 'name' ) .'</h1>';
}
```
> * :book: https://developer.wordpress.org/themes/functionality/custom-logo/
