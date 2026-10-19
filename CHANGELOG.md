# Changelog

Todas as mudancas notaveis deste repositorio serao documentadas neste arquivo.

O formato segue [Keep a Changelog](https://keepachangelog.com/pt-BR/1.1.0/).

## [1.1.0] - 2026-10-17

### Added
- Analise e quality gate do SonarCloud no job `Build and tests`, ativados pelo segredo `SONAR_TOKEN` do chamador; gate reprovado falha o job e bloqueia o deploy. Entradas `sonar_organizacao`, `sonar_projeto` e `sonar_exclusoes` (F4-09)

### Changed
- Cobertura gerada em Cobertura e OpenCover, independentemente do `coverlet.runsettings` do servico
- Checkout com historico completo, para o SonarCloud separar o codigo novo

## [1.0.0] - 2026-10-17

### Added
- `servico-dotnet.yml`: pipeline reutilizavel dos microsservicos .NET, com build, testes com cobertura e build da imagem em todo PR, e deploy no EKS (ECR, Secret do Secrets Manager, manifests via Kustomize e rollout) quando o chamador informa o ambiente. Nasceu do `deploy-eks.yml` do `tech-challenge-oficina-mecanica` (F4-08)
- Lint dos workflows com actionlint e check `Origem do PR` (F4-10)
