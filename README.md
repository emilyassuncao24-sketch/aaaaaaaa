🛡️ Pipeline CI/CD com CodeQL no GitHub Actions
Este repositório contém o trabalho final da disciplina Desenvolvimento de Sistemas – Segurança da Informação (FATEC Santana de Parnaíba).
Foi implementada uma pipeline CI/CD completa usando GitHub Actions e CodeQL para análise estática de segurança em um projeto Python.

🔄 Fluxo da Pipeline
A pipeline é composta por 3 jobs em sequência, seguindo o modelo da apostila:

🔒 Análise CodeQL

Executa análise estática de segurança em Python
Usa .github/codeql-config.yml com consultas de segurança estendida e segurança + qualidade
Publica alertas em Security → Code scanning alerts
Se falhar, interrompe toda a pipeline
🧪 Testes Automatizados

Executa testes com pytest e verificação de estilo com flake8
Garante que o código funciona corretamente e segue boas práticas
Só roda se a análise CodeQL for bem-sucedida
🚀 Deploy para Stage (simulado)

Simula o deploy para o ambiente stage configurado no repositório
Mostra a versão (SHA do commit) e a branch publicada
Só executa se os Jobs 1 e 2 passarem
📂 Estrutura Principal do Projeto
.github/workflows/ci-cd-pipeline.yml – Pipeline CI/CD (CodeQL → Testes → Deploy Stage)
.github/codeql-config.yml – Configuração das consultas do CodeQL
main.py – Código principal em Python (funções de exemplo usadas nos testes)
tests/test_main.py – Testes automatizados com pytest
requirements.txt – Dependências do projeto (app, testes e ferramentas)
README.md – Documentação do trabalho
🎯 Objetivo do Trabalho
Demonstrar, na prática, o uso de CI/CD + CodeQL dentro do GitHub para:

1. Processo finalizado (com sucesso)

<img width="968" height="367" alt="toma" src="https://github.com/user-attachments/assets/2beb1314-728c-423a-a066-59d890065b50" />

2. Aviso de injeção SQL ao código

<img width="1013" height="305" alt="toma2" src="https://github.com/user-attachments/assets/2d2245ee-b96e-4044-921e-2eee165129aa" />

3. Processo dos passos

<img width="966" height="464" alt="toma3" src="https://github.com/user-attachments/assets/2d299f7a-a3f3-4754-abfe-68651f4a3c9d" />



Detectar vulnerabilidades de segurança (como SQL Injection) automaticamente
Impedir que código inseguro avance para o fluxo de entrega
Integrar segurança, testes e deploy em um processo contínuo, seguindo o conceito de DevSecOps proposto.

Autor
Nome: Emily Giovana paiva Assunção

SegInfo — FATEC

Disciplina: Desenvolvimento de Sistema seguro (SO)

Professor: Idirley Soares
