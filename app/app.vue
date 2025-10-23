<template>
  <Card>
    <template #title>Welcome To My Portfolio!</template>
    <template #content>
      <p class="m-0">
        Hi, I'm wizard-lgtm, i'm a software developer works on Systems.
      </p>
      <Image alt="Image" preview>
        <template #previewicon>
          <i class="pi pi-search"></i>
        </template>
        <template #image>
          <img src="/wizardhiding.png" alt="image" />
        </template>
        <template #preview="slotProps">
          <img
            src="/wizardhiding.png"
            alt="preview"
            :style="slotProps.style"
            @click="slotProps.onClick"
          />
        </template>
      </Image>

      <Divider />
      <Panel header="Notable Projects">
        <ul>
          <li>hhcc | The Holy Holy C Language Compiler Built on LLVM</li>
          <li>tiny-http-zig | a tiny web framework</li>
          <li>RISC-V tutorials | Kernel Development Tutorials on riscv64</li>
        </ul>
      </Panel>
      <Divider />
      <Panel class="m-x-10" header="Please KOntankt!">
        <IftaLabel>
          <InputText id="username" v-model="name" />
          <label for="username">Name:</label>
        </IftaLabel>
        <IftaLabel>
          <InputText id="email" v-model="email" />
          <label for="email">Email:</label>
        </IftaLabel>
        <IftaLabel>
          <Textarea name="message" v-model="value" rows="5" cols="30" />
          <label for="message">Message:</label>
        </IftaLabel>
        <Button class="block p-10" label="Send" />
      </Panel>
    </template>
  </Card>
</template>

<script setup>
import Image from "primevue/image";
import Textarea from "primevue/textarea";
import { reactive } from "vue";

const name = reactive("");
const email = reactive("");
</script>
