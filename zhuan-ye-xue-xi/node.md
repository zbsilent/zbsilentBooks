# Node

[![github](https://raw.githubusercontent.com/zbsilent/imag/main/rootgithubb.svg)![](https://img.shields.io/badge/React-zbsilent-brightgreen)](https://github.com/zbsilent)

```javascript
/*app.js*/
const express = require('express');
const server = express();

server.listen(2812);

server.use('/get',(req,res)=>{
  res.send(['china','japan','ruishi'])
})

server.use(express.static('./'))
```

```bash
node app.js
```

