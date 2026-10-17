# Changelog

Todas as mudancas notaveis deste repositorio serao documentadas neste arquivo.

O formato segue [Keep a Changelog](https://keepachangelog.com/pt-BR/1.1.0/).

## [1.0.0] - 2026-10-17

### Added
- `servico-dotnet.yml`: pipeline reutilizavel dos microsservicos .NET, com build, testes com cobertura e build da imagem em todo PR, e deploy no EKS (ECR, Secret do Secrets Manager, manifests via Kustomize e rollout) quando o chamador informa o ambiente. Nasceu do `deploy-eks.yml` do `tech-challenge-oficina-mecanica` (F4-08)
- Lint dos workflows com actionlint e check `Origem do PR` (F4-10)
