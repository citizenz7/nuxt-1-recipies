<!--
<template>
  <main>
    <section class="container py-10">
      <h1 class="text-3xl font-extrabold mb-6 text-balance border-b text-center">Nous contacter</h1>
      <div class="bg-white dark:bg-gray-900">
        <div class="px-4 mx-auto max-w-screen-md">
          <p class="mb-8 lg:mb-16 font-light text-center text-gray-500 dark:text-gray-400 sm:text-l">
            Vous avez un problème technique ?<br>
            Vous souhaitez nous faire part de vos commentaires sur une fonctionnalité bêta ?<br>
            Vous avez besoin de détails sur notre forfait Business ?<br>
            Faites-le nous savoir.
          </p>
          <form action="#" class="space-y-8">
            <div>
              <label for="email" class="block mb-2 text-sm font-medium text-gray-900 dark:text-gray-300">Votre adresse e-mail</label>
              <input type="email" id="email"
                class="shadow-sm bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-primary-500 focus:border-primary-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-primary-500 dark:focus:border-primary-500 dark:shadow-sm-light" placeholder="monnom@gmail.com" required>
            </div>
            <div>
              <label for="subject"
                class="block mb-2 text-sm font-medium text-gray-900 dark:text-gray-300">Sujet</label>
              <input type="text" id="subject"
                class="block p-3 w-full text-sm text-gray-900 bg-gray-50 rounded-lg border border-gray-300 shadow-sm focus:ring-primary-500 focus:border-primary-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-primary-500 dark:focus:border-primary-500 dark:shadow-sm-light" placeholder="Dites-nous comment nous pouvons vous aider" required>
            </div>
            <div class="sm:col-span-2">
              <label for="message" class="block mb-2 text-sm font-medium text-gray-900 dark:text-gray-400">Votre message</label>
              <textarea id="message" rows="6" class="block p-2.5 w-full text-sm text-gray-900 bg-gray-50 rounded-lg shadow-sm border border-gray-300 focus:ring-primary-500 focus:border-primary-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-primary-500 dark:focus:border-primary-500"
                placeholder="Ecrivez votre message"></textarea>
            </div>
            <button type='button' class="text-white bg-blue-500 hover:bg-blue-600 tracking-wide rounded-md text-sm px-4 py-3 w-full">Envyoyer le message</button>
          </form>
        </div>
      </div>
    </section>
  </main>
</template>
-->

<template>
  <main>
    <section class="container py-10">
      <h1 class="text-3xl font-extrabold mb-6 text-balance border-b text-center">Nous contacter</h1>
      <p class="mb-8 lg:mb-16 font-light text-center text-gray-500 dark:text-gray-400 sm:text-l">
        Vous avez un problème technique ?<br>
        Vous souhaitez nous faire part de vos commentaires sur une fonctionnalité bêta ?<br>
        Vous avez besoin de détails sur notre forfait Business ?<br>
        Faites-le nous savoir.
      </p>
      <form
        accept-charset="UTF-8"
        v-on:submit.prevent="onSubmit()"
        method="POST"
        class="space-y-8"
      >
        <div class="px-4 mx-auto max-w-screen-md">
          <label class="block mb-2 text-sm font-medium text-gray-900 dark:text-gray-300">E-mail</label>
          <input type="email" v-model="email" class="shadow-sm bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-primary-500 focus:border-primary-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-primary-500 dark:focus:border-primary-500 dark:shadow-sm-light" placeholder="Entrez votre adresse e-mail" required="required">
        </div>
        <div class="px-4 mx-auto max-w-screen-md">
          <label class="block mb-2 text-sm font-medium text-gray-900 dark:text-gray-300">Nom</label>
          <input type="text" v-model="name" class="block p-3 w-full text-sm text-gray-900 bg-gray-50 rounded-lg border border-gray-300 shadow-sm focus:ring-primary-500 focus:border-primary-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-primary-500 dark:focus:border-primary-500 dark:shadow-sm-light" placeholder="Entrez votre nom complet" required="required">
        </div>

        <div class="px-4 mx-auto max-w-screen-md">
          <label class="block mb-2 text-sm font-medium text-gray-900 dark:text-gray-300">Sujet</label>
          <input type="text" v-model="subject" class="block p-3 w-full text-sm text-gray-900 bg-gray-50 rounded-lg border border-gray-300 shadow-sm focus:ring-primary-500 focus:border-primary-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-primary-500 dark:focus:border-primary-500 dark:shadow-sm-light" placeholder="Entrez le sujet de votre message" required="required">
        </div>

        <div class="px-4 mx-auto max-w-screen-md">
          <label class="block mb-2 text-sm font-medium text-gray-900 dark:text-gray-400">Message</label>
          <textarea type="text" v-model="message" rows="6" class="block p-2.5 w-full text-sm text-gray-900 bg-gray-50 rounded-lg shadow-sm border border-gray-300 focus:ring-primary-500 focus:border-primary-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-primary-500 dark:focus:border-primary-500" placeholder="Entrez votre message" required="required"></textarea>
        </div>
        <div class="px-4 mx-auto max-w-screen-md text-center text-green-800 font-extrabold text-1xl" v-if="isSuccess">Le message à bien été envoyé !</div>
        <div class="px-4 mx-auto max-w-screen-md">
          <button type="submit" class="text-white bg-blue-500 hover:bg-blue-600 tracking-wide rounded-md text-sm px-4 py-3 w-full">Envoyer le message</button>
        </div>
      </form>
    </section>
  </main>
</template>

<script>
import axios from "axios";

export default {
  name: "Contact",
  props: {
    msg: String
  },
  data() {
    return {
      loading: true,
      name: "",
      email: "",
      subject: "",
      message: "",
      isSuccess: false
    };
  },
  methods: {
    onSubmit() {
      let data = {
        name: this.name,
        email: this.email,
        subject: this.subject,
        message: this.message
      };
      axios
        .post("https://getform.io/f/awnnykyb", data, {
          headers: {
            Accept: "application/json"
          }
        })
        .then(
          response => {
            this.isSuccess = response.data.success ? true : false;
          },
          response => {
            // Error
          }
        );
    }
  }
};
</script>
