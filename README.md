# motor-fraude-parent

Pom pai dos serviços do motor de detecção de transações suspeitas: versões do Spring Boot e das bibliotecas, `pluginManagement`, regras do enforcer (Java 21, Jackson 3, convergência de dependências) e Jacoco.

Repositório de visão geral, specs e infraestrutura local: https://github.com/luizavramos/motor-fraude

## Publicar
```bash
./mvnw install     # local (~/.m2)
./mvnw deploy      # GitHub Packages (precisa do token, ver abaixo)
```

## Token do GitHub Packages
Os repositórios são privados, então ler e publicar artefatos exige um token pessoal com `read:packages` (e `write:packages` para publicar). Em `~/.m2/settings.xml`:
```xml
<settings><servers><server>
  <id>github-motor-fraude</id><username>SEU_USUARIO</username><password>SEU_TOKEN</password>
</server></servers></settings>
```
Sem registry, instale localmente na ordem: motor-fraude-parent, contracts, platform-commons.
