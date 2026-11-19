# Avaliação 02 - Relatório de evidências

Estudante:Lucas Machacado Floriano
Turma: ADS(Analise e desenvolvimento de sistemas) fase 4  Data: 18/11/2026
Identificador AV02_ID: luke_1   Porta utilizada: 8080

## E01 - Preparação / configuração válida
- Comandos executados:docker compose version, docker compose conifg --quiet, docker compose up -d --build e docker compose ps
- Saída relevante (retire qualquer senha real):
- Evidência anexada: E01.png, E01_2.png e E01_3.png

## E02 - Configuração segura do Compose
- Alterações no compose.yaml e .env.example: APP_PORT alterado e security_opt e cap_drop no compose.yaml
- Como conferi que backend e db não publicam portas no host: 
- Evidência anexada: E02.png, E02_2.png

## E03 - Liveness, readiness e healthcheck
- Respostas HTTP normais observadas: não conectou ao servidor
- Arquivos alterados: app.py e compose.yml
- Evidência anexada: E03.png

## E04 - Integração
- Título único da tarefa: AV02-<luke_1>-integracao
- POST: código HTTP e trecho da resposta:
- GET ou tela da tarefa:
- Caminho da requisição browser > ... > banco:

## E05 - Persistência
- ID/título antes do down: luke_1
- Comandos utilizados, sem -v: docker compose down e docker compose up -d
- Evidência do mesmo registro após up: não conectou ao servidor

## E06 - Falha controlada e recuperação
- Com db parado: /api/live = respondeu que não conectou no servidor e /api/ready = respondeu que não conectou no servidor
- Qual log ou sinal investiguei:
- Após o start do db: /api/ready = não consegiu conectar
- Evidência anexada: E06.png

## E07 - Justificativa técnica
1. Por que somente o frontend publica uma porta no host?
Resposta:

2. Por que .env não deve ser tratado como cofre de segredos?
Resposta:

3. depends_on: service_healthy resolve indisponibilidade posterior do banco?
Resposta: Não

4. Volume nomeado é o mesmo que backup externo? Justifique.
Resposta:

## Checklist final
- [X] compose.yaml final
- [X] backend/app.py final
- [X] .env.example com valores estritamente fictícios
- [X] relatorio_evidencias.md preenchido
- [] Evidências E01-E06
- [X] Sem .env nem dados sensíveis
