miguel@malconb-vd04:~$ curl -X DELETE "https://api.todoist.com/rest/v2/projects/" -H "Authorization: Bearer $mytoken" -v
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
* Using Stream ID: 1 (easy handle 0x55f33847deb0)
* TLSv1.2 (OUT), TLS header, Supplemental data (23):
> DELETE /rest/v2/projects/ HTTP/2
> Host: api.todoist.com
> user-agent: curl/7.81.0
> accept: */*
> authorization: Bearer XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
> 
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* TLSv1.3 (IN), TLS handshake, Newsession Ticket (4):
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* Connection state changed (MAX_CONCURRENT_STREAMS == 128)!
* TLSv1.2 (OUT), TLS header, Supplemental data (23):
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* TLSv1.2 (IN), TLS header, Supplemental data (23):
< HTTP/2 405 
< content-type: application/json
< content-length: 173
< date: Mon, 11 Mar 2024 19:16:41 GMT
< cache-control: no-cache
< referrer-policy: strict-origin-when-cross-origin
< retry-after: 3
< server: gunicorn
< set-cookie: todoistd="/CUdA09psYiwY7pwgn9sRGC/RQQ=?"; Domain=.todoist.com; Expires=Tue, 11-Mar-2025 19:16:41 GMT; Max-Age=31536000; Secure; HttpOnly; Path=/; SameSite=None
< strict-transport-security: max-age=31536000; includeSubDomains; preload
< vary: Accept-Encoding
< x-cache: Error from cloudfront
< via: 1.1 ba321a618e817037ce8e0d09e9005b46.cloudfront.net (CloudFront)
< x-amz-cf-pop: LIM50-P1
< x-amz-cf-id: ZUu_1vJdRTF5Xg1lfdY2P_GNJB2O5UWZuWiqtxu0Ptpf3K42VrGt-A==
< 
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* Connection #0 to host api.todoist.com left intact
{"error":"Method Not Allowed","error_code":62,"error_extra":{"event_id":"d93ea0fc7a7b44fabc40ea80d2b120a9","retry_after":3},"error_tag":"METHOD_NOT_ALLOWED","http_code":405}