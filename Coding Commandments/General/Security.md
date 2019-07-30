*  Always use SSL (HTTPS) to serve dynamic content
*  It's better to host application and database server on separate machines. Do not allow internet access on database server.
*  Be careful while serializing user objects, e.g. when sending user data to client side. Make sure sensitive information e.g. password, credit card number information, etc is not getting serialized.
* Ensure data from input fields is getting validated on both frontend and backend. Use built-in frameworks (e.g. Spring in Java, Express with relevant modules in NodeJS) to avoid XSS and SQL injection attacks.   