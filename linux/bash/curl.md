# CURL

## For file upload

```sh
curl --form "fileupload=@filename.txt" "http://hostname/resource"
```

## POST

```sh
curl --request POST "http://example.com/form/" --data "field1=value1&field2=value2
```

or
```sh
curl -X POST "http://test.com/form" -d "field=value1&field2=value2"
```

## CORS

```sh
curl -H "Origin: https://localhost:4200" --insecure --verbose "https://api.domain.com/v2/test"
```

## SSL certificate problem

```sh
curl -ki -X GET "https://localhost/test"
```

## download file

```sh
curl -L -o {file_name} {url}
```


## encode pass

```sh
echo -n "login:pass" | base64 -w0
curl --header "Authorization: Basic {hash_from_terminal}" ...
```
