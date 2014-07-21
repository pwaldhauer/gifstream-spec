# GifStream Specification

GifStream uses a really simple JSON format to describe lists of gif files. Everything should be pretty self-explanatory.

````
{
    "version": 1,
    "title": "GifStream Teststream",
    "identifier": "com.example.gifstream-teststream",
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

The `identifier` field must contain a string that uniquely identifies your GifStream. We recommend using [UTI format](http://en.wikipedia.org/wiki/Uniform_Type_Identifier).

The `base` field can be omitted if you want to use absolute URLs in the `files` array.

The `license` field is optional, too.

## File objects

| Field         | Description                                                | Type   |
|---------------|------------------------------------------------------------|--------|
| `title`       | optional, the title of the gif                             | String |
| `src`         | required, URL or relative path                             | String |
| `license`     | recommended, overwrites the global `license` field         | String |
| `added`       | unix timestamp in seconds                                  | Int  |
