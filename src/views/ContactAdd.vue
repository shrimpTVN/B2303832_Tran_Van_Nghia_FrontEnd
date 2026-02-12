<script>
import ContactForm from "@/components/ContactForm.vue";
import ContactService from "@/services/contact.service";

export default {
  components: {
    ContactForm,
  },
  data() {
    return {
      contact: {
        name: "",
        address: "",
        phone: "",
        email: "",
      },
    };
  },
  methods: {
    async createContact(contact) {
      try {
        await ContactService.create(contact);
        alert("Thêm liên hệ mới thành công!");
        this.$router.push({ name: "contactbook" });
      } catch (err) {
        console.log(err);
      }
    },
  },
};
</script>

<template>
  <div class="page">
    <h4>Thêm liên hệ mới</h4>
    <ContactForm :contact="contact" @submit:contact="createContact" />
  </div>
</template>
