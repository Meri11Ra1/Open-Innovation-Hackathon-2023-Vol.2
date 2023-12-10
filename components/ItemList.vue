<template>
  <div>
    <div v-for="itemList in itemData" :key="itemList.id" class="item">
      <dl>
        <input id="toggle" type="checkbox">
        <label for="toggle">
          <dt>
            {{ itemList.listName }}
          </dt>
        </label>
        <dd v-for="items in itemList.items" :key="items.id">
          <ul>
            <li>
              <img :src="items.icon" />
              <p>{{ items.name }}</p>
              <button>交換する</button>
            </li>
          </ul>
        </dd>
      </dl>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    itemData: Object
  }
}
</script>

<style>
img {
  width: 80%;
}

.item dl,
.item dt,
.item dd {
margin: 0;
padding: 0;
}

.item dl+dl {
margin-top: 1rem;
}

.item dt,
.item dd {
padding: 10px;
}

.item dl {
position: relative;
overflow: hidden;
}

.item dl>input {
display: none;
}

.item dt {
position: relative;
z-index: 1;
padding-right: 40px;
cursor: pointer;
background: #e6e6e6;
transition: .4;
border: solid 1px #adadad;
}

.item dd {
position: absolute;
visibility: hidden;
transform: translateY(-100%);
transition: .4s;
background: #f5f5f5;
border: solid 1px #adadad;
border-top: none;
}

.item dl>input:checked+label+dd {
position: relative;
visibility: visible;
transform: translateY(0);
}

.item dt::before {
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

.item dl>input:checked+label>dt::before {
transform: translateY(-50%) rotate(180deg);
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
