<script>
  import Navbar from "./lib/Navbar.svelte";
  import FeaturedProjects from "./lib/FeaturedProjects.svelte";
  import src from "./assets/bluepnwage.jpg";
</script>

<Navbar />
<main style="min-height: 100vh;" class="bg-gray-50 flex flex-col items-center">
  <section class="w-3/5 mt-10 flex mb-10 ">
    <div class="w-2/4">
      <header>
        <h1 class="font-bold text-gray-800 text-5xl">Agis Carty</h1>
        <h2 class="mt-2 font-bold text-2xl mb-8 text-gray-500">Aspiring Front-end developer</h2>
      </header>
      <article>
        <p class="text-gray-900">
          Dolor cupidatat ea esse et nulla enim consectetur nisi. In laborum sunt et aute laboris laborum. Laboris
          ullamco reprehenderit proident voluptate irure. Dolor exercitation ullamco nostrud veniam do in consectetur
          magna. In anim consectetur velit ipsum cillum ipsum nulla aliquip culpa officia. Qui minim ex Lorem amet
          veniam veniam dolor veniam anim officia.
        </p>
      </article>
    </div>
    <div class="grow flex justify-center mt-5">
      <figure class="aspect-square w-16 ">
        <img {src} style="border-radius: 50%;" alt="mad kirby" width="100%" height="100%" />
      </figure>
    </div>
  </section>
  <section class="w-3/5">
    <header>
      <h2 class="font-bold text-gray-900 text-2xl">Featured Projects</h2>
    </header>
    <FeaturedProjects />
  </section>
</main>
