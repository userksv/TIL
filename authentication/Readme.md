Session Based Authentication
In the session based authentication, the server will create a session for the user after the user logs in. The session id is then stored on a cookie on the user’s browser. While the user stays logged in, the cookie would be sent along with every subsequent request. The server can then compare the session id stored on the cookie against the session information stored in the memory to verify user’s identity and sends response with the corresponding state!

/authentication/image.png

Token Based Authentication
Many web applications use token instead of sessions for authentication. In the token based application, the server creates token with a secret and sends the token to the client. The client stores the token (usually in local storage) and includes token in the header with every request. The server would then validate the token with every request from the client and sends the response.

![Getting Started](./authentication/image-1.png)

The biggest difference here is that the user’s state is not stored on the server, as the state is stored inside the token on the client side instead. Most of the modern web applications use JWT for authentication for reasons including scalability and mobile device authentication.

taken from https://stackoverflow.com/a/66085236
