<template>
  <span :class="nouvelleClasse" v-html="icones[src]"></span>
</template>

<script>
export default {
  data() {
    return {
      icones: {
        ticket: `<svg class="contour" xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 512 512"><path fill="none" stroke="currentColor" stroke-miterlimit="10" stroke-width="32" d="M366.05 146a46.7 46.7 0 0 1-2.42-63.42a3.87 3.87 0 0 0-.22-5.26l-44.13-44.18a3.89 3.89 0 0 0-5.5 0l-70.34 70.34a23.62 23.62 0 0 0-5.71 9.24a23.66 23.66 0 0 1-14.95 15a23.7 23.7 0 0 0-9.25 5.71L33.14 313.78a3.89 3.89 0 0 0 0 5.5l44.13 44.13a3.87 3.87 0 0 0 5.26.22a46.69 46.69 0 0 1 65.84 65.84a3.87 3.87 0 0 0 .22 5.26l44.13 44.13a3.89 3.89 0 0 0 5.5 0l180.4-180.39a23.7 23.7 0 0 0 5.71-9.25a23.66 23.66 0 0 1 14.95-15a23.62 23.62 0 0 0 9.24-5.71l70.34-70.34a3.89 3.89 0 0 0 0-5.5l-44.13-44.13a3.87 3.87 0 0 0-5.26-.22a46.7 46.7 0 0 1-63.42-2.32Z"/><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-miterlimit="10" stroke-width="32" d="m250.5 140.44l-16.51-16.51m60.53 60.53l-11.01-11m55.03 55.03l-11-11.01m60.53 60.53l-16.51-16.51"/></svg>`,
        mappin: `<svg class="contour" xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"><path fill="currentColor" d="M12 12q.825 0 1.413-.587T14 10q0-.825-.587-1.412T12 8q-.825 0-1.412.588T10 10q0 .825.588 1.413T12 12m0 7.35q3.05-2.8 4.525-5.087T18 10.2q0-2.725-1.737-4.462T12 4Q9.475 4 7.738 5.738T6 10.2q0 1.775 1.475 4.063T12 19.35M12 22q-4.025-3.425-6.012-6.362T4 10.2q0-3.75 2.413-5.975T12 2q3.175 0 5.588 2.225T20 10.2q0 2.5-1.987 5.438T12 22m0-12"/></svg>`,
        bas: `<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"><path fill="currentColor" d="M11.708 14.17q.123.13.289.13q.165 0 .295-.13l2.094-2.095q.187-.187.09-.438q-.097-.252-.368-.252H9.883q-.264 0-.36.252q-.096.251.09.438zm.295 6.83q-1.866 0-3.51-.708q-1.643-.709-2.859-1.924q-1.216-1.214-1.925-2.856Q3 13.87 3 12.003q0-1.866.708-3.51q.709-1.643 1.924-2.859q1.214-1.216 2.856-1.925Q10.13 3 11.997 3q1.866 0 3.51.708q1.643.709 2.859 1.924q1.216 1.214 1.925 2.856Q21 10.13 21 11.997q0 1.866-.708 3.51q-.709 1.643-1.924 2.859q-1.214 1.216-2.856 1.925Q13.87 21 12.003 21M12 20q3.35 0 5.675-2.325T20 12q0-3.35-2.325-5.675T12 4Q8.65 4 6.325 6.325T4 12q0 3.35 2.325 5.675T12 20m0-8"/></svg>`,
      },
    };
  },
  props: {
    src: { default: "play" },
    class: {
      default: "icone",
    },
  },
  computed: {
    nouvelleClasse() {
      return this.class + " icone-svg";
    },
  },
};
</script>
<style>
.icone-svg svg {
  width: 1em;
  height: 1em;
  color: currentColor;
}

.icone-svg svg:not(.contour) path,
.icone-svg svg:not(.contour) polygon {
  fill: currentColor;
}
</style>
