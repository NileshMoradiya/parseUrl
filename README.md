## parseUrl v0.0.1-alpha
*Written by [Talon Poole](http://theghostin.me) and released under the MIT license*

This simple function uses Regex to deconstruct and extract all
the good stuff out of a URL. It's currently:

### *Under Development*

## How to Use
Simply call `parseUrl()` and pass in the url as a string.

	var urlStuff = parseUrl("https://github.com/LegitTalon/parseUrl");

It will return an object. Here's what the URL above would return:

    { protocol: "https"
    , baseUrl: "github.com"
    , dirs: ["/LegitTalon", "/parseUrl"]
    , filePath: "/LegitTalon/parseUrl"
    , file: "index.html"
    , fileType: "html"
    , fileName: "index"
    };

in the example above

    urlStuff.fileType == "html"; // true
	urlStuff.name == "index"; // true

because those are the defaults choosen by `parseUrl` if it doesn't
find an extension.

	var coolSong = parseUrl("https://theghostin.me/cool%20Song.mp3");

returns:

	{ protocol: "https"
	, baseUrl: "theghostin.me"
    , dirs: ["/"]
    , filePath: "coolsong.mp3"
    , file: "coolsong.mp3"
    , fileType: ".mp3"
    , fileName: "coolsong"
	};

## Bugs?
If there's a bug please report it appropriately or submit a pull request.