# CRLF-Payloads

Here are some examples of how to use CRLF injection payloads:

* **Normal payloads:**
    * %0D%0A
    * \r\n
    * \n
    * %0A
    * \r
    * %0D

These payloads can be used to inject a newline character into a web request, which can then be used to bypass certain security controls. For example, a CRLF injection payload could be used to bypass a web application firewall (WAF) that is configured to block requests that contain newline characters.

* **WAF bypass payloads:**
    * %250D%250A
    * %250A
    * %250D
    * %25250D%25250A
    * %25250A
    * %25250D

These payloads can be used to bypass WAFs that are configured to block requests that contain certain characters, such as newline characters. For example, a WAF bypass payload could be used to inject a newline character into a web request, even if the WAF is configured to block requests that contain newline characters.

To use a CRLF injection payload, you can simply add the payload to the end of a web request. For example, if you are making a request to the URL `http://example.com/index.php`, you could add the payload `%0D%0A` to the end of the URL, like this:

`http://example.com/index.php%0D%0A`

When the web server receives the request, it will interpret the payload as a newline character and process the request accordingly. This could allow you to bypass certain security controls, such as WAFs.

To use a CRLF injection payload in the body of a web request, you can simply add the payload to the body of the request. For example, if you are making a POST request to the URL http://example.com/index.php, you could add the payload %0D%0A to the body of the request, like this:

--------
POST /index.php HTTP/1.1                
Host: example.com                 
Content-Type: application/x-www-form-urlencoded         

username=admin&password=password%0D%0A

--------

When the web server receives the request, it will interpret the payload as a newline character and process the request accordingly. This could allow you to bypass certain security controls, such as WAFs.

In this case, the attacker has injected a newline character into the password field of the login form. This will cause the web server to interpret the password as two separate values, "password" and "%0D%0A". This could allow the attacker to bypass the password authentication and gain access to the web server.
