<script lang="ts">
  export let name: string;
  export let bio: string;
  export let imageUrl: string;
</script>

<div class="flex flex-col items-center justify-center w-full min-h-screen">
  <div
    class="flex flex-col md:flex-row items-center w-full justify-center text-center md:text-left"
    style="margin-top: -10vh;"
  >
    <div class="w-full md:w-1/2 p-4">
      <h2
        class="text-4xl font-extrabold leading-10 tracking-tight text-gray-800 sm:text-5xl sm:leading-none md:text-6xl"
      >
        <span class="font-bold">{name}</span>
      </h2>
      <p
        class="max-w-md mx-auto mt-3 text-base text-gray-500 sm:text-lg md:mt-5 md:text-xl md:max-w-3xl"
      >
        {bio}
      </p>
    </div>
    <div
      class="relative w-full md:w-1/2 flex justify-center mt-6 md:mt-0 p-4 image-container"
    >
      <img
        src={imageUrl}
        alt={name}
        class="w-48 h-48 rounded-full md:w-64 md:h-64 transform transition duration-700 ease-in-out"
      />
    </div>
  </div>
</div>

<style>
  /* Glowing ring animation */
  @keyframes glowing {
    0% {
      box-shadow: 0 0 0 0 rgba(45, 55, 72, 0.7);
    }
    50% {
      box-shadow: 0 0 20px 10px rgba(45, 55, 72, 0);
    }
    100% {
      box-shadow: 0 0 0 0 rgba(45, 55, 72, 0);
    }
  }

  /* Image hover effect */
  .image-container {
    position: relative;
    overflow: hidden;
    border-radius: 50%; /* Ensure the container is also circular */
    width: 300px; /* Adjust as necessary */
    height: 300px; /* Adjust as necessary */
  }

  .image-container img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: cover; /* Ensure the image fills the circular container */
    border-radius: 50%; /* Make the image circular */
    transition:
      transform 0.3s ease-in-out,
      filter 0.3s ease-in-out;
  }

  .image-container:hover img {
    transform: scale(1.05);
    filter: brightness(1.2);
  }

  .image-container::before {
    content: "";
    position: absolute;
    top: -10%;
    left: -10%;
    right: -10%;
    bottom: -10%;
    border-radius: 50%;
    animation: glowing 2s infinite;
    box-shadow: 0 0 20px 10px rgba(45, 55, 72, 0.7);
  }
</style>
