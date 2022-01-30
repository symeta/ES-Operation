# ES-Operation

## access ES
* in order to get access to ES cluster, a url of the following format is essential:
```
  url = host + '/' + index + '/' + type
  host = 'https://example.com' # for instance
  index = 'index_1' #for instance
  type = '_doc'
  headers = { "Content-Type": "application/json" }
```
* make sure that an index named 'index_1' is created in ES.

## Dev Tools operation
* create index
```
PUT index_1
{
  "mappings": {
    "properties": {
      "timestamp":{
        "type": "date",
        "format": "dd/MMM/yyyy:HH:mm:ss Z||epoch_millis"
      }
    }
  }
}
```
27/Jan/2022:15:26:09 +0800

* get index meta info
```
get index_1
```
* get index records info
```
get index_1/_search
```
* put a record into index
```
put index_1/_doc/1?pretty
{
  "timestamp":"26/01/2022:15:26:09 +0800"
}
```
