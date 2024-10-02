<template>
    <div class="container">
      <h1>Perguntas Frequentes</h1>
  
      <div class="company-description">
        <p>Na TechPulse Insights, nossa missão é capturar o pulso da inovação tecnológica através da voz anônima dos usuários. Somos os guardiões imparciais das experiências digitais, oferecendo uma plataforma onde as opiniões sobre as gigantes da tecnologia podem ser expressas livremente, moldando o futuro da indústria tech com cada feedback compartilhado.</p>
      </div>
  
      <div class="faq-item" v-for="(item, index) in faqItems" :key="index">
        <p class="faq-question">{{ item.question }}</p>
        <p class="faq-answer">{{ item.answer }}</p>
      </div>
    </div>
  </template>
  
  <script setup>
  const faqItems = [
    {
      question: "O que é a TechPulse Insights?",
      answer: "Somos uma empresa independente dedicada a coletar e analisar feedback anônimo sobre as maiores empresas de tecnologia do mundo (bigtechs). Nossa plataforma permite que usuários compartilhem suas experiências e opiniões de forma segura e confidencial."
    },
    {
      question: "Por que o feedback é anônimo?",
      answer: "O anonimato garante que os usuários possam expressar suas opiniões honestamente, sem medo de repercussões. Isso nos permite coletar dados mais precisos e valiosos sobre a qualidade dos produtos e serviços das bigtechs."
    },
    {
      question: "Como vocês garantem o anonimato?",
      answer: "Utilizamos tecnologias avançadas de criptografia e não coletamos informações pessoais identificáveis. Nossos sistemas são projetados para separar completamente o feedback do usuário que o forneceu."
    },
    {
      question: "O que vocês fazem com o feedback coletado?",
      answer: "Analisamos os dados para identificar tendências, pontos fortes e áreas de melhoria nas bigtechs. Publicamos relatórios regulares com insights agregados, que são utilizados por empresas, pesquisadores e o público em geral para entender melhor o impacto das grandes empresas de tecnologia."
    },
    {
      question: "Como posso participar e fornecer feedback?",
      answer: "Você pode acessar nosso formulário de feedback através do link na barra de navegação. O processo é simples, rápido e, claro, totalmente anônimo. Sua contribuição é valiosa para moldar o futuro da tecnologia!"
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
    max-width: 800px;
    margin: 80px auto 40px;
    padding: 2rem;
    background-color: #1e1e1e;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
  }
  
  h1 {
    color: #ffffff;
    text-align: center;
    font-size: 2rem;
    margin-bottom: 1.5rem;
  }
  
  .company-description {
    background-color: #2c2c2c;
    padding: 1.5rem;
    border-radius: 8px;
    margin-bottom: 2rem;
    text-align: center;
    font-style: italic;
  }
  
  .faq-item {
    margin-bottom: 2rem;
  }
  
  .faq-question {
    font-weight: bold;
    color: #b8b8ff;
    margin-bottom: 0.5rem;
  }
  
  .faq-answer {
    padding-left: 1rem;
  }
  
  @media (max-width: 768px) {
    .container {
      margin: 60px auto 30px;
      padding: 1.5rem;
    }
  
    h1 {
      font-size: 1.75rem;
    }
  
    .company-description {
      padding: 1rem;
    }
  
    .faq-answer {
      padding-left: 0.5rem;
    }
  }
  
  @media (max-width: 480px) {
    .container {
      margin: 40px auto 20px;
      padding: 1rem;
    }
  
    h1 {
      font-size: 1.5rem;
    }
  
    .company-description {
      padding: 0.75rem;
    }
  
    .faq-item {
      margin-bottom: 1.5rem;
    }
  
    .faq-question {
      font-size: 0.95rem;
    }
  
    .faq-answer {
      font-size: 0.9rem;
      padding-left: 0;
    }
  }
  </style>