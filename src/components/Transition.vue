<template>
  <h1 class="text-center mb-4">Testing Animations on Vue Application</h1>
  <div>
    <button @click="show = !show">Toggle Me</button>

    <transition name="fade">
      <p v-if="show">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quos, nulla iure ducimus, tempora tempore culpa iusto possimus laudantium quam illo molestiae temporibus numquam, delectus neque minima dolorum! Mollitia, eius natus.
      </p>
    </transition>
  </div>

  <br>
  <br>
  <button @click="show1 = !show1">
    Toggle render
  </button>

  <transition name="slide-fade">
    <p v-if="show1">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Qui, fugiat eius expedita adipisci illo accusamus aliquam, illum, tenetur est officia eos voluptatum sit? Laborum, ad maiores. Obcaecati tempore voluptatum temporibus.
    </p>
  </transition>
  <br>
  <br>

   <button @click="show2 = !show2">Toggle show</button>
  <transition name="bounce">
    <p v-if="show2">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris facilisis
      enim libero, at lacinia diam fermentum id. Pellentesque habitant morbi
      tristique senectus et netus.
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores expedita officia fuga. Necessitatibus fugiat eum, nostrum veritatis repellat laborum exercitationem libero, quo animi, culpa illum velit delectus facilis beatae. Qui.
    </p>
  </transition>
<hr>
<br>
<br>
  <div id="list-demo">
  <button @click="add">Add</button>
  <button @click="remove">Remove</button>
  <transition-group name="list" tag="p">
    <span v-for="item in items" :key="item" class="list-item">
      {{ item }}
    </span>
  </transition-group>
</div>
</template>

<script>
export default {
  data() {
    return {
      show: true,
      show1:true,
      show2:true,
      items: [1, 2, 3, 4, 5, 6, 7, 8, 9],
      nextNum: 10
    };
  },
  methods: {
    randomIndex() {
      return Math.floor(Math.random() * this.items.length)
    },
    add() {
      this.items.splice(this.randomIndex(), 0, this.nextNum++)
    },
    remove() {
      this.items.splice(this.randomIndex(), 1)
    }
  }
};
</script>

<style scoped>
.list-item {
  display: inline-block;
  margin-right: 10px;
}
.list-enter-active,
.list-leave-active {
  transition: all 1s ease;
}
.list-enter-from,
.list-leave-to {
  opacity: 0;
  transform: translateY(30px);
}
.bounce-enter-active {
  animation: bounce-in 0.5s;
}
.bounce-leave-active {
  animation: bounce-in 0.5s reverse;
}
@keyframes bounce-in {
  0% {
    transform: scale(0);
  }
  50% {
    transform: scale(1.25);
  }
  100% {
    transform: scale(1);
  }
}

.slide-fade-enter-active {
  transition: all 0.3s ease-out;
}

.slide-fade-leave-active {
  transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-fade-enter-from,
.slide-fade-leave-to {
  transform: translateX(20px);
  opacity: 0;
}


.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
  color:blueviolet
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
