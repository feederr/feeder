# feeder

## How to clone?
`git clone --recurse-submodules https://github.com/feederr/feeder.git` 

## How to use dependencies from Github packages?
Add section to your _.m2/settings.xml_:
```xml
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

Add section to your pom.xml:

```xml
  <repositories>
    <repository>
      <id>github</id>
      <url>${link to github packages}</url>
    </repository>
  </repositories>
```

## How to build project?

Run `./mvnw clean package` from the root directory

## How to pull new modules locally in case they was added?

1. `git submodule update --init --recursive --remote`
2. `git submodule foreach --recursive git checkout master`

## Service -> port mapping

| service       | port |
|---------------|------|
| application   | 8081 |
| authorization | 8082 |
| statistics    | 8083 |

## Docker

* Run infrastructure instances via [following script](https://github.com/feederr/feeder-devtools/blob/master/run-infra.sh) 

* Stop infrastructure instances via [following script](https://github.com/feederr/feeder-devtools/blob/master/stop-infa.sh) 

* Run infrastructure and service instances via [following script](https://github.com/feederr/feeder-devtools/blob/master/docker-compose.services.yml)

* Stop infrastructure and service instances via [following script](https://github.com/feederr/feeder-devtools/blob/master/stop-all.sh)

* Build images using via [following script](https://github.com/feederr/feeder-devtools/blob/master/rebuild-all.sh)

> Docker hub account is configured for this organization, so you can pull images using `:latest` tag directly from remote registry. 
> They will have format: `feederr/{service name}:{version}`

## Useful Intellij Idea plugin to work with umbrella repo

* GitToolBox

## If you want to contribute
* use [appropriate](https://github.com/feederr/feeder/blob/master/google-code-style.xml) code style
