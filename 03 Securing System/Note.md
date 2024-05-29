# Securing System
## Encription
## Wi-Fi
the traffic, any of the internet packet, information must be encrypted. this is what we call encrypted network.

## WPA (Wi-Fi protected access)
this is the encrypted version of Wi-Fi.

## HTTP
Nazu <--> Eve <--> Bob
if you search http://...com the packet that are send from your browesr to the server just only using "http".. this is not secure.. every thing is sent in plain so that Eve can steal everything that nazu send it to bob. this is what we call MITM attack.


so when you visit a website.. you are downling some frontend codes..such as js, html and css codes.
```html
<html>
    ...
    <body>
        ...
    </body>
    ...
</html>
```

so if we are using normal plain http.. so the attacker in our case eve can inject another evil html code that can preform evil shit.. maybe staeling our cookies, password and so on...
```html
<!DOCTYPE html>
<html lang="en">
<body>
    <p>Hey</p>
    <script src="evil.js"></script>
</body>
</html>
```

## Packet sniffing
well it is just sniffing the packets that are transationing.

for example look this:
```http
GET /search?q=cats HTTP/3
Host: exmaple.com
```
a browser requesting a server using search funtionality a query "cats".. if some can sniff this.. he can see your request.

```http
POST /checkout HTTP/3
Host: exmaple.com

private_code=12123u01293
```
what if you are doing and get sniffed? well that is critical.

## Cookies
a data about your prifrence, settings and so on.. that can be stored on your PC.
for example
```http
GET / HTTP/3
Cookie: session=1234abcd
```
### Session Hijacking
if you are not using encryption which is https.. therefore your cookie session is visble to anyone.. which is crticla.

ohh nazu's session cookie is "1234abcd" lets copy it and send to trick the servr that I'm nazu.. book!! so they logged with my account without knowing my password and username but just by using session cookie.

## HTTPS
to solve these all grabage.. we need to use HTTPS.. with secure..
so now there is no eve/attacker .. we talk end-to-end
`Nazu <--> Bob`

## TLS
so https use TLS inorder to do this..
## Certficte
What does thoese do?? they just use public key cryptography, using public and private key.. they establish secured connection.

## X.509
## CA

AND SO ON....