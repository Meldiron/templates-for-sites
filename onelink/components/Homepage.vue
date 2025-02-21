<template>
  <main class="p-4 bg-white h-full w-full space-y-8 pt-12 max-w-lg mx-auto">
    <div class="text-center">
      <div
        v-if="acc.photo"
        class="h-20 w-20 rounded-full overflow-hidden ring ring-slate-200 mx-auto"
      >
        <img :src="acc.photo" alt="name" class="h-full w-full object-cover" />
      </div>
      <h1 v-if="acc.name" class="text-2xl font-bold mt-4 text-slate-800">
        {{ acc.name }}
      </h1>
      <p v-if="acc.d" class="text-sm mt-2 text-slate-600">
        {{ acc.description }}
      </p>
    </div>
    <div
      class="flex items-center justify-center flex-wrap"
    >
      <span v-if="acc.facebook" class="p-1">
        <a :href="acc.facebook" target="_blank" rel="noopener | noreferrer">
          <icon name="ph:facebook-logo-duotone" class="h-6 w-6" />
        </a>
      </span>
      <span v-if="acc.twitter" class="p-1">
        <a :href="acc.twitter" target="_blank" rel="noopener | noreferrer">
          <icon name="ph:twitter-logo-duotone" class="h-6 w-6" />
        </a>
      </span>
      <span v-if="acc.instagram" class="p-1">
        <a :href="acc.instagram" target="_blank" rel="noopener | noreferrer">
          <icon name="ph:instagram-logo-duotone" class="h-6 w-6" />
        </a>
      </span>
      <span v-if="acc.email" class="p-1">
        <a :href="acc.email" target="_blank" rel="noopener | noreferrer">
          <icon name="ph:envelope-duotone" class="h-6 w-6" />
        </a>
      </span>
      <span v-if="acc.telegram" class="p-1">
        <a :href="acc.telegram" target="_blank" rel="noopener | noreferrer">
          <icon name="ph:telegram-logo-duotone" class="h-6 w-6" />
        </a>
      </span>
      <span v-if="acc.phone" class="p-1">
        <a :href="`https://wa.me/${acc.w}`" target="_blank" rel="noopener | noreferrer">
          <icon name="ph:whatsapp-logo-duotone" class="h-6 w-6" />
        </a>
      </span>
      <span v-if="acc.youtube" class="p-1">
        <a :href="acc.youtube" target="_blank" rel="noopener | noreferrer">
          <icon name="ph:youtube-logo-duotone" class="h-6 w-6" />
        </a>
      </span>
      <span v-if="acc.email" class="p-1">
        <a :href="`mailto:${acc.email}`" target="_blank" rel="noopener | noreferrer">
          <icon name="ph:envelope-duotone" class="h-6 w-6" />
        </a>
      </span>
      <span v-if="acc.github" class="p-1">
        <a :href="acc.github" target="_blank" rel="noopener | noreferrer">
          <icon name="ph:github-logo-duotone" class="h-6 w-6" />
        </a>
      </span>
      <span v-if="acc.linkedin" class="p-1">
        <a :href="acc.linkedin" target="_blank" rel="noopener | noreferrer">
          <icon name="ph:linkedin-logo-duotone" class="h-6 w-6" />
        </a>
      </span>
    </div>
    <ul class="space-y-2">
      <ExternalLink
        v-for="(link, id) in acc.links"
        :label="link.title"
        :icon="link.icon"
        :url="link.url"
        :key="id"
      />
    </ul>
  </main>
</template>
<script setup>
const props = defineProps({
  acc: {
    type: Object,
    required: true,
  },
});
</script>
