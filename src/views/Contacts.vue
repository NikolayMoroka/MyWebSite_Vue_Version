<template>
    <div class="contacts">
        <v-container>
            <div>
                <h3 class="title_block mb-5">
                    CONTACTS
                </h3>
            </div>
            <v-card color="#290653">
                <v-row>
                    <v-col cols="12" class="text-left">
                        <div v-for="(contact, index) in contactsInfo" :key="index" class="mb-3">
                            <p class="text_block text-left mb-0">{{ contact.title }}</p>
                            <p class="contacts_small_text text-left mb-0">{{ contact.text }}</p>
                            <a :href="contact.link" class="text-left contacts_small_text"> {{ contact.link }} </a>
                        </div>
                    </v-col>
                    <v-col>

                    </v-col>
                </v-row>
            </v-card>
        </v-container>
    </div>
</template>

<script>
export default {
    name: 'Contacts',
    data: () => ({
        contactsInfo: [
            {
                title: 'Location',
                text: 'Kharkiv, Ukraine',
            },
            {
                title: 'Phone number',
                text: '+380 66 000 12 86 (Telegram, Viber, WhatsApp)',
            },
            {
                title: 'LinkedIn',
                link: 'linkedin.com/in/nikolay-moroka-b467991a7',
            },
            {
                title: 'GitHub',
                link: 'https://github.com/NikolayMoroka',
            },
            {
                title: 'Email',
                text: 'nikolaymorokaw@gmail.com',
            },
        ]

    })
}
</script>

<style scoped>
 a {
    color: white !important;
    font-family: 'PT Sans', sans-serif !important;
    font-size: 16px;
    text-decoration: none;
 }

</style>