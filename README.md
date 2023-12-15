# all-React-Documentation

**Accessing environment var:**<br>
#in create-react-app:
<br>
These environment variables will be defined for you on process.env. For example, having an environment variable named REACT_APP_NOT_SECRET_CODE will be exposed in your JS as process.env.REACT_APP_NOT_SECRET_CODE.
<br>
#in vite:
<br>
To prevent accidentally leaking env variables to the client, only variables prefixed with VITE_ are exposed to your Vite-processed code. e.g. for the following env variables:


VITE_SOME_KEY=123
DB_PASSWORD=foobar
Only VITE_SOME_KEY will be exposed as import.meta.env.VITE_SOME_KEY to your client source code, but DB_PASSWORD will not.
