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
