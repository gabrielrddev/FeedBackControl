<script>
import HeaderItem from '../components/HeaderItem.vue'

export default {
components: {
  HeaderItem
}
}

</script>

<template>
  <HeaderItem/>
  <div class="container">
    <h2>Formulário de Feedback</h2>
    <form>
      <label for="satisfaction">Nível de Satisfação:</label>
      <select id="satisfaction" name="satisfaction" required>
        <option value="">Selecione uma opção</option>
        <option value="5">Muito Satisfeito</option>
        <option value="4">Satisfeito</option>
        <option value="3">Neutro</option>
        <option value="2">Insatisfeito</option>
        <option value="1">Muito Insatisfeito</option>
      </select>
      <label for="best-feature">O que você mais gostou?</label>
      <select id="best-feature" name="best-feature" required>
        <option value="">Selecione uma opção</option>
        <option value="atendimento">Atendimento</option>
        <option value="qualidade">Qualidade dos produtos/serviços</option>
        <option value="preco">Preço</option>
        <option value="ambiente">Ambiente</option>
        <option value="rapidez">Rapidez no serviço</option>
      </select>
      <label for="improvement">O que poderia ser melhorado?</label>
      <select id="improvement" name="improvement" required>
        <option value="">Selecione uma opção</option>
        <option value="atendimento">Atendimento</option>
        <option value="qualidade">Qualidade dos produtos/serviços</option>
        <option value="preco">Preço</option>
        <option value="ambiente">Ambiente</option>
        <option value="rapidez">Rapidez no serviço</option>
      </select>
      <label for="additional-comments">Comentários adicionais:</label>
      <textarea id="additional-comments" name="additional-comments"></textarea>
      <button type="submit">Enviar Feedback</button>
    </form>
  </div>
</template>

<style>
body {
  margin: 0;
  padding: 0;
  font-family: Arial, sans-serif;
  background-color: #121212;
}

.container {
  background-color: #1e1e1e;
  padding: 1.5rem;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
  width: 90%;
  max-width: 500px;
  margin: 5rem auto 2rem;
  flex-grow: 1;
}

h2 {
  color: #ffffff;
  text-align: center;
  font-size: 1.5rem;
  margin-bottom: 1.5rem;
}

form {
  display: flex;
  flex-direction: column;
}

label {
  margin-top: 1rem;
  color: #bdbdbd;
  font-size: 0.9rem;
}

select, textarea {
  width: 100%;
  padding: 0.5rem;
  margin-top: 0.5rem;
  border: 1px solid #424242;
  border-radius: 4px;
  box-sizing: border-box;
  background-color: #2c2c2c;
  color: #e0e0e0;
  font-size: 0.9rem;
}

textarea {
  resize: vertical;
  min-height: 100px;
}

button {
  background-color: #ffffff;
  color: #121212;
  border: none;
  padding: 0.75rem;
  margin-top: 1.5rem;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s ease, color 0.3s ease;
  font-size: 1rem;
}

button:hover {
  background-color: #e0e0e0;
  color: #000000;
}

@media (max-width: 600px) {
  .container {
    width: 95%;
    padding: 1rem;
    margin: 3rem auto 1rem;
  }

  h2 {
    font-size: 1.3rem;
  }

  label, select, textarea, button {
    font-size: 0.85rem;
  }

  button {
    padding: 0.6rem;
  }
}

@media (max-width: 400px) {
  .container {
    width: 98%;
    padding: 0.8rem;
  }

  h2 {
    font-size: 1.2rem;
  }

  label, select, textarea, button {
    font-size: 0.8rem;
  }
}
</style>