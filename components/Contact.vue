<template>
  <div class="bg-[#f9f9f9] py-[50px] lg:pt-[80px] lg:pb-[116px]">
    <Container>
      <h2 class="font-serif text-[#1d1d1d] text-4xl md:text-5xl">Contact</h2>

      <div class="flex flex-row mt-[30px] lg:mt-[40px]">
        <form
          action="https://getform.io/f/9ebd8290-40d4-4040-b854-c5044bec49d1"
          method="POST"
          class="contact__card"
        >
          <label for="name">Your Name:</label>
          <input type="text" name="name" placeholder="Your Name" required />
          <label for="email">Your Email:</label>
          <input
            type="email"
            name="email"
            placeholder="your@email.com"
            required
          />
          <label for="message">Message:</label>
          <textarea
            type="text"
            name="message"
            placeholder="Your message..."
            class="textarea"
            required
          />

          <button type="submit" class="contact__button">Send message</button>
        </form>

        <div class="contact__panel">
          <h3 class="text-4xl font-serif">How Can I Help?</h3>
          <p class="mt-[50px]">🧠 You’ve got a project in mind?</p>
          <p class="mt-[40px]">🤲 Your current project needs more hands?</p>
          <p class="mt-[40px]">🤷 Don’t know where to start?</p>
          <p class="mt-[40px] font-semibold">
            📩 Shoot me a message and I’ll get back to you ASAP.
          </p>
          <p class="mt-[40px]">
            Speak soon,<br />
            José :)
          </p>
        </div>
      </div>
    </Container>
  </div>
</template>

<script>
export default {
  name: 'Contact',
}
</script>

<style lang="postcss">
.contact__card {
  @apply w-full md:w-6/12 bg-white rounded-xl md:rounded-r-none shadow-md p-[16px] lg:px-[42px] lg:py-[50px] text-2xl md:my-[24px];
}
input,
textarea {
  @apply text-xl border border-[#1d1d1d] rounded-md mt-[10px] mb-[16px] lg:mb-[40px] w-full h-[40px] px-[8px];
  &.textarea {
    @apply h-[170px] pt-[8px];
    resize: none;
  }
}
.contact__button {
  @apply w-full rounded-lg h-[56px] bg-gradient-to-r from-[#28f3c3] to-[#9a65d9] text-[#f9f9f9] font-semibold;
}

.contact__panel {
  @apply w-6/12 hidden md:block bg-gradient-to-br from-[#9a65d9] to-[#28F3C3] text-[#f9f9f9] shadow-2xl px-[16px] py-[44px] lg:px-[44px] lg:py-[116px] text-2xl;
}
</style>
