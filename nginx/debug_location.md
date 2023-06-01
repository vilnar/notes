## debug location

```conf
location ~* ^/(?:us/)?blog {
	try_files $uri $uri/ /blog/index.php;

	location ~ \.php$ {
return 200 "debug nginx: \n
document_root: $document_root
fastcgit_script_name: $fastcgi_script_name
request_filename: $request_filename
uri: $uri
scheme: $scheme
host: $host
is_args: $is_args
args: $args
request_uri: $request_uri";

		add_header 'X-Fastcgi-Cache-Status' 'is_blog';

		fastcgi_pass   app:9000;
		fastcgi_index  index.php;
		include        fastcgi_params;
		fastcgi_param  SCRIPT_FILENAME $document_root/index.php;
	}
}
```
