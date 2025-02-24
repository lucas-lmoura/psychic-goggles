## Executando

Baixe e instale a _aws-cli_ disponível em:

```bash
  https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html
```

Após a instalação execute o seguinte comando e informe dados fictícios:

```bash
  aws configure
```

Crie uma códia do env.example

```bash
  cp .env.example .env
```

Informe as credenciais criadas anteriormente, serviços, a porta onde o serviço irá executar e por fim basta subir o container.

```bash
  docker compose up
```

## Verificando o serviço pelo terminal

Utilizando o S3 como exemplo e o serviço rodando na porta 4566:

```bash
  aws s3api create-bucket --bucket localdev --region us-east-1  --endpoint-url=http://localhost:4566
```

Verificando a existência do bucket:

```bash
  aws s3 ls --endpoint-url=http://localhost:4566
```
