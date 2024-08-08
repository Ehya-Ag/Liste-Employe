<template>
  <div class="liste-employes">
    <h2>Liste des employés</h2>
    <ol class="elements-employes">
      <li class="employe" v-for="employe in employes" :key="employe.nom">
        {{ employe.nom }} - {{ employe.poste }}
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  data() {
    return {
      employes: [
        { nom: 'Alice', poste: 'Directrice' },
        { nom: 'Bob', poste: 'Développeur' },
        { nom: 'Charlie', poste: 'Designer' },
        { nom: 'David', poste: 'Testeur' },
        { nom: 'Eve', poste: 'Ressources Humaines' }
      ]
    };
  }
};
</script>

<style scoped>
.liste-employes {
  max-width: 600px;
  margin: 0 auto;
  background-color: #f2f2f2;
  padding: 20px;
  border-radius: 5px;
  box-shadow: 0 0 10px rgba(0,0,0,0.1);
}

.liste-employes h2 {
  text-align: center;
}

.elements-employes {
  list-style-type: none;
  padding: 0;
}

.employe {
  padding: 10px;
  border-bottom: 1px solid #ccc;
  cursor: pointer;
}

.employe:hover {
  background-color: #e6f7ff;
}
</style>
