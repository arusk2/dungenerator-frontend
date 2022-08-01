<script setup>
import WelcomeItem from "./WelcomeItem.vue";
import DocumentationIcon from "./icons/IconDocumentation.vue";
import ToolingIcon from "./icons/IconTooling.vue";
import EcosystemIcon from "./icons/IconEcosystem.vue";
import CommunityIcon from "./icons/IconCommunity.vue";
import SupportIcon from "./icons/IconSupport.vue";
</script>

<template>
  <WelcomeItem>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>Documentation</template>

    Lorem ipsum dolor, sit amet consectetur adipisicing elit. Commodi reiciendis
    ipsa, modi ut repellat vero voluptate quam odit. Quibusdam, adipisci.
    Numquam repellat voluptates architecto dicta commodi repellendus distinctio
    eveniet quam!
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>Tooling</template>

    Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dicta sapiente
    veniam consectetur aspernatur asperiores, incidunt temporibus! Enim
    distinctio magnam quasi aliquam, libero repellat quia veniam. Hic aspernatur
    vero nesciunt porro?

    <br />

    More instructions are available in <code>README.md</code>.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <EcosystemIcon />
    </template>
    <template #heading>Ecosystem</template>

    Lorem ipsum, dolor sit amet consectetur adipisicing elit. Nam, architecto
    ex? Cum, officia impedit nesciunt aspernatur nemo exercitationem vitae neque
    quas, repellat odit suscipit sunt corrupti sed illum temporibus porro.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <CommunityIcon />
    </template>
    <template #heading>Community</template>

    Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt eligendi
    eos laborum nihil id ipsa eveniet! Deleniti recusandae fuga tenetur
    laboriosam pariatur error ut delectus dicta, perspiciatis aliquid quaerat
    earum!
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <SupportIcon />
    </template>
    <template #heading>Support Vue</template>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium numquam
    fugit ipsa odio doloremque repellendus magnam inventore. Corrupti esse
    excepturi, quis quo quidem repudiandae voluptates provident adipisci,
    praesentium, reprehenderit doloremque.
  </WelcomeItem>
</template>
