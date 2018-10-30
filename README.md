##

## Running

`docker-compose up`

## Test Results

|URL|Test|Result|
|http://localhost:8085/audio-302.htm|Redirect on audio source|:thumbsdown:|
|http://localhost:8086/audio-302.htm|No redirect, same origin|:thumbsup:|
|http://localhost:8085/audio-302.htm?port=8086|No redirect, cross origin|:thumbsup:|
