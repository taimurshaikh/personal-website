<section
  id="contact"
  class="min-h-screen py-16 bg-white flex items-center w-full"
>
  <div class="container mx-auto px-4">
    <h2
      class="text-4xl font-extrabold leading-10 tracking-tight text-gray-800 mb-4"
    >
      Contact
    </h2>
    <p class="text-base text-gray-500 sm:text-lg md:text-xl mb-8">
      Feel free to reach out to me via email or through my social media
      profiles.
    </p>
    <form
      action="https://formspree.io/f/your-form-id"
      method="POST"
      class="bg-gray-100 p-6 rounded-lg shadow-md"
    >
      <div class="mb-4">
        <label for="name" class="block text-gray-700">Name</label>
        <input
          type="text"
          id="name"
          name="name"
          class="w-full px-3 py-2 mt-1 border rounded-md focus:outline-none focus:ring focus:border-blue-300"
        />
      </div>
      <div class="mb-4">
        <label for="email" class="block text-gray-700">Email</label>
        <input
          type="email"
          id="email"
          name="_replyto"
          class="w-full px-3 py-2 mt-1 border rounded-md focus:outline-none focus:ring focus:border-blue-300"
        />
      </div>
      <div class="mb-4">
        <label for="message" class="block text-gray-700">Message</label>
        <textarea
          id="message"
          name="message"
          rows="4"
          class="w-full px-3 py-2 mt-1 border rounded-md focus:outline-none focus:ring focus:border-blue-300"
        ></textarea>
      </div>
      <button
        type="submit"
        class="px-4 py-2 bg-blue-500 text-white rounded-md hover:bg-blue-600 focus:outline-none focus:ring focus:border-blue-300"
        >Send</button
      >
    </form>
  </div>
</section>
