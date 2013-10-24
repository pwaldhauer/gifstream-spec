# GifStream Specification

GifStream uses a really simple JSON format to describe lists of gif files. Everything should be pretty self-explanatory.

````
{
    "version": 1,
    "title": "GifStream Teststream",
    "base": "http://example.com/gifs/",
    "files": [
        "0001.gif",
        "0002.gif"
    ]
}
````

The `base` field can be omitted if you want to use absolute URLs in the `files` array.
