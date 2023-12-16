# all-React-Documentation

**Accessing environment var:**<br>
#in create-react-app:
<br>
These environment variables will be defined for you on process.env. For example, having an environment variable named <br><br>REACT_APP_NOT_SECRET_CODE<br><br> will be exposed in your JS as<br><br> process.env.REACT_APP_NOT_SECRET_CODE.<br><br>
<br>
https://create-react-app.dev/docs/adding-custom-environment-variables/
<br><br>

#in vite:
<br>
To prevent accidentally leaking env variables to the client, only variables prefixed with **VITE_** are exposed to your Vite-processed code. e.g. for the following env variables:


VITE_SOME_KEY=123<br>
DB_PASSWORD=foobar<br><br>
Only VITE_SOME_KEY will be exposed as<br>
<br>import.meta.env.VITE_SOME_KEY <br><br> to your client source code, but DB_PASSWORD will not.
<br>
https://vitejs.dev/guide/env-and-mode
<br>
<br>
** setting up appwrite **<br>
1) create new project <br>
2) create new database <br>
3) create new collectiom <br>
4) give permission in the collection's setting to read write or update and delete. <br>
5) create attributes. <br>
6) go to storage and create bucket <br>
7) Give permission in the bucket's setting.<br>
8) inside your src folder create a conf folder and create a conf file where you import and export all the env variables like:
   <br>
   ```
   const conf = {
    appwriteUrl : String(import.meta.VITE_APPWRITE_URL) ,
    appwriteProjectId : String(import.meta.VITE_APPWRITE_PROJECT_ID) ,
    appwriteDatabaseId : String(import.meta.VITE_APPWRITE_DATABASE_ID) ,
    appwriteCollectionId : String(import.meta.VITE_APPWRITE_COLLECTION_ID) ,
    appwriteBucketId : String(import.meta.VITE_APPWRITE_BUCKET_ID) 
     }
    export default conf
```
