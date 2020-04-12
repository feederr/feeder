# feeder

## How to clone?
`git clone --recurse-submodules https://github.com/feederr/feeder.git` 

## How to use dependencies from Github packages?
Add section to you _.m2/settings.xml_:
```
   <servers>
     <server>
       <id>github</id>
       <username>${username}</username>
       <password>${password}</password>
     </server>
   </servers>
```
* username is your github username;
* password is your token that could be generated [there](https://github.com/settings/tokens);
