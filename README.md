# OpenAPI-Specification
OpenAPI 3.0 specification 

OpenAPI 3.0 is *NOT* backward compatibility OpenAPI 2.0 is not usable

#### Documentation link
https://swagger.io/specification/

#### Viewable UI link (not usable)

https://editor.swagger.io/?url=https://raw.githubusercontent.com/NardoLee3/OpenAPI-Specification/main/demo.yaml

## OpenAPI 3.0 Specification to Postman Collection
### Install openapi-to-postmanv2

```
npm install -g openapi-to-postmanv2
```

### run command line

```
openapi2postmanv2 -s demo.yaml -o collection.json -p -O folderStrategy=Tags,includeAuthInfoInExample=false
```


## Starting Mock Server
### Creating Config File
The config file must named followed by `-config.yaml`

### run command line
```
docker run -ti -p 8080:8080 \
    -v $(pwd):/opt/imposter/config \
    outofcoffee/imposter-rest
```

#### View UI page
http:localhost:8080/_spec/
