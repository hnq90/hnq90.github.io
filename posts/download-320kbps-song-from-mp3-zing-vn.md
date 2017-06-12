# Download 320Kbps song from mp3.zing.vn

```
#!/bin/sh
songId=$1

parseJson () {
  python -c "import json,sys;sys.stdout.write(json.dumps(json.load(sys.stdin)$1))";
}

fetch () {
  local output=`wget -q --method GET --progress=dot --output-document - http://api.mp3.zing.vn/api/mobile/song/getsonginfo?requestdata={\"id\":\"$songId\"}`
  local link=$(echo $output | parseJson "['source']['320']")
  local artist=$(echo $output | parseJson "['artist']")
  local title=$(echo $output | parseJson "['title']")

  link="${link%\"}"
  link="${link#\"}"
  title="${title%\"}"
  title="${title#\"}"
  artist="${artist%\"}"
  artist="${artist#\"}"

  local fileName=`echo "$(echo -e $title)_$(echo -e $artist)_320kbps"`

  wget --method GET \
    --header 'cache-control: no-cache' \
    --output-document="$fileName.mp3" \
    - $link
}

fetch
```

Source: https://gist.github.com/hnq90/38eaa792ad1f19df6f88345477c5badb
