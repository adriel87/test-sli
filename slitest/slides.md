---
theme: unicorn
logoHeader: ''
website: 'jotateam.dev'
handle: 'jotateam'
layout: intro
introImage: ''
---

# DentistApp

Tu solucion a las prisas detales
<!-- falta imagen del dientito -->

---
layout: cover
preload: false
---

# Que es ??

<v-click>

<div
  v-motion
  :initial="{ x: -80 }"
  :enter="{ x: 0 }">
  Una solucion para que las clinicas puedan gestionar de forma facil y rapida tanto urgencias como citas previas
  <br/>
  <br/>
  <br/>

</div>

</v-click>

## 
## 

<v-click>

## Formulario sencillo para urgencias <twemoji-face-screaming-in-fear /> 


</v-click>

<br/>
  <br/>
  <br/>

<v-click>

## Una cita previa sin complicaciones <twemoji-smiling-face-with-heart-eyes />


</v-click>

---
layout: table-contents
gradientColors: ['#8EC5FC', '#E0C3FC']
---

# Que vamos a ver ?? <twemoji-eyes />


<v-click>

pasos para construir la solucion

<br/>
<br/>

</v-click>


<v-click>

## En lo profundo del back <twemoji-octopus />
<br/>
<br/>

</v-click>

<v-click>

## Trabajando en el esqueleto <twemoji-skull />
<br/>
<br/>

</v-click>

<v-click>

## Vamos a ponernos guapis  <twemoji-lipstick />
<br/>
<br/>

</v-click>

<v-click>

## go to the moon <twemoji-rocket />
<br/>
<br/>

</v-click>

---

# El back-tender <twemoji-tropical-drink />


¿Por que <logos-javascript /> ?

<!-- principalmente para el aprendizaje , aunque a medida-->

como realizamos el acceso a datos con un ORM en JS

Diseñando modelos <twemoji-scissors />

sirviendo los datos 


---

# Express y sequelize

```ts
const express = require('express');
const { sequelize } = require('../app/models/index');
//middlewares
//rutas
server.listen(PORT , ()=> {
  console.log(`\n${'Servidor levantado en puerto'.bold} ${PORT.toString().green.bold}\n`);
    sequelize.sync({
    force:true,
  })
  .then(()=>{
    console.log(`\nconectado con ${process.env.TABLE_DATABASE}`);
  })
})
```

---

# sequelize

```ts
const sequelize = new Sequelize(options)
```
y como son las opciones
```ts
const options = {
  username: process.env.USERNAME_DATABASE,
  password: process.env.PASSWORD_DATABASE,
  database: process.env.TABLE_DATABASE,
  host: process.env.HOST_DATABASE,
  dialect: process.env.DIALECT_DATABASE,

  seederStorage:'sequelize',
  seederStorageTableName:'SequelizeSeeds',

  define:{
    timestamps: false,
    underscored: true,
  }
}
```

---

# Modelos

podemos crearlos manualmente <twemoji-keyboard />

o bien usando el CLI

```bash
npx sequelize-cli model:generate --name Teeth --attributes pieces:string
```
<br/>
de cualquier forma tendremos un archivo

que va a representar el objeto y sus relaciones en la base de datos

---

# Los pollitos del front <twemoji-hatching-chick />

Como enviar los datos <twemoji-open-mailbox-with-raised-flag />

```ts
//utilizamos el modelo
const { patient } =require('../models/index');
const PatientsController={};
//nos hacemos nuestras funciones CRUD
PatientsController.get = async(req, res) =>{
  patient.findAll()
  .then(patients=> res.status(200).json({
    ok:true,
    patients
  }))
  .catch(err=>res.status(500).json({
    ok:false,
    err
  }))
}
// todo lo que necesites hacer aqui y luego exporta
module.exports = PatientsController;
```
---

# ahora solo queda consumir
y como lo hacemos

## pues construyendo el front <twemoji-building-construction />

---

# Nestor  <logos-php />-MAN

---

# Laura our <logos-java /> DEV

---

# Abigail <logos-css3 /> Comander

