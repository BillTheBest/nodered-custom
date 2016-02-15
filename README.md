# Node-RED

http://nodered.org

## Custom changes

red/api/theme.js

function serveFile(app,baseUrl,file) {

  try {
    var url = baseUrl+path.basename(file);
    //console.log(url,"->",file);
    app.get(url,function(req, res) {
      res.sendFile(file);
    });
    return "../public"+url;
  } catch(err) {
    //TODO: log filenotfound
    return null;
  }
}

## Authors

Node-RED is a creation of [IBM Emerging Technology](http://ibm.com/blogs/et).

* Nick O'Leary [@knolleary](http://twitter.com/knolleary)
* Dave Conway-Jones [@ceejay](http://twitter.com/ceejay)

For more open-source projects from IBM, head over [here](http://ibm.github.io).

## Copyright and license

Copyright 2013, 2015 IBM Corp. under [the Apache 2.0 license](LICENSE).
