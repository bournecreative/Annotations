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

{% hint style="info" %}
 Super-powers are granted randomly so please submit an issue if you're not happy with yours.
{% endhint %}

Once you're strong enough, save the world:

```
// Ain't no code for that yet, sorry
echo 'You got to trust me on this, I saved the world'
```



