<script setup lang="ts">
useSeoMeta({
    title: "RecettesAMoi",
    description: "Des recettes à cuisiner !",
    ogTitle: "RecettesAMoi",
    ogDescription: "Des recettes à cuisiner !",
    ogImage: "/nuxt-course-hero.png",
    ogUrl: `http:localhost:3000`,
    twitterTitle: "RecettesAMoi",
    twitterDescription: "Des recettes à cuisiner !",
    twitterImage: "nuxt-course-hero.png",
    twitterCard: "summary",
});
</script>

<template>
  <main>
    <section class="container py-10">
      <h1 class="text-3xl font-extrabold mb-6 text-balance border-b text-center">A propos de ce site</h1>
      <NuxtImg sizes="xs:100vw lg:13vw" class="float-left rounded-md mt-1 mr-10" src="/me_jpg_75.jpg" format="webp" densities="x1" alt="" />
      <p class="mb-6 text-balance text-justify text-sm ">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quo dolore nihil nemo aut deleniti soluta quia doloremque corporis voluptates aspernatur, vel placeat tempore ut recusandae veritatis incidunt quae veniam nesciunt?<br>
        Nisi sunt delectus laudantium dolor animi tempora alias magni libero! Blanditiis, adipisci? Laudantium officia nobis possimus accusamus hic culpa laboriosam aliquid nam id nisi. Aspernatur deleniti hic sed alias adipisci.<br>
        Cupiditate explicabo perferendis officiis possimus suscipit exercitationem temporibus, ullam, facere rem provident autem dolorem quam ratione voluptates fugit quibusdam vel distinctio. Aperiam soluta dolore atque nam quos doloribus rerum magnam!
        Fugit eveniet, assumenda est quibusdam alias, debitis dignissimos repellat sint autem natus dolor blanditiis consequatur nemo accusamus. Sint, natus alias minus necessitatibus voluptatibus, magni molestiae nesciunt deleniti accusantium ipsa numquam!
        Similique, debitis? Saepe amet culpa vel voluptate ad sunt pariatur ipsam impedit fugit eligendi aliquam enim suscipit totam in officia quae, molestiae, commodi minus! Esse explicabo voluptatem unde sint illo!
      </p>
      <p class="text-l mb-6 text-balance text-justify text-sm ">
        Ducimus, eaque voluptatem debitis quisquam dolorum praesentium ipsam fugiat quaerat esse facere quos modi voluptatibus obcaecati mollitia nulla quas itaque, porro quo illo amet sed. Labore minima sint nisi unde?
        Laudantium ipsa sapiente ab, maiores, quod atque qui beatae mollitia dolores aliquid et laborum odit. Qui delectus quaerat magnam, fuga rem debitis ad atque! Totam minus ad consectetur dolorum natus?
        Itaque laborum ratione soluta commodi! Aut provident ipsum sit. Velit, sapiente? Suscipit incidunt ducimus esse distinctio atque assumenda nostrum, veritatis minima dolorum asperiores aperiam quasi aliquid odit eaque deleniti illo!<br>
        Deleniti natus architecto adipisci voluptas officiis sapiente, sit maiores, quas neque eligendi perspiciatis. Esse eos, doloremque minima, voluptatem laborum quis quisquam aut fuga similique omnis illum voluptates hic atque rem.
      </p>
    </section>
  </main>
</template>
