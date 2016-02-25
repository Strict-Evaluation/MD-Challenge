# MD-Challenge

A webpage downloading tool, to use it:
(Make sure that you have port 12345 free).
Fire up the downloader with
```
./downloader.rb start &
```
and then set a couple pages up to download like so:
```
./downloader.rb google.com
```
which'll give you a job ID back.
Running:
```
./downloader.rb check <ID>
```
will tell you the status of your download, or if finished, print it to stdout.
When you want to stop running your daemon, simply run:
```
./downloader.rb kill
```

## Notes
Instead of threading it I wanted to make my program run as a daemon in the background.
I could've just popped off a thread for each URL to download, but since you wanted a download queue I decided not to make it asynchronous.
It might be nice to store the local port to connect to in an environment variable instead of hardcoding it too.
