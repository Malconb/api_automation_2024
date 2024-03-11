curl -X GET https://api.todoist.com/rest/v2/projects/23300594601 -H "Authorization: Bearer $mytoken" -v
Note: Unnecessary use of -X or --request, GET is already inferred.
*   Trying 108.158.104.61:443...
* Connected to api.todoist.com (108.158.104.61) port 443 (#0)
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
* Using Stream ID: 1 (easy handle 0x5585851d0eb0)
* TLSv1.2 (OUT), TLS header, Supplemental data (23):
> GET /rest/v2/projects/23300594601 HTTP/2
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
< HTTP/2 404 
< content-type: text/plain; charset=utf-8
< content-length: 17
< date: Mon, 11 Mar 2024 17:16:15 GMT
< access-control-allow-credentials: false
< access-control-allow-origin: *
< referrer-policy: strict-origin-when-cross-origin
< server: gunicorn
< set-cookie: csrf=f143e76742004b2783ef52a0f1cdac79; Expires=Thu, 09-Mar-2034 17:16:15 GMT; Secure; Path=/; SameSite=None
< set-cookie: tduser=v4.public.eyJ1c2VyX2lkIjogNDg1MzY5NjgsICJleHAiOiAiMjAyNC0wMy0yNVQxNzoxNjoxNSswMDowMCJ9tkoAUVU4EbNUeRBKVa9ing6PRu2I-ywdy0yaS4CU0GnoYnr3SB_zeq4cqdSoVF_tOHZNiEB8hsxMOKJpVKOzAg; Domain=.todoist.com; Expires=Mon, 25-Mar-2024 17:16:15 GMT; Max-Age=1209600; Secure; HttpOnly; Path=/
< set-cookie: todoistd="/CUdA09psYiwY7pwgn9sRGC/RQQ=?"; Domain=.todoist.com; Expires=Tue, 11-Mar-2025 17:16:15 GMT; Max-Age=31536000; Secure; HttpOnly; Path=/; SameSite=None
< strict-transport-security: max-age=31536000; includeSubDomains; preload
< vary: Accept-Encoding
< x-cache: Error from cloudfront
< via: 1.1 e9ca790c177fd72d240e2c2ced6f13ae.cloudfront.net (CloudFront)
< x-amz-cf-pop: LIM50-P1
< x-amz-cf-id: XZqJnFv-v1Al6h1q3rDqMRQUFwMrbM3NzSNKGU0IZqAfHYNojZd_dA==
< 
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* Connection #0 to host api.todoist.com left intact
Project not found