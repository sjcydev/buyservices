<script>
  import Fa from "svelte-fa";
  import {
    faPlaneUp,
    faTruckFast,
    faWarehouse,
  } from "@fortawesome/free-solid-svg-icons";
  import AbrirCasillero from "$lib/components/AbrirCasillero.svelte";
  import WorldPng from "$lib/assets/world.png";
  import PaperPlane from "$lib/assets/paperplane.png";

  let services = [
    {
      title: "Carga Aérea",
      icon: faPlaneUp,
      section: "areo",
      content:
        "Servicio de transporte rápido y seguro de mercancías por avión, ideal para tus compras en linea",
    },
    {
      title: "Delivery Rápido",
      icon: faTruckFast,
      section: "deliver",
      content:
        "Entrega a domicilio en la Ciudad capital, coordinamos la entrega por encomienda al interior del país",
    },
    {
      title: "Base en Miami",
      icon: faWarehouse,
      section: "warehouse",
      content:
        "Nuestro depósito estratégicamente ubicado en Miami ofrece almacenamiento seguro y servicios de distribución eficientes para tus pedidos.",
    },
  ];
</script>

<svelte:head>
  <title>
    507BuyServices - Agencia de Carga Internacional con base en Miami y Panama
  </title>
</svelte:head>

<div
  class="hero min-h-screen"
  style="background-image: url(https://images.unsplash.com/photo-1587293852726-70cdb56c2866?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1472&q=80);"
>
  <div class="hero-overlay bg-opacity-70" />
  <div class="hero-content text-center text-neutral-content lg:mb-36">
    <div class="max-w-2xl">
      <span class="uppercase font-normal">Compras por internet</span>
      <h1 class="mb-5 text-4xl lg:text-8xl font-semibold">
        Facil Rápido<br />Sencillo
      </h1>
      <p class="mb-5">
        Te facilitamos tus compras por internet de cualquier parte del mundo.
        Compra y recibe tus ordenes en un solo lugar a un precio accessible y
        sin costo adicional.
      </p>
      <button class="btn btn-secondary">Abre tu Casillero Gratis</button>
    </div>
  </div>
</div>

<div class="grid place-items-center relative">
  <div
    class="card w-full max-w-7xl bg-base-100 rounded-none lg:shadow-2xl lg:absolute
    lg:-top-56"
  >
    <div class="card-body grid lg:grid-cols-2 place-items-center p-2 lg:p-8">
      <div class="grid place-items-center">
        <img src={WorldPng} alt="Cajas" class="p-6" />
        <h2 class="md:text-2xl font-semibold max-w-md text-center">
          Recibe tus paquetes del cualquier parte del mundo
        </h2>
      </div>
      <AbrirCasillero />
    </div>
  </div>
</div>

<div
  class="hidden md:card bg-base-100 text-black w-full max-w-7xl
  lg:rounded-none lg:mt-[37rem] mx-auto place-items-center"
>
  <h3 class="text-2xl font-medium mb-10">Nuestros Servicios</h3>
  <div class="grid lg:grid-cols-3 gap-x-8 place-items-center">
    {#each services as service}
      <div
        class="text-xl font-medium p-12 text-left shadow-2xl
        max-w-lg h-full"
      >
        <Fa icon={service.icon} class="text-secondary text-3xl" />
        <h3 class="mt-6">{service.title}</h3>
        <p class="text-sm font-light">{service.content}</p>
      </div>
    {/each}
  </div>
</div>

<div class="grid place-items-center md:hidden mt-10">
  <h3 class="text-xl font-medium">Nuestros Servicios</h3>

  <div class="carousel carousel-center max-w-full p-4 space-x-4 w-full">
    {#each services as service}
      <div
        class="carousel-item text-xl font-medium text-left shadow-lg flex-col items-start w-3/4 p-6"
      >
        <Fa icon={service.icon} class="text-secondary" />
        <h3 class="mt-6">{service.title}</h3>
        <p class="text-sm font-light">{service.content}</p>
      </div>
    {/each}
  </div>
</div>

<div class="grid place-items-center lg:mt-24">
  <div class="card w-full max-w-5xl bg-base-100 rounded-none">
    <div class="card-body grid lg:grid-cols-2 place-items-center">
      <div class="p-5">
        <h3 class="text-2xl font-semibold mb-5">Precio Único</h3>
        <p>
          Solo te facturamos lo que traes. Con una sola tarifa no te tienes que
          preocupar de nada mas. Consigue tu casillero GRATIS!
        </p>
      </div>
      <div
        class="place-self-start px-5 lg:px-0 lg:text-center lg:place-self-center"
      >
        <h3 class="text-3xl lg:text-5xl font-semibold">$2.75</h3>
        <p>/ libra sin volumen</p>
      </div>
    </div>
    <!-- <img -->
    <!--   src={PaperPlane} -->
    <!--   alt="Avion de Papel" -->
    <!--   class="absolute w-32 -bottom-8 -right-8" -->
    <!-- /> -->
  </div>
</div>

<div
  class="hero min-h-[24rem] max-w-7xl mx-auto mt-10"
  style="background-image: url(https://images.unsplash.com/photo-1580160667723-8f98952d1017?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1374&q=80);"
>
  <div class="hero-overlay bg-opacity-50" />
  <div class="hero-content text-center text-neutral-content">
    <div class="max-w-md">
      <h1 class="mb-5 text-4xl lg:text-5xl font-bold">Una vez en Miami</h1>
      <p class="mb-5">Le entregamos su paquete en 48 horas!</p>
      <button class="btn btn-secondary">Comprar en Linea Ahora</button>
    </div>
  </div>
</div>
