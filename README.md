# Terraform Azure Storage Account

## Projeto: Terraform para criação de conta de armazenamento na Azure

Este projeto fornece um modelo do Terraform para provisionar uma conta de armazenamento do Azure. Ele inclui recursos para criar uma conta de armazenamento, contêineres de armazenamento e um conjunto de regras de acesso a contas.

## Pré-requisitos

- Uma assinatura ativa do Azure.
- Instalação do Terraform na máquina local.
- Configuração da autenticação com o Azure (pode ser feita através do arquivo de credenciais ou variáveis de ambiente)
- az login

## Utilização

1. Clone o repositório para a sua máquina local.
2. Acesse o diretório do projeto e crie um arquivo `variables.tf` com as seguintes variáveis:

- `subscription_id`: ID da sua assinatura do Azure.
- `client_id`: ID do cliente da sua conta do Azure.
- `client_secret`: Segredo do cliente da sua conta do Azure.
- `tenant_id`: ID do locatário da sua conta do Azure.
- `storage_account_name`: Nome desejado para a conta de armazenamento.

3. Execute o comando `terraform init` para baixar e configurar os módulos necessários.
4. Execute o comando `terraform plan` para verificar as alterações que serão feitas na sua conta do Azure.
5. Execute o comando `terraform apply` para realizar a implantação.
6. Execute o comando `terraform destroy` para realizar a destruição da infraestrutura e não gerar possíveis custos.

## Observações

- O Terraform irá criar uma conta de armazenamento com tipo de armazenamento padrão (`Standard_LRS`) e um container padrão (`$web`)
- Também é possível especificar outros parâmetros e recursos adicionais na configuração do Terraform, como região, grupo de recursos, etc.
- Depois de rodar o terraform apply, você pode usar o comando terraform show para verificar todas as infomrações sobre a conta de armazenamento.

## Notas finais

Este modelo fornece uma configuração básica para a criação de uma conta de armazenamento do Azure. Ele pode ser modificado para incluir mais recursos e configurações conforme necessário. Certifique-se de testar sua configuração em um ambiente de teste antes de aplicá-la em um ambiente de produção.
