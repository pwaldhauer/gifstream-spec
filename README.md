# GifStream Specification

GifStream uses a really simple JSON format to describe lists of gif files. Everything should be pretty self-explanatory.

````
{
    "version": 1,
    "title": "GifStream Teststream",
    "base": "http://example.com/gifs/",
    "license": "Very important license information",
    "files": [
        {
            "added": 123123123,
            "license": "Detailed license information",
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

The `license` field is optional, too.

## File objects

| Field         | Description                                                | Type   |
|---------------|------------------------------------------------------------|--------| 
| `src`         | required, URL or relative path                             | String |
| `license`     | recommended, overwrites the global `license` field         | String |
| `added`       | unix timestamp in seconds                                  | Int  |
