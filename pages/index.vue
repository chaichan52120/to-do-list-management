<template lang="pug">
.bg-center.bg-cover.relative.flex.min-h-screen.flex-col.justify-center.overflow-hidden.bg-gray-50(class="bg-[url('~/assets/bg-login.jpg')]")
  .relative.bg-white.p-10.shadow-xl.ring-1.ring-gray-200.mx-auto.rounded-xl.container.max-w-screen-lg
    svg(width="180" height="50")
      image(xlink:href="https://play.tailwindcss.com/img/logo.svg" src="yourfallback.png" width="180" height="50")
    .grid.grid-cols-3.gap-4
      .col-span-3.p-10(class="md:col-span-2")
        img(src="~/assets/service.png" alt="service" class="w-full")
      .col-span-3(class="md:col-span-1")
        p.text-3xl.font-light.text-gray-800.mb-3 Welcome Back :)
        p.text-xs.font-light.text-gray-600.mb-6 to keep connected with us please login with your personal infomarion by email address and password
          svg.inline(fill="orange" width="15" height="15" stroke="currentColor" stroke-width="1.5" viewBox="0 0 25 25" xmlns="http://www.w3.org/2000/svg" aria-hidden="true")
            path(stroke-linecap="round" stroke-linejoin="round" d="M14.857 17.082a23.848 23.848 0 005.454-1.31A8.967 8.967 0 0118 9.75v-.7V9A6 6 0 006 9v.75a8.967 8.967 0 01-2.312 6.022c1.733.64 3.56 1.085 5.455 1.31m5.714 0a24.255 24.255 0 01-5.714 0m5.714 0a3 3 0 11-5.714 0")
        .mb-3
        .relative.mb-1
          .absolute.inset-y-0.left-0.flex.items-center.pl-3.pointer-events-none
            svg.w-6.h-6.text-gray-400(xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor")
              path(stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 01-2.25 2.25h-15a2.25 2.25 0 01-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0019.5 4.5h-15a2.25 2.25 0 00-2.25 2.25m19.5 0v.243a2.25 2.25 0 01-1.07 1.916l-7.5 4.615a2.25 2.25 0 01-2.36 0L3.32 8.91a2.25 2.25 0 01-1.07-1.916V6.75")
          input.bg-slate-200.text-gray-800.block.w-full.pl-12.px-5(type="text" class="focus:bg-white focus:border-0" :class="email.length > 0 ? 'pt-5 pb-3' : 'pt-3 pb-5'" v-model="email")
          .absolute.pointer-events-none.text-gray-400(:class="email.length > 0 ? 'text-xs top-1 left-12' : 'text-base top-4 left-12'") Email Address
          button.bg-green-600.rounded-full.p-1.text-white.absolute.right-4.top-5(type="submit" v-show="email.includes('@')")
            svg.w-3.h-3(xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="3" stroke="currentColor")
              path(stroke-linecap="round" stroke-linejoin="round" d="M4.5 12.75l6 6 9-13.5")
        .relative.mb-6
          .absolute.inset-y-0.left-0.flex.items-center.pl-3.pointer-events-none
            svg.w-6.h-6.text-gray-400(xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor")
              path(stroke-linecap="round" stroke-linejoin="round" d="M16.5 10.5V6.75a4.5 4.5 0 10-9 0v3.75m-.75 11.25h10.5a2.25 2.25 0 002.25-2.25v-6.75a2.25 2.25 0 00-2.25-2.25H6.75a2.25 2.25 0 00-2.25 2.25v6.75a2.25 2.25 0 002.25 2.25z")
          input.bg-slate-200.text-gray-800.block.w-full.pl-12.px-5(type="password" class="focus:bg-white focus:border-0" :class="password.length > 0 ? 'pt-5 pb-3' : 'pt-3 pb-5'" v-model="password")
          .absolute.pointer-events-none.text-gray-400(:class="password.length > 0 ? 'text-xs top-1 left-12' : 'text-base top-4 left-12'") Password
        .mb-4.grid.grid-cols-4.gap-2.px-3
          .col-span-2.flex
            input.h-4.w-4(type="checkbox")
            label.pl-2.text-xs.font-light.text-gray-500 Remember Me
          .col-span-2.text-right
            p.text-xs.font-light.text-gray-500 Forget Password?
        .mb-4
          button.py-2.px-4.text-white.rounded-full.bg-blue-500.text-sm.shadow Login Now
          button.py-2.px-4.text-gray-600.rounded-full.bg-white.text-sm.ml-3.shadow Create Account
        p.text-xs.font-light.text-gray-500 Or you can join with
        .mt-4
          button.rounded-full.p-2.shadow-md(class="hover:shadow-lg focus:shadow-lg focus:outline-none focus:ring-0 active:shadow-lg" type="button" data-te-ripple-init data-te-ripple-color="light" style="background-color: #CA4A3B")
            svg.h-4.w-4(xmlns="http://www.w3.org/2000/svg" fill="white" viewBox="0 0 24 24")
              path(d="M7 11v2.4h3.97c-.16 1.029-1.2 3.02-3.97 3.02-2.39 0-4.34-1.979-4.34-4.42 0-2.44 1.95-4.42 4.34-4.42 1.36 0 2.27.58 2.79 1.08l1.9-1.83c-1.22-1.14-2.8-1.83-4.69-1.83-3.87 0-7 3.13-7 7s3.13 7 7 7c4.04 0 6.721-2.84 6.721-6.84 0-.46-.051-.81-.111-1.16h-6.61zm0 0 17 2h-3v3h-2v-3h-3v-2h3v-3h2v3h3v2z" fill-rule="evenodd" clip-rule="evenodd")
          button.ml-2.rounded-full.p-2.shadow-md(class="hover:shadow-lg focus:shadow-lg focus:outline-none focus:ring-0 active:shadow-lg" type="button" data-te-ripple-init data-te-ripple-color="light" style="background-color: #3C5695")
            svg.h-4.w-4(xmlns="http://www.w3.org/2000/svg" fill="white" viewBox="0 0 24 24")
              path(d="M9 8h-3v4h3v12h5v-12h3.642l.358-4h-4v-1.667c0-.955.192-1.333 1.115-1.333h2.885v-5h-3.808c-3.596 0-5.192 1.583-5.192 4.615v3.385z")
          button.ml-2.rounded-full.p-2.shadow-md(class="hover:shadow-lg focus:shadow-lg focus:outline-none focus:ring-0 active:shadow-lg" type="button" data-te-ripple-init data-te-ripple-color="light" style="background-color: #6DABEA")
            svg.h-4.w-4(xmlns="http://www.w3.org/2000/svg" fill="white" viewBox="0 0 24 24")
              path(d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z")
</template>

<script lang="ts" setup>
const email = ref<string>('')
const password = ref<string>('')
</script>

<style scoped>
.bg-white {
  background-color: #F9FAFC;
}
</style>