h2. quick-ftp

quick-ftp is a very simple  wrapper for pyftpdlib that provides the user with a ready-to-use
FTP server for testing and experiments.

h2. Usage

```javascript
var Server = require('quick-ftp');

var myFtp = new Server();

myFtp.on('stdout', function(data) {
  console.log(data);
});

myFtp.on('stderr', function(data) {
  console.log('ERROR', data);
})

myFtp.init({
  user: "sergi",
  pass: "1234",
  port: "3334"
});
```