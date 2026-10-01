# Entrega — Prova do Primeiro Bimestre (DevOps)

**Aluno:** Gabriel de Souza Oliveira  
**RA:** 6325262  
**Data:** [DATA DA PROVA]  
**Ferramentas de IA utilizadas:** Claude e Kiro

## Repositório do Projeto

- URL: https://github.com/biel334/prova-primeiro-bimestre-devops

## Checklist de Evidências

- [x] Repositório público com README (nome + RA) e .gitignore
- [x] Mínimo de 6 commits com Conventional Commits + feature branch
- [x] API com **CRUD completo** de reservas (POST, GET, GET/:id, PUT, DELETE) + /health
- [x] Rotas de CRUD gravando no **banco PostgreSQL** (não em memória)
- [x] Dockerfile funcional da API de Reservas
- [x] docker-compose.yml (API + PostgreSQL) subindo com um comando
- [x] Terraform modularizado (vpc, security-group, ec2, rds)
- [x] **RDS PostgreSQL provisionado** nas subnets privadas (banco da API na nuvem)
- [x] Remote State configurado (S3 + DynamoDB)
- [x] Uso de LabRole/LabInstanceProfile (sem criar IAM próprio)
- [x] terraform validate e terraform plan sem erros
- [x] relatorio.md completo (4 questões)
- [x] terraform destroy executado após evidências

## Evidências

Todas em https://github.com/biel334/prova-primeiro-bimestre-devops/tree/main/evidencias

- `docker-build.txt`: build da imagem e container rodando como usuário não-root (`appuser`)
- `compose-ps.txt`: `docker compose ps` com API e PostgreSQL `healthy`, volume nomeado, rede bridge e CRUD local
- `terraform-plan.txt`: plan com 18 recursos a criar
- `terraform-apply-e-recursos.txt`: outputs, state, RDS (`PubliclyAccessible = False`, `StorageEncrypted = True`) e state remoto no S3
- `api-nuvem.txt` e `api-nuvem-crud.txt`: API na EC2 com o CRUD completo gravando no RDS
- `terraform-destroy.txt`: 18 recursos destruídos
- `screenshots-crud/`: capturas de tela do CRUD

Relatório: https://github.com/biel334/prova-primeiro-bimestre-devops/blob/main/relatorio.md1
