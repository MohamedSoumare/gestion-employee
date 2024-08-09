<template>
  <div>
    <h1>Liste des employés</h1>
    <ol>
      <li 
        v-for="employe in employes" :key="employe.id" 
        @mouseover="hover = employe.id"
        @mouseleave="hover = null"
        :class="{ 'hovered': hover === employe.id }"
      >
      {{ employe.nom }}
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  name: 'EmployeList',
  data() {
    return {
      employes: [
        { id: 1, nom: 'Salif Dia' },
        { id: 2, nom: 'Mohamed Diop' },
        { id: 3, nom: 'Pierre John' },
        { id: 4, nom: 'Ismail ou Mohameden' },
      ],
      hover: null,
    };
  },
};
</script>

<style scoped>
ol {
  padding-left: 20px;
}

li {
  padding: 10px;
  margin: 5px 0;
  list-style-type: decimal;
  transition: background-color 0.3s ease;
}

li.hovered {
  background-color: #25fd04;
}
</style>
