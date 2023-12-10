<template>
  <div>
    <h1>
      交換品一覧
    </h1>
    <item-list :item-data="itemData" />
  </div>
</template>

<script>
export default {
  data () {
    return {
      itemData: [
        {
          id: 1,
          listName: 'clothes',
          items: [
            {
              id: 1,
              cost: 5,
              icon: require('../static/tshirt.png'),
              name: 'yuhayuhaのプリントTシャツ'
            },
            {
              id: 2,
              cost: 5,
              icon: require('../static/tshirt.png'),
              name: 'yuhayuhaのプリントTシャツ'
            }
          ]
        },
        {
          id: 2,
          listName: 'props',
          items: [
            {
              id: 1,
              cost: 5,
              icon: require('../static/tshirt.png'),
              name: 'yuhayuha'
            },
            {
              id: 2,
              cost: 5,
              icon: require('../static/tshirt.png'),
              name: 'yuhayuha'
            }
          ]
        }
      ]
    }
  }
}
</script>

<style>
h1 {
  text-align: center;
}

p, button , label{
  font-size: 4.5vw;
}

button {
  width: 50%;
  border: none;
  border-radius: 3vh;
  background-color: rgb(54, 155, 255);
  color: white;
  padding: 1.5vh;
}
</style>
