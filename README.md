Chrome 71 seems to reject all audio elements loaded into an AudioContext if the audio element's source is redirected

Error in console when this occurs:

> MediaElementAudioSource outputs zeroes due to CORS access restrictions for...

Issue reported here: https://bugs.chromium.org/p/chromium/issues/detail?id=899745

## Running

`docker-compose up`

## Test Results

|URL|Test|Chrome 71|Chrome 70 (and Safari, Edge, Firefox)
|---|---|---|---|
|http://localhost:8085/audio-302.htm|Redirect on audio source|:thumbsdown:|:thumbsup:|
|http://localhost:8086/audio-302.htm|No redirect, same origin|:thumbsup:|:thumbsup:|
|http://localhost:8085/audio-302.htm?port8086|No redirect, cross origin|:thumbsup:|:thumbsup:|
