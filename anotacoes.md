# 📝 Anotações do Laboratório AWS EC2

Este documento registra o **passo a passo** das práticas realizadas durante o desafio, incluindo insights e comandos utilizados.

---

## 1. Criação da Instância EC2

1. Acesse o **Console AWS** → EC2.
2. Clique em **Executar instância**.
3. Configure:
   - **Nome**: `lab-ec2`
   - **AMI**: Amazon Linux 2
   - **Tipo de instância**: `t2.micro` (Free Tier)
   - **Par de chaves (Key Pair)**: criar/usar existente
   - **Rede**: VPC padrão
   - **Security Group**: liberar porta 22 (SSH)
4. Lançar instância.

📌 **Comando para conectar via SSH:**
```bash
ssh -i "minha-chave.pem" ec2-user@<IP_Público_da_Instância>
