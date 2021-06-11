<template>
  <div class="--flare --flare-block" :class="revealer ? `${this.rev}` : ''">
    <div class="content">
      <div class="box">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Block",
    props: {
      revealer: {
        type: Boolean,
        require: false,
      }
    },
    data: () => ({
      observer: null,
      rev: '--fl-revealer',
    }),
    mounted() {
      this.observer = new IntersectionObserver(([entry]) => {
        let el = this.$el;
        if (el.classList.contains(this.rev) && entry.isIntersecting) {
          this.$emit("intersect");
          el.classList.add('active');
        } else {
          el.classList.remove('active');
        }
      });
      this.observer.observe(this.$el);
    },
    destroyed() {
      this.observer.disconnect();
    },
  };

</script>