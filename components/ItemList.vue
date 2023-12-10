<template>
  <div>
    <div class="header">
      <div class="header-text">
        <NuxtLink to="/my_page">
          <img src="@/assets/arrow-left.svg" class="back-img">
        </NuxtLink>
      </div>
      <p class="possession">保有pt: {{ userPoint }}</p>
    </div>
    <div>
      <div v-for="itemList in itemData" :key="itemList.id" class="item_data">
        <dl>
          <input :id="itemList.id" type="checkbox">
          <label :for="itemList.id">
            <dt>
              {{ itemList.listName }}
            </dt>
          </label>
          <dd>
            <div v-for="items in itemList.items" :key="items.id" class="items">
              <ul>
                <li>
                  <img :src="items.icon" />
                  <p>{{ items.name + ' ' + items.cost + 'pt'}}</p>
                  <button @click="confirmExchange(items)">交換する</button>
                </li>
              </ul>
            </div>
          </dd>
        </dl>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    itemData: Array,
    point: Number
  },
  data () {
    return {
      userPoint: this.point
    }
  },
  methods: {
    confirmExchange (items) {
      this.userPoint -= items.cost
      alert(items.name + 'を交換しました')
      console.log(this.userPoint)
    }
  }
}
</script>

<style scoped>
img {
  width: 80%;
}
.possession {
  margin-left: 50vw;
}

.header {
  display: flex;
  align-items: center;
  justify-content: left;

  height: 40px;
  padding: 4px 8px;

  width: 100%;
  margin-left: -8px;
  margin-top: -8px;
  margin-bottom: 15px;

  box-shadow: 0px 2px 6px 0px rgba(0, 0, 0, 0.15);
}

.back-img {
  margin-top: 7px;
  margin-left: 5.6vw;
  height: 40px;
  width: 10vw;
}

.item_data dl,
.item_data dt,
.item_data dd {
margin: 0;
padding: 0;
}

.item_data dl+dl {
margin-top: 1rem;
}

.item_data dt,
.item_data dd {
padding: 10px;
}

.item_data dl {
position: relative;
overflow: hidden;
}

.item_data dl>input {
display: none;
}

.item_data dt {
position: relative;
z-index: 1;
padding-right: 40px;
cursor: pointer;
background: #e6e6e6;
transition: .4;
border: solid 1px #adadad;
}

.item_data dd {
position: absolute;
visibility: hidden;
transform: translateY(-100%);
transition: .4s;
background: #f5f5f5;
border: solid 1px #adadad;
border-top: none;
}

.item_data dl>input:checked+label+dd {
position: relative;
visibility: visible;
transform: translateY(0);
}

.item_data dt::before {
content: ”;
position: absolute;
top: 50%;
right: 10px;
border-style: solid;
border-width: 17.3px 10px 0 10px;
border-color: #666 transparent transparent transparent;
transform: translateY(-50%);
transition: .4s;
}

.item_data dl>input:checked+label>dt::before {
transform: translateY(-50%) rotate(180deg);
}

.items {
  margin-top: 2vh;
}

ul {
  all: unset;
}

li {
  all: unset;
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
}
</style>
