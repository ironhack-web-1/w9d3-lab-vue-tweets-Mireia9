<template>
    <div>
        <span className="user">
          <span className="name">{{ name }}</span>
          <span className="handle">@{{ handle }}</span>
        </span>
    </div>
  </template>
  
  <script>
  

  export default {
    props: ["name", "handle" ],
  };
  </script>