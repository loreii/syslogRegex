# syslogRegex
RFC3164 RFC5424 simple parser, after this split is neccesary a parse of data and structured data in order to use it.

## RFC3164
```javascript
^\<([0-9]{1,3})\>([A-Za-z]{3} [0-9]{1,2} \d{2}:\d{2}:\d{2}) ([\S]+) ([\S\s]+)
```
Match:
```
<131>Jan 23 17:05:05 rdmlpavesi1d gs-rest-service error message slf4j thread:http-nio-8080-exec-1 priority:ERROR category:command.AppSyslogd.Application exception:
```
## RFC5424
```javascript
^\<([0-9]{1,3})\>(\d{0,2}) (\-|[\S]+) (\-|[\S]{1,255}) (\-|[\S]{1,48}) (\-|[\S]{1,128}) (\-|[\S]{1,32}) (\-|\[[\S\s]+\]) ([\S\s]+){0,1}
```
Match:
```
match : __<165>1 2003-10-11T22:14:15.003Z mymachine.example.com evntslog - ID47 [exampleSDID@32473 iut="3" eventSource="Application" eventID="1011"] An application event log entry...
```

