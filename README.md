# Wordpress Checklist
My Personal Wordpress Theme Development Checklist

# Table of Content
- [Head](#head)
- [Function](#function)
- ~~[Body]()~~ *Coming Soon*
- ~~[Footer]()~~ *Coming Soon*
- ~~[Plug-ins]()~~ *Coming Soon*

# Head
[ ] **DOCTYPE:** ![High](img/high-label.svg?raw=true "Preview") Reference the browser to use HTML5
```
<!doctype html> <!-- HTML5 -->
```

[ ] **Charset:** ![High](img/high-label.svg?raw=true "Preview") Declare charset. Reccomended charset: UTF-8
```
<meta charset="utf-8">
```

[ ] **Viewport:** ![High](img/high-label.svg?raw=true "Preview") Declare viewport and responsive support
```
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
```

# Function
[ ] **title-tag:** ![High](img/high-label.svg?raw=true "Preview") Theme support function to add `<title>` in `wp_head()`
```
add_theme_support( 'title-tag' );
```
> book https://codex.wordpress.org/Title_Tag

[ ] **featured-thumbnail:** ![Medium](img/medium-label.svg?raw=true "Preview") Theme support function to add post thumbnail
```
add_theme_support( 'post-thumbnails' ); 
```
> book https://codex.wordpress.org/Post_Thumbnails