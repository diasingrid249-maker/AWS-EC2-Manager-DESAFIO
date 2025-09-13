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


2. Criação de uma AMI (Amazon Machine Image)

No Console, selecione a instância criada.

Clique em Ações → Imagem e modelos → Criar imagem.

Defina:

Nome: lab-ami

Descrição: AMI personalizada criada a partir da instância lab-ec2

Confirmar.

📌 Insight: AMIs permitem replicar rapidamente um ambiente já configurado.

3. Elastic Block Store (EBS)

No Console, vá em Volumes.

Clique em Criar volume.

Tipo: gp2

Tamanho: 8 GiB

Zona de disponibilidade: mesma da instância EC2

Anexar o volume à instância.

📌 Comando dentro da EC2 para verificar:

lsblk


📌 Montagem do volume:

sudo mkfs -t ext4 /dev/xvdf
sudo mkdir /meuvolume
sudo mount /dev/xvdf /meuvolume

4. Snapshots EBS

No Console, selecione o volume EBS.

Clique em Ações → Criar Snapshot.

Nome: lab-ebs-snapshot

Confirmar.

📌 Insight: Snapshots permitem backup incremental e podem ser usados para criar novos volumes.

5. Security Groups

Configuração inicial:

Porta 22 (SSH) → acesso remoto seguro

Porta 80 (HTTP) → caso hospede aplicações web

Prática recomendada: abrir apenas portas necessárias.

6. Insights Gerais

Snapshots simplificam backup e recuperação rápida.

AMIs otimizam o tempo ao replicar ambientes.

EBS garante persistência de dados, diferente do armazenamento efêmero da EC2.

Security Groups funcionam como firewall virtual.

✍️ Autora: Ingrid Dias
📌 Parte do Desafio DIO - Gerenciamento de Instâncias EC2 na AWS
ssh -i "minha-chave.pem" ec2-user@<IP_Público_da_Instância>
