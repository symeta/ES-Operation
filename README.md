# ES-Operation

## access ES
* in order to get access to ES cluster, a url of the following format is essential:

  >url = host + '/' + index + '/' + type
  
  >host = 'https://example.com' # for instance
  
  >index = 'index_1' #for instance
  
  >type = '_doc'
    
  >headers = { "Content-Type": "application/json" }

* make sure that an index named 'index_1' is created in ES.

## Dev Tools operation
* create index
`PUT f_9
{
  "mappings": {
    "properties": {
      "time_local":{
        "format": "dd/MMM/yyyy:HH:mm:ss Z||epoch_millis",
        "type": "date"
      }
    }
  }
}`