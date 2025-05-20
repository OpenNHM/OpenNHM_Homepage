## Code for the AvaFrame homepage

To develop, use `hugo server -D`

To deploy: run `hugo`

then copy the files to our server on uberspace.de

`scp -r ./public/* avaframe@helin.uberspace.de:~/html/`

To add a new post:

- either look at content/post and edit with your favorite editor

- or use the provided decapCMS (from here https://decapcms.org/docs/working-with-a-local-git-repository/):
  
  - Run `npx decap-server` from the root directory of the  repository.
  - Start hugo with `hugo server -D`
  - Go to localhost:XXXX/admin 
  - Add new post 
  - the use the deploy from above
  - do not forget to commit the new post to git