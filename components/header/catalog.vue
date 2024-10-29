<template>
  <div class="catalog" :class="{ active: isCatalogVisible }">
    <div
      class="catalog__item"
      v-for="item in categories"
      :key="item.semanticId"
      @mouseenter="setActivateCategory(item.semanticId)"
      :class="{ active: isActiveCategory(item.semanticId) }"
    >
      <nuxt-link
        class="catalog__item-link"
        :to="`${basePath}/${item.semanticId}/`"
        :data-parent="item.semanticId"
        @click.native="toggleCatalog"
      >
        <span class="catalog__item-name">{{ item.name }}</span>
      </nuxt-link>
    </div>
  </div>
</template>

<script>
import { BasePath } from '@/assets/js/const';

const DEFAULT_CATEGORY = '1';

export default {
    props: {
        categories: {
            type: Array,
            required: true
        }
    }
}
</script>