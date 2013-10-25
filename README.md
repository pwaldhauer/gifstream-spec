# GifStream Specification

GifStream uses a really simple JSON format to describe lists of gif files. Everything should be pretty self-explanatory.

````
{
    "version": 1,
    "title": "GifStream Teststream",
    "base": "http://example.com/gifs/",
    "files": [
        {
            "title":"a cat riding a bike",
            "src": "0001.gif"
        },
        {
            "title":"a dog riding a bike",
            "src": "0002.gif"
        }
    ]
}
````

The `base` field can be omitted if you want to use absolute URLs in the `files` array.

## File objects

Each file should at least have a `src` property. All other properties are optional.
