<template>
  <div>
    <homepage :acc="account" />
  </div>
</template>
<script setup>
const account = {
  name: "John Snow",
  description: "Im John Snow, the king in the north. I know Nothing.",
  photo: "https://i.insider.com/56743fad72f2c12a008b6cc0",
  facebook: "https://www.facebook.com/john_snow",
  twitter: "https://twitter.com/john_snow",
  instagram: "https://www.instagram.com/john_snow",
  email: "mail@john_snow.cc",
  github: "https://github.com/john_snow",
  telegram: "https://t.me/john_snow",
  phone: "+918888888888",
  youtube: "https://youtube.com/@john_snow",
  linkedin: "https://linkedin.com/john_snow",
  // For link icons, see: https://nuxt.com/modules/icon
  links: [
    {
      title: "My Website",
      icon: "ph:facebook-logo-duotone",
      url: "https://example.com",
    },
    {
      title: "Amazon wishlist",
      icon: "ant-design:amazon-outlined",
      url: "https://amazon.in",
    },
    {
      title: "React JS course",
      icon: "grommet-icons:reactjs",
      url: "https://reactjs.org/",
    },
    {
      title: "Donate for our cause",
      icon: "iconoir:donate",
      url: "https://who.int",
    },
    {
      title: "Download my resume",
      icon: "ph:file-pdf",
      url: "https://google.com",
    },
  ],
};
</script>
