# EC2Manager 🚀

Este repositório contém minhas anotações, práticas e insights adquiridos durante o laboratório de **Gerenciamento de Instâncias EC2** no bootcamp da DIO.

---
## 📚 Objetivos do Desafio

- Aplicar conceitos aprendidos em ambiente prático;
- Documentar processos técnicos de forma clara e organizada;
- Utilizar o GitHub como ferramenta de compartilhamento de documentação técnica.

---

## 🖥️ Conteúdo do Repositório

- `README.md`: explicação detalhada do desafio e minhas anotações principais;
- `anotacoes.md`: registros passo a passo de comandos, configurações e observações;
- `/images`: capturas de tela para apoiar a documentação.

---

## 📝 Principais Conceitos Praticados

1. **Criação de Instâncias EC2**
   - Escolha do tipo de instância ( t2.micro)
   - Configuração de rede e segurança
   - Conexão via SSH

2. **Amazon Machine Image (AMI)**
   - Criação de uma AMI personalizada
   - Vantagens do uso de AMIs em ambientes de produção

3. **Elastic Block Store (EBS)**
   - Criação de volumes EBS
   - Snapshots para backup e recuperação
   - Diferença entre instâncias com armazenamento temporário e persistente

4. **Boas Práticas**
   - Uso de tags para organização
   - Regras de segurança (Security Groups)
   - Escalabilidade vertical x horizontal

---

## 📷 Evidências

As imagens do processo estão organizadas na pasta `/images`:
## 🔗 Diagrama de Interação dos Serviços AWS

Abaixo está a visualização da interação entre **EC2, AMI, EBS, Snapshots e Security Groups**:

[Diagrama AWS]

<img width="632" height="425" alt="Image" src="https://github.com/user-attachments/assets/2546223a-fff7-4d2d-80d6-c0b5a04d6ffe" />



- Criação da instância EC2
- Configuração de segurança
- Snapshot EBS
- AMI personalizada

---

## 🌟 Insights Pessoais

- O uso de **snapshots** simplifica backups e restaurações rápidas.
- As **AMIs** permitem replicar ambientes de forma ágil, economizando tempo em implantações.
- Gerenciar **Security Groups** corretamente é essencial para segurança.
- A prática reforçou a importância da **escolha certa da família de instância** para otimização de custos e desempenho.

---

## 🔗 Referências

- [Documentação Oficial da AWS](https://docs.aws.amazon.com/)
- [DIO - Bootcamp Santander Code Girls](https://www.dio.me/)

---

✍️ **Autor:** Ingrid Dias  
📌 *Este repositório faz parte do desafio proposto pela DIO.*
