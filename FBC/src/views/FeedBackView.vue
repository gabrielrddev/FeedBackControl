<template>
    <div class="container">
      <h1>Status de Feedbacks</h1>
  
      <div class="table-container">
        <table>
          <thead>
            <tr>
              <th>Data</th>
              <th>Satisfação</th>
              <th>Mais Gostou</th>
              <th>Melhoria</th>
              <th>Status</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="(feedback, index) in feedbacks" :key="index">
              <td data-label="Data">{{ feedback.date }}</td>
              <td data-label="Satisfação">{{ feedback.satisfaction }}</td>
              <td data-label="Mais Gostou">{{ feedback.liked }}</td>
              <td data-label="Melhoria">{{ feedback.improvement }}</td>
              <td data-label="Status">
                <span :class="['status', `status-${feedback.status.toLowerCase()}`]">
                  {{ feedback.status }}
                </span>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </template>
  
  <script setup>
  const feedbacks = [
    {
      date: '2024-03-15',
      satisfaction: 'Muito Satisfeito',
      liked: 'Qualidade dos produtos/serviços',
      improvement: 'Preço',
      status: 'Revisado'
    },
    {
      date: '2024-03-14',
      satisfaction: 'Satisfeito',
      liked: 'Atendimento',
      improvement: 'Rapidez no serviço',
      status: 'Pendente'
    },
    {
      date: '2024-03-13',
      satisfaction: 'Neutro',
      liked: 'Ambiente',
      improvement: 'Qualidade dos produtos/serviços',
      status: 'Acao Necessaria'
    },
    {
      date: '2024-03-12',
      satisfaction: 'Insatisfeito',
      liked: 'Preço',
      improvement: 'Atendimento',
      status: 'Revisado'
    },
    {
      date: '2024-03-11',
      satisfaction: 'Muito Satisfeito',
      liked: 'Rapidez no serviço',
      improvement: 'Ambiente',
      status: 'Pendente'
    }
  ];
  </script>
  
  <style scoped>
  body {
    font-family: Arial, sans-serif;
    background-color: #121212;
    color: #e0e0e0;
    margin: 0;
    padding: 0;
    line-height: 1.6;
  }
  
  .container {
    max-width: 1000px;
    margin: 80px auto 40px;
    padding: 1rem;
    background-color: #1e1e1e;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
  }
  
  h1 {
    color: #ffffff;
    text-align: center;
    font-size: 1.8rem;
    margin-bottom: 1.5rem;
  }
  
  .table-container {
    overflow-x: auto;
  }
  
  table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 1rem;
  }
  
  th, td {
    padding: 0.75rem;
    text-align: left;
    border-bottom: 1px solid #424242;
  }
  
  th {
    background-color: #2c2c2c;
    color: #b8b8ff;
  }
  
  tr:nth-child(even) {
    background-color: #242424;
  }
  
  .status {
    padding: 0.4rem 0.6rem;
    border-radius: 4px;
    font-weight: bold;
    display: inline-block;
  }
  
  .status-revisado {
    background-color: #4caf50;
    color: #ffffff;
  }
  
  .status-pendente {
    background-color: #ffa500;
    color: #000000;
  }
  
  .status-acao {
    background-color: #f44336;
    color: #ffffff;
  }
  
  @media screen and (max-width: 768px) {
    .container {
      margin: 60px auto 30px;
      padding: 0.5rem;
    }
  
    h1 {
      font-size: 1.5rem;
    }
  
    table {
      border: 0;
    }
  
    table thead {
      display: none;
    }
  
    table tr {
      margin-bottom: 0.625em;
      display: block;
      border-bottom: 2px solid #424242;
    }
  
    table td {
      display: block;
      text-align: right;
      font-size: 0.8em;
      border-bottom: 1px dotted #424242;
    }
  
    table td::before {
      content: attr(data-label);
      float: left;
      font-weight: bold;
      text-transform: uppercase;
    }
  
    table td:last-child {
      border-bottom: 0;
    }
  }
  
  @media screen and (max-width: 480px) {
    .container {
      margin: 40px auto 20px;
    }
  
    h1 {
      font-size: 1.3rem;
    }
  
    .status {
      padding: 0.3rem 0.5rem;
      font-size: 0.7em;
    }
  }
  </style>