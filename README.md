# ES-Operation

## access ES
in order to get access to ES cluster, a url of the following format is essential:

  >url = host + '/' + index + '/' + type
  
  >host = 'https://search-jan2-jsuwsxlwenpntew53nwxoz74gy.us-west-2.es.amazonaws.com' # for instance
  >index = 'lambda-s3-index' #for instance
  >type = '_doc'
    
  >headers = { "Content-Type": "application/json" }
