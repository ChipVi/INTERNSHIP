<template>
    <transition :name="direction" mode="out-in">
      <div v-if="visibleimg === index" class="imgcontainer">
        <img :src="srcp" />
      </div>
    </transition>
  </template>
  
  <script>
  export default {
    props: ['index', 'visibleimg', 'direction', 'srcp'],
  };
  </script>
  
  <style scoped>
  .left-enter-active,
  .left-leave-active,
  .right-enter-active,
  .right-leave-active {
    width: 100%;
    height: 100%;
  }
  
  .left-enter-active,
  .left-leave-active,
  .right-enter-active,
  .right-leave-active {
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    top: 0;
  }
  
  .left-enter-active {
    animation: leftAnimation 1s ease-in-out;
  }
  .left-leave-active {
    animation: leftOutAnimation 1s ease-in-out;
  }
  @keyframes leftAnimation {
    from {
      transform: translateX(100%);
    }
    to {
      transform: translateX(0);
    }
  }
  @keyframes leftOutAnimation {
    from {
      transform: translateX(0);
    }
    to {
      transform: translateX(-100%);
    }
  }
  
  .right-enter-active {
    animation: rightAnimation 1s ease-in-out;
  }
  .right-leave-active {
    animation: rightOutAnimation 1s ease-in-out;
  }
  @keyframes rightAnimation {
    from {
      transform: translateX(-100%);
    }
    to {
      transform: translateX(0);
    }
  }
  @keyframes rightOutAnimation {
    from {
      transform: translateX(0);
    }
    to {
      transform: translateX(100%);
    }
  }
  .imgcontainer {
    width: 100%;
    height: 250px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  </style>