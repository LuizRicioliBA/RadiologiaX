[README.md](https://github.com/user-attachments/files/35217382/README.md)
# 🩻 Solução RaioX

Agende. Confirme. Laude. Fature. — a operação do raio-x veterinário móvel em um só lugar.

![Portais](https://img.shields.io/badge/Portais-dono%20%C2%B7%20cl%C3%ADnica%20%C2%B7%20equipe-green)
![Dados](https://img.shields.io/badge/Dados-100%25%20simulados-blue)
![Projeto](https://img.shields.io/badge/Projeto-em%20desenvolvimento-orange)

---

## 🎯 Sobre o Projeto

O **Solução RaioX** é um sistema para organizar a operação inteira de uma empresa de raio-x veterinário que
atende clínicas em várias cidades. A proposta é tirar o controle de cabeça (e de planilha) e colocar tudo em
três portais que conversam entre si: o **dono** acompanha e fatura, a **clínica** agenda e paga, e a
**equipe de campo** executa com um app de celular. Tudo roda no navegador, **sem backend e sem instalação**:
o "banco" é de mentira (memória + `localStorage`), então nenhum dado real é usado ou enviado.

## 🚀 O que o sistema faz

- 🏠 **Reúne três portais em um só app**: dono (operação e dinheiro), clínica (agenda e pagamentos) e equipe (app de campo em moldura de celular).
- 📅 **Monta a agenda da equipe com vagas de última hora**: quando alguém cancela, o horário é oferecido na hora às outras clínicas da cidade — o que era prejuízo vira exame.
- ✅ **Confirma presença de verdade (AVISO-VIVO)**: a clínica confirma o próximo exame na tela de Avisos; a equipe recebe "podem ir" e o dono recebe o zap. Cancelou? Abre o cancelamento real, com motivo e todas as consequências.
- 💳 **Aplica a regra de ouro do faturamento**: a cobrança só nasce quando o laudo é entregue — antes disso, não existe cobrança e ninguém liga cobrando.
- ⚖️ **Não deixa ninguém decidir sozinho**: se a clínica cancela depois de a equipe já ter executado, vira *conflito* para a administração — o sistema não apaga o trabalho de ninguém.
- 🤖 **Tem assistente que não demora**: responde em ~0,5 s com o cérebro local; a IA (chave opcional do dono) só *melhora a mesma bolha* depois, desistindo sozinha em até 10 s.
- 🗼 **Mostra a operação na Torre de Controle**: hoje e amanhã, cidade a cidade, com contadores, conflitos e laudos atrasados em uma tela só.
- 🌗 **Respeita o tema claro e o escuro** com variáveis de tinta: nenhuma tela fica com texto invisível; e as **notificações não grudam** — somem sozinhas e no clique.
- 📝 **Deixa o dono escrever os próprios textos** em `js/textos.js`, com padrão seguro se alguma chave faltar ou quebrar.

## 📙 Como funciona

1. A clínica agenda um horário verde na agenda (ou pega uma ⚡ vaga de última hora liberada por cancelamento).
2. Um dia antes, a clínica **confirma presença** na tela de Avisos — a equipe recebe o aviso de que pode ir.
3. A equipe realiza o exame no app de campo e envia as imagens; o laudador analisa e emite o laudo.
4. **Só então** a cobrança nasce: a clínica paga com Pix ou boleto e o comprovante sai na hora.
5. O dono acompanha tudo pelo resumo das 8h, pela Torre de Controle e pelo WhatsApp 8h — e o mês fecha com fatura consolidada por clínica.
