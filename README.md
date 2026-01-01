# API com Swagger (Documentação Automatizada)

Este projeto foi desenvolvido durante o bootcamp CI&T: Back-end com Java & AWS, com foco em boas práticas de documentação de APIs REST.

## Funcionalidades
- Spring Web
- Spring Boot 4.0.1
- Swagger
- SpringDoc OpenAPI

## Como acessar a documentação:
Após rodar o projeto, a interface do Swagger estará disponível em: http://localhost:8083/swagger-ui/index.html

## Dica técnica para esse projeto
Para o Swagger funcionar no Spring Boot 4.0.1, verifique se no seu pom.xml:
```
    <dependency>
        <groupId>org.springdoc</groupId>
        <artifactId>springdoc-openapi-starter-webmvc-ui</artifactId>
        <version>2.3.0</version>
    </dependency> 
```

## Desafios Enfrentados e Aprendizados
Neste projeto, decidi aplicar a mesma estratégia de modernização utilizada em projetos anteriores para garantir a compatibilidade e segurança do ecossistema.

1. **O Desafio da Incompatibilidade:**
O maior obstáculo foi lidar com bibliotecas de documentação legadas (como o SpringFox) que não possuem suporte nativo para o Spring Boot 3/4 e o Jakarta EE. Ao tentar seguir o material original do curso com versões antigas, o sistema apresentou falhas críticas de inicialização.

2. **A Estratégia de Resolução**
Mantendo a consistência do meu portfólio, optei por:
* Recriar o projeto do zero utilizando Java 17 e Spring Boot 4.0.1, eliminando "lixo" de configurações de versões anteriores.
* Substituir o Swagger antigo pelo SpringDoc OpenAPI 2, que é a biblioteca padrão e atualizada para as versões mais recentes do Spring.

3. **O que aprendi no processo**
* **Evolução do Java**: Consolidei o conhecimento na transição do javax.* para o jakarta.*, entendendo como essa mudança impacta as dependências de API.
* **Documentação como Código**: Aprendi que manter a documentação da API atualizada (via Swagger) é tão importante quanto o código funcional, especialmente em arquiteturas de microserviços.
* **Gestão de Dependências**: Aprendi a analisar o pom.xml de forma crítica, identificando quais dependências são "starters" modernos e quais estão obsoletas.