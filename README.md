# twitter-video-url
Twitter video url retriever via a function

```
$ git clone https://github.com/linuxjuggler/twitter-video-url \
  cd twitter-video-url
```

Now deploy:

```
$ faas-cli deploy
```

The YAML file is optional:

```
$ faas-cli deploy -f \
https://raw.githubusercontent.com/linuxjuggler/twitter-video-url/master/stack.yml
```

Or from the local file:

```
$ faas-cli deploy
```

Try it out:

```
$ echo -n https://twitter.com/RavenTest/status/1053357651101470729 | \
  faas-cli invoke twitter-video-url
```

Or with `curl`:

```
$ curl localhost:8080/function/twitter-video-url \
 -d "https://twitter.com/RavenTest/status/1053357651101470729"
```

## Notes:

Please note that the script depends on [Youtube-dl](https://rg3.github.io/youtube-dl/) script, which means it may not work 100% as twitter is trying hard to get the video URL

## Credits:

This image has been modified and built based on the code from [faas-and-furious/youtube-dl](https://github.com/faas-and-furious/youtube-dl)