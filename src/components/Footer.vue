<template>
  <div>
    <v-footer dark padless>
      <v-container>
        <v-row>
          <v-col v-for="user in social_medias" :key="user.name" md6>
            <v-list dark>
              <v-subheader>{{ user.name }}</v-subheader>
              <v-list-item v-for="item in user.data" :key="item.name">
                <v-list-item-icon>
                  <v-icon :color="item.color" v-text="item.icon"></v-icon>
                </v-list-item-icon>
                <v-list-item-content>
                  <a class="pl-2" :href="item.link">{{ item.name }}</a>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </v-col>
        </v-row>
        <v-row md12 class="text-center">
          <v-col md12>
            <p>
              Criado para a disciplina de Técnicas Avançadas de Desenvolvimento
              de Sistemas.
            </p>
            <p>2020 — {{ new Date().getFullYear() }}</p>
          </v-col>
        </v-row>
      </v-container>
    </v-footer>
  </div>
</template>

<script>
export default {
  data: () => ({
    social_medias: [
      {
        name: "Mateus Ragazzi",
        data: [
          {
            name: "mateusragazzi.b@gmail.com",
            icon: "mdi-email",
            link: "malito:mateusragazzi.b@gmail.com",
            color: "pink",
          },
        ],
      },
      {
        name: "Fernando Kendy",
        data: [
          {
            name: "yahirokendy@gmail.com",
            icon: "mdi-email",
            link: "malito:yahirokendy@gmail.com",
            color: "pink",
          },
        ],
      },
    ],
  }),
};
</script>