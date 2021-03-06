# Sources for the akka-stream / akka-http scala.world 2015 conference talk

To test, run this in sbt:

```
log-service/re-start
backend/runMain example.repoanalyzer.Step6
```

Then, open the browser at [http://localhost:8080](http://localhost:8080). All the other steps should work as well.

Geo IP resolution uses the server at http://freegeoip.net/ which only allows a certain quota of free requests per period
(though requests will be cached between runs, see `Cache` and the `ip-cache` folder). Also, we experienced some downtime
of this free server so we included part of the cache with the source code.

The sources contain an example log file to replay which contains a big amount of nonsense data in the right format.

Here's the output of running Step5:

![Step 5 output screencast](https://raw.githubusercontent.com/jrudolph/scala-world-2015/master/screencast.gif)
