# Infraestrutura como Código

Repositório base para o desenvolvimento de um pipeline que provisiona um recurso (arquivo de texto) através de código.

A Infraestrutura como Código (IaC) nos permite gerenciar e provisionar recursos de maneira reproduzível e escalável, reduzindo erros humanos e garantindo consistência entre diferentes ambientes.

## Comandos Básicos do Terraform

- **`terraform init`**  
  Inicializa o diretório de trabalho com os arquivos de configuração do Terraform. É o primeiro comando que deve ser executado antes de usar `plan` ou `apply`.

- **`terraform validate`**  
  Verifica se os arquivos de configuração possuem sintaxe correta e estão prontos para uso.

- **`terraform plan`**  
  Gera e exibe um plano de execução, detalhando as mudanças que serão feitas na infraestrutura.

- **`terraform apply`**  
  Aplica as mudanças especificadas no plano para provisionar ou modificar os recursos.

- **`terraform destroy`**  
  Remove os recursos gerenciados pelo Terraform, garantindo a limpeza do ambiente.

## Exercícios Propostos

1. **Configurar um projeto Terraform básico:**  
   Completar a estrutura fornecida no repositório para criar um arquivo local chamado `exemplo.txt`. Personalizar o nome e o conteúdo do arquivo utilizando variáveis (variables.tf) no Terraform.

2. **Executar o pipeline GitLab:**  
   Validar, planejar e aplicar as configurações no pipeline do GitLab, observando as suas etapas de execução.

3. **Validar o artefato gerado:**  
   Realizar o download do arquivo `exemplo.txt`, gerado como artefato do pipeline, e confirmar que seu conteúdo está de acordo com as configurações no Terraform.

## Executando o Projeto Localmente

Caso tenha o Terraform client instalado localmente, você pode executar os passos a seguir para reproduzir a prática:

1. **Inicializar o Terraform:**
   ```
   terraform init
   ```

2. **Validar os arquivos de configuração:**
   ```
   terraform validate
   ```

3. **Planejar a execução da infraestrutura:**
   ```
   terraform plan -out=plan.out
   ```

4. **Aplicar as configurações para criar o arquivo:**
   ```
   terraform apply -auto-approve plan.out
   ```

5. **Verificar o arquivo gerado:**
   O arquivo `exemplo.txt` será criado no diretório local.

## Novo Licenciamento do Terraform

O **Open Tofu** é um fork do Terraform, criado após a migração do Terraform para a licença Business Source License (BSL). Ele mantém a compatibilidade total com os arquivos de configuração do Terraform e utiliza os mesmos comandos (`tofu init`, `tofu plan`, `tofu apply`), tornando a migração transparente para usuários. Licenciado sob Apache 2.0, o Open Tofu é uma solução comunitária que preserva os valores do código aberto.