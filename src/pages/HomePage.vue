<template>
  <v-container>
    <div>Home Page</div>
    <stack :column-min-width="200" :gutter-width="10" :gutter-height="8">
      <stack-item v-for="(item, i) in items" :key="i">
        <image-card
          :url="item.url"
          :meta="{
            name: item.name,
            occupation: item.occupation,
            profileImageUrl: item.profileImageUrl,
          }"
        />
      </stack-item>
    </stack>
  </v-container>
</template>

<script>
import { Stack, StackItem } from "vue-stack-grid";
import ImageCard from "../components/ImageCard";

export default {
    components:{Stack, StackItem, ImageCard},
  data() {
    return {
      items: [
        {
          url: "https://images.unsplash.com/photo-1544735716-392fe2489ffa?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Mnx8bmVwYWx8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Felipe Gomes",
          occupation: "Developer",
          profileImageUrl:
            "https://images.unsplash.com/photo-1610024062303-e355e94c7a8c?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=634&q=80",
        },
        {
          url: "https://images.unsplash.com/photo-1554710869-95f3df6a3197?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NHx8bmVwYWx8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "João Gomes Sena",
          occupation: "Developer",
          profileImageUrl:
            "https://images.unsplash.com/photo-1470259078422-826894b933aa?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1053&q=80",
        },
        {
          url: "https://images.unsplash.com/photo-1543860856-79e478a9452b?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTF8fG5lcGFsfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Matheus Lima (O rei)",
          occupation: "CTO",
          profileImageUrl:
            "https://images.unsplash.com/photo-1474511019749-26a5a4b632b2?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1052&q=80",
        },
        {
          url: "https://images.unsplash.com/photo-1523512090443-2d7df8b40358?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=634&q=80",
          name: "Matheus Felipe (O Principe)",
          occupation: "Tech lead",
          profileImageUrl:
            "https://images.unsplash.com/photo-1505033575518-a36ea2ef75ae?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjJ8fHByb2ZpbGUlMjBpbWFnZXxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1551088701-77512773d322?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjB8fG5lcGFsfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Tales Coelho",
          occupation: "Infra",
          profileImageUrl:
            "https://images.unsplash.com/photo-1505033575518-a36ea2ef75ae?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjJ8fHByb2ZpbGUlMjBpbWFnZXxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1544735716-392fe2489ffa?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Mnx8bmVwYWx8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Mateus Freitas",
          occupation: "Developer",
          profileImageUrl:
            "https://images.unsplash.com/photo-1505033575518-a36ea2ef75ae?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjJ8fHByb2ZpbGUlMjBpbWFnZXxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1546005035-1c047504a71a?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjZ8fG5lcGFsfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Brenda",
          occupation: "Doceira",
          profileImageUrl:
            "https://images.unsplash.com/photo-1525550557089-27c1bfedd06c?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjN8fHByb2ZpbGUlMjBpbWFnZXxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1553521756-74004ab1e8bd?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
          name: "Manu",
          occupation: "Rico",
          profileImageUrl:
            "https://images.unsplash.com/photo-1522075469751-3a6694fb2f61?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjF8fHByb2ZpbGUlMjBpbWFnZXxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1567761653114-6b6eb3101c79?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Mjh8fG5lcGFsfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Malaquias ",
          occupation: "Minerador",
          profileImageUrl:
            "https://images.unsplash.com/photo-1531427186611-ecfd6d936c79?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjV8fHByb2ZpbGUlMjBpbWFnZXxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
      ],
    };
  },
};
</script>

<style>
</style>