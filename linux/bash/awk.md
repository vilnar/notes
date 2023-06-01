## AWK

```sh
awk '($0 ~ /"status": "200"/){print $0}' source1.log

awk '{ print $4, $5}' query.log
awk '$4 == 5 { print $0}' query.log


awk -f testfile /etc/passwd
```
