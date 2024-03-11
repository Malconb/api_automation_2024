miguel@malconb-vd04:~$ curl "https://api.todoist.com/rest/v2/projects/2330059478" -X POST --data '{"name": "Example negative case update"}' -H "Content-Type: application/json" -H "Authorization: Bearer $mytoken" -v
Note: Unnecessary use of -X or --request, POST is already inferred.
*   Trying 108.158.104.37:443...
* Connected to api.todoist.com (108.158.104.37) port 443 (#0)
* ALPN, offering h2
* ALPN, offering http/1.1
*  CAfile: /etc/ssl/certs/ca-certificates.crt
*  CApath: /etc/ssl/certs
* TLSv1.0 (OUT), TLS header, Certificate Status (22):
* TLSv1.3 (OUT), TLS handshake, Client hello (1):
* TLSv1.2 (IN), TLS header, Certificate Status (22):
* TLSv1.3 (IN), TLS handshake, Server hello (2):
* TLSv1.2 (IN), TLS header, Finished (20):
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* TLSv1.3 (IN), TLS handshake, Encrypted Extensions (8):
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* TLSv1.3 (IN), TLS handshake, Certificate (11):
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* TLSv1.3 (IN), TLS handshake, CERT verify (15):
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* TLSv1.3 (IN), TLS handshake, Finished (20):
* TLSv1.2 (OUT), TLS header, Finished (20):
* TLSv1.3 (OUT), TLS change cipher, Change cipher spec (1):
* TLSv1.2 (OUT), TLS header, Supplemental data (23):
* TLSv1.3 (OUT), TLS handshake, Finished (20):
* SSL connection using TLSv1.3 / TLS_AES_128_GCM_SHA256
* ALPN, server accepted to use h2
* Server certificate:
*  subject: CN=todoist.com
*  start date: May 11 00:00:00 2023 GMT
*  expire date: Jun  8 23:59:59 2024 GMT
*  subjectAltName: host "api.todoist.com" matched cert's "*.todoist.com"
*  issuer: C=US; O=Amazon; CN=Amazon RSA 2048 M02
*  SSL certificate verify ok.
* Using HTTP2, server supports multiplexing
* Connection state changed (HTTP/2 confirmed)
* Copying HTTP/2 data in stream buffer to connection buffer after upgrade: len=0
* TLSv1.2 (OUT), TLS header, Supplemental data (23):
* TLSv1.2 (OUT), TLS header, Supplemental data (23):
* TLSv1.2 (OUT), TLS header, Supplemental data (23):
* Using Stream ID: 1 (easy handle 0x55755da57eb0)
* TLSv1.2 (OUT), TLS header, Supplemental data (23):
> POST /rest/v2/projects/2330059478 HTTP/2
> Host: api.todoist.com
> user-agent: curl/7.81.0
> accept: */*
> content-type: application/json
> authorization: Bearer XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
> content-length: 40
> 
* TLSv1.2 (OUT), TLS header, Supplemental data (23):
* We are completely uploaded and fine
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* TLSv1.3 (IN), TLS handshake, Newsession Ticket (4):
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* Connection state changed (MAX_CONCURRENT_STREAMS == 128)!
* TLSv1.2 (OUT), TLS header, Supplemental data (23):
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* TLSv1.2 (IN), TLS header, Supplemental data (23):
< HTTP/2 404 
< content-type: text/plain; charset=utf-8
< content-length: 17
< date: Mon, 11 Mar 2024 17:48:01 GMT
< access-control-allow-credentials: false
< access-control-allow-origin: *
< cache-control: no-cache
< referrer-policy: strict-origin-when-cross-origin
< server: gunicorn
< set-cookie: csrf=4f6808780b4e43a8a618206e23240df7; Expires=Thu, 09-Mar-2034 17:48:01 GMT; Secure; Path=/; SameSite=None
< set-cookie: tduser=v4.public.eyJ1c2VyX2lkIjogNDg1MzY5NjgsICJleHAiOiAiMjAyNC0wMy0yNVQxNzo0ODowMSswMDowMCJ9om8vmEgtFMTFNFdlPx86_Ktfz_VNTJfg-qLeHjA-6QMnsAUYV8YzpvFXtlWp7zWEKylUTGsUr_2diMeUs_M4BQ; Domain=.todoist.com; Expires=Mon, 25-Mar-2024 17:48:01 GMT; Max-Age=1209600; Secure; HttpOnly; Path=/
< set-cookie: todoistd="/CUdA09psYiwY7pwgn9sRGC/RQQ=?"; Domain=.todoist.com; Expires=Tue, 11-Mar-2025 17:48:01 GMT; Max-Age=31536000; Secure; HttpOnly; Path=/; SameSite=None
< strict-transport-security: max-age=31536000; includeSubDomains; preload
< vary: Accept-Encoding
< x-cache: Error from cloudfront
< via: 1.1 3601b3583b8fa2c1ff5a4060892d24b2.cloudfront.net (CloudFront)
< x-amz-cf-pop: LIM50-P1
< x-amz-cf-id: c6rBv4T_aNadksGZuuEKR2is2wTKVOstzNHq7eu0OUPst46BpeIR7w==
< 
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* Connection #0 to host api.todoist.com left intact
Project not found