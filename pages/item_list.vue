<template>
  <div>
    <h1>
      交換品一覧
    </h1>
    <div class="item_list">
      <dl>
        <input id="clothes_toggle" type="checkbox">
        <label for="clothes_toggle">
          <dt>
            服
          </dt>
        </label>
        <dd>
          <ul>
            <li>
              <img src="../static/fashion_tshirt1_white.png" alt="yuhayuhaのプリントTシャツ">
              <p>yuhayuhaのプリントTシャツ 50ポイント</p>
              <button>交換する</button>
            </li>
          </ul>
        </dd>
      </dl>
    </div>
  </div>
</template>

<style>
h1 {
  text-align: center;
}

img {
  width: 80%;
}

.item_list dl,
.item_list dt,
.item_list dd {
margin: 0;
padding: 0;
}

.item_list dl+dl {
margin-top: 1rem;
}

.item_list dt,
.item_list dd {
padding: 10px;
}

.item_list dl {
position: relative;
overflow: hidden;
}

.item_list dl>input {
display: none;
}

.item_list dt {
position: relative;
z-index: 1;
padding-right: 40px;
cursor: pointer;
background: #e6e6e6;
transition: .4;
border: solid 1px #adadad;
}

.item_list dd {
position: absolute;
visibility: hidden;
transform: translateY(-100%);
transition: .4s;
background: #f5f5f5;
border: solid 1px #adadad;
border-top: none;
}

.item_list dl>input:checked+label+dd {
position: relative;
visibility: visible;
transform: translateY(0);
}

.item_list dt::before {
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

.item_list dl>input:checked+label>dt::before {
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
p, button , label{
  font-size: 4.5vw;
}

</style>
