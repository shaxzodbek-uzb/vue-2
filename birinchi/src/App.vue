<template>
  <div id="app">
    <p style="font-size: 20px;" class="qalin-text">Salom</p>
    <input type="text" v-model="surename" />
    <textarea cols="30" rows="10" v-model="desc"></textarea>

    <table>
      <tr>
        <td>1</td>
        <td>{{ full_name }}</td>
      </tr>
    </table>
    <NameComponent name="Jasurbek" :surename="surename" v-if="false" />
    <NameComponent name="Shaxzodbek" />
    <NameComponent v-bind:name="item" v-for="(item, index) in names" :key="index" />
    <hr />
    {{ desc }}
    <div v-text="desc"></div>
    <div v-html="desc"></div>
    <hr />
    <div v-if="son == 1">Bir</div>
    <div v-else>Ikki</div>
    <hr />
    <div v-if="son == 1">Bir</div>
    <div v-else-if="son == 2">Ikki</div>
    <div v-else-if="son == 3">Uch</div>
    <div v-else-if="son == 4">To'rt</div>
    <div v-else-if="son == 5">Besh</div>
    <div v-else>Bunday sonni bilmayman</div>
  </div>
</template>

<script>
// Bir komponentani boshqasi ichida ishlatish uchun
// 1. import qilish kerak
// 2. komponentani ro'yhatdan o'tkazish
// 3. o'z nomi bilan foydalanish tag ko'rishida
import NameComponent from "./components/Name";
export default {
  name: "AsosiyKomponenta",
  components: { NameComponent },
  props: {
    // parentdan keladigan atributlarni qabul qiladi
  },
  data() {
    // Componentaning reative o'zgaruvchilarini saqlash uchun
    return {
      name: "Shaxzodbek",
      surename: "Abdurasulov",
      names: ["Ibrohim", "Shahobiddin", "Anvar", "Dilshod"],
      desc: "",
      son: 7
    };
  },
  computed: {
    // boshqa ma'lumotlar o'zgarishiga qarab o'z qiymatini o'zgartiradi
    full_name() {
      return "Mr " + this.name;
    }
  },
  methods: {
    // komponentaga tegishli bo'lgan logik funksiyalar jamlanmasi
    qoshish(a, b) {
      return a + b;
    }
  }
};
</script>


<style>
/* istalgan css, sass, less... kodlarini kiritish mumkin */
.qalin-text {
  font-weight: bold;
}
</style>
