miguel@malconb-vd04:~$ curl -X GET https://api.todoist.com/rest/v2/projects -H "Authorization: Bearer $mytoken" -v
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
* Using Stream ID: 1 (easy handle 0x5649734d6eb0)
* TLSv1.2 (OUT), TLS header, Supplemental data (23):
> GET /rest/v2/projects HTTP/2
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
< HTTP/2 200 
< content-type: application/json
< content-length: 640
< date: Mon, 11 Mar 2024 16:27:45 GMT
< access-control-allow-credentials: false
< access-control-allow-origin: *
< referrer-policy: strict-origin-when-cross-origin
< server: gunicorn
< set-cookie: csrf=6a11c72d23674eae8638312d425fe66b; Expires=Thu, 09-Mar-2034 16:27:44 GMT; Secure; Path=/; SameSite=None
< set-cookie: tduser=v4.public.eyJ1c2VyX2lkIjogNDg1MzY5NjgsICJleHAiOiAiMjAyNC0wMy0yNVQxNjoyNzo0NCswMDowMCJ9OPfaa40eCMrqSAntqgKq5hkZeh8v4HJ9jfQ_T9p1HA9rsD31ofdx3T2uDyxAVPQOO0xJE4Wm8g6beR7L_SQUCg; Domain=.todoist.com; Expires=Mon, 25-Mar-2024 16:27:44 GMT; Max-Age=1209600; Secure; HttpOnly; Path=/
< set-cookie: todoistd="/CUdA09psYiwY7pwgn9sRGC/RQQ=?"; Domain=.todoist.com; Expires=Tue, 11-Mar-2025 16:27:45 GMT; Max-Age=31536000; Secure; HttpOnly; Path=/; SameSite=None
< strict-transport-security: max-age=31536000; includeSubDomains; preload
< vary: Accept-Encoding
< x-cache: Miss from cloudfront
< via: 1.1 672a274f5830cff711168a1debfae76c.cloudfront.net (CloudFront)
< x-amz-cf-pop: LIM50-P1
< x-amz-cf-id: sdUrJnXaZYJG2zxre6tm-geipmQNiXTd-OdrQNKcw2DZMKNQ9skIxA==
< 
[
	{
		"id": "2330045591",
		"parent_id": null,
		"order": 0,
		"color": "charcoal",
		"name": "Inbox",
		"comment_count": 0,
		"is_shared": false,
		"is_favorite": false,
		"is_inbox_project": true,
		"is_team_inbox": false,
		"url": "https://todoist.com/showProject?id=2330045591",
		"view_style": "list"
	},
	{
		"id": "2330047932",
		"parent_id": null,
		"order": 2,
		"color": "charcoal",
		"name": "Example for CRUD update",
		"comment_count": 0,
		"is_shared": false,
		"is_favorite": false,
		"is_inbox_project": false,
		"is_team_inbox": false,
		"url": "https://todoist.com/showProject?id=2330047932",
		"view_style": "list"
	}
]
* TLSv1.2 (IN), TLS header, Supplemental data (23):
* Connection #0 to host api.todoist.com left intact
