<template>
  <Card>
    <template #title>Welcome To My Portfolio!</template>
    <template #content>
      <p class="m-0">
        Hi, I'm wizard-lgtm, i'm a software developer works on Systems.
      </p>
      <Image alt="Image" preview class="s-w-full max-w-full">
        <template #previewicon>
          <i class="pi pi-search"></i>
        </template>
        <template #image>
          <img src="/wizardhiding.png" alt="image" class="w-full h-auto max-w-full object-contain" />
        </template>
        <template #preview="slotProps">
          <img
            src="/wizardhiding.png"
            alt="preview"
            :style="slotProps.style"
            @click="slotProps.onClick"
            class="w-full h-auto max-w-full object-contain"
          />
        </template>
      </Image>

      <Divider />
      <Panel header="Notable Projects">
        <div style="display: flex; flex-direction: column; gap: 1rem;">
          <Card style="background: var(--p-content-background); border: 1px solid var(--p-content-border-color);">
            <template #title>
              <div style="display: flex; align-items: center; gap: 0.5rem; font-size: 1.25rem;">
                <i class="pi pi-code" style="color: var(--p-primary-color);"></i>
                <span>hhcc</span>
              </div>
            </template>
            <template #content>
              <p style="margin: 0; color: var(--p-text-muted-color); line-height: 1.6;">
                The Holy Holy C Language Compiler Built on LLVM
              </p>
              <div style="margin-top: 0.75rem;">
                <Tag value="C" severity="secondary" style="margin-right: 0.5rem;"></Tag>
                <Tag value="LLVM" severity="secondary"></Tag>
              </div>
            </template>
          </Card>

          <Card style="background: var(--p-content-background); border: 1px solid var(--p-content-border-color);">
            <template #title>
              <div style="display: flex; align-items: center; gap: 0.5rem; font-size: 1.25rem;">
                <i class="pi pi-server" style="color: var(--p-primary-color);"></i>
                <span>tiny-http-zig</span>
              </div>
            </template>
            <template #content>
              <p style="margin: 0; color: var(--p-text-muted-color); line-height: 1.6;">
                A tiny web framework for building fast HTTP servers
              </p>
              <div style="margin-top: 0.75rem;">
                <Tag value="Zig" severity="secondary" style="margin-right: 0.5rem;"></Tag>
                <Tag value="Web Framework" severity="secondary"></Tag>
              </div>
            </template>
          </Card>

          <Card style="background: var(--p-content-background); border: 1px solid var(--p-content-border-color);">
            <template #title>
              <div style="display: flex; align-items: center; gap: 0.5rem; font-size: 1.25rem;">
                <i class="pi pi-book" style="color: var(--p-primary-color);"></i>
                <span>RISC-V Tutorials</span>
              </div>
            </template>
            <template #content>
              <p style="margin: 0; color: var(--p-text-muted-color); line-height: 1.6;">
                Kernel Development Tutorials on riscv64 architecture
              </p>
              <div style="margin-top: 0.75rem;">
                <Tag value="RISC-V" severity="secondary" style="margin-right: 0.5rem;"></Tag>
                <Tag value="Kernel Dev" severity="secondary"></Tag>
              </div>
            </template>
          </Card>
        </div>
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
        <Button class="mt-4 px-6 py-3"  label="Send" />
      </Panel>
    </template>
  </Card>
</template>

<script setup>
import Image from "primevue/image";
import Textarea from "primevue/textarea";
import { reactive } from "vue";

onRenderTriggered(() => {
const name = reactive("");
const email = reactive("");
});
</script>
