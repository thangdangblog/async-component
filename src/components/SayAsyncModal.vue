<template>
    <div class="modal">
      <div class="modal-content">
        <p>Hi Async Modal</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'SayAsyncModal',
  }
  </script>
  
  <style scoped>
  .modal {
    position: fixed; 
    z-index: 1; 
    left: 0;
    top: 0;
    width: 100%; 
    height: 100%; 
    overflow: auto; 
    background-color: rgba(0,0,0,0.4); 
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  .modal-content {
    background-color: #f94e4e;
    margin: 15% auto; 
    padding: 20px;
    border: 1px solid #888;
    width: 80%;
    max-width: 600px;
    color: white;
    
  }
  
  .close-button {
    color: #aaa;
    float: right;
    font-size: 28px;
    font-weight: bold;
  }
  
  .close-button:hover,
  .close-button:focus {
    color: black;
    text-decoration: none;
    cursor: pointer;
  }
  </style>