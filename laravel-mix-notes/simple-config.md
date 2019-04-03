# Simple Config

## Configuration for Mix

Here's a minimal mix setup that uses browser sync for hot reloading and some css post processing

```
mix
.js("src/js/app.js", "dist/js")
.sass("src/scss/app.scss", "dist/css")
.setPublicPath("./")
.options({
    postCss: [
        require('postcss-sorting')({
            "properties-order": "alphabetical"
        })
    ]
})
.browserSync({
    proxy: "http://localhost:8080/",
    files: ['src/**/*.*', '*.html']
})
```



