# Rrvis-o_Node.JS
Revisão de consceitos de Node.js

```

const fs = require('fs')


const palavra = 'arquitetura'
const arquivo = './arquivo.txt'

console.time('tempo')


fs.readFile(arquivo, 'utf8', (err, data) => {
  if(err){
    console.log('Erro ao abrir o arquivo', err.message)
    return err
  }
  
  
  if(data.includes(palavra)){
    console.log(`A palavra ${palavra} foi encontrada no arquivo`)
  }else{
    console.log(`A palavra ${palavra} não foi encontrada no arquivo`)
  }
  
  const inteiras = new RegExp(`\\b${palavra}\\b`, 'gi');
  const ocorrencias = (data.match(inteiras) || []).length;
  const total = data.length;
  
  "use strict";
  
  const myBuffer = new Buffer(data)
  const slic = myBuffer.slice(6, 10)
  const json = JSON.stringify(myBuffer)
  const buff2 = new Buffer(JSON.parse(json).data)
  
  
  console.log(`A palavrea ${palavra} aparece ${ocorrencias} vezes e tem ${total} palavras, ${buff2}`)
  
  console.timeEnd('tempo')
})


Object.keys(global).forEach((value) => {
  console.log(value)
})


```
