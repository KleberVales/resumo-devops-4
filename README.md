# resumo-devops-4

## criar pipeline de build do OCI DevOps

Um **pipeline de build** no OCI DevOps é uma sequência de etapas automatizadas que transforma código-fonte em artefatos prontos para implantação. Ele permite compilar, testar, analisar e empacotar aplicações de forma segura e repetível.  
Principais pontos:

- Um pipeline pode incluir etapas como:
  - **Build gerenciado**: Compila o código e gera artefatos.
  - **Testes automatizados**: Executa testes unitários, integração ou de segurança.
  - **Verificação de código**: Analisa vulnerabilidades e falhas de qualidade.
  - **Exportar artefatos**: Envia os artefatos gerados para repositórios como OCI Object Storage, Container Registry ou Artifact Registry.
- Integração com **OCI Vault** para armazenar segredos, tokens ou credenciais de forma segura.
- Suporte a triggers automáticos a partir de commits em repositórios de código (OCI Code Repository, GitHub, GitLab).

---

## OCI Object Storage.

O **OCI Object Storage** é um serviço de armazenamento em nuvem escalável e durável para guardar dados não estruturados. É usado no contexto DevOps para:

- Armazenar artefatos de build e pacotes de software.
- Arquivar logs, backups ou arquivos de configuração.
- Servir como repositório intermediário para pipelines antes de enviar artefatos para produção.
- Permite integração com políticas de IAM para controle de acesso seguro.

---

## etapas da estratégia canary

 **estratégia Canary** permite implantar novas versões de uma aplicação gradualmente, reduzindo riscos de falha em produção. As etapas típicas incluem:

1. **Deploy Canary**: Implantação da nova versão em um subconjunto limitado de usuários ou instâncias.
2. **Validar**: Monitorar métricas de desempenho e erros da versão Canary.
3. **Shift Traffic**: Redirecionar o tráfego gradualmente para a nova versão conforme a validação positiva.
4. **Production**: Completar a implantação para todo o ambiente de produção.
5. **Rollback** (opcional): Reverter para a versão anterior em caso de problemas detectados durante a validação.

---

## estrutura do Dockerfile

Um **Dockerfile** é um arquivo de configuração declarativo usado para criar imagens de containers. Estrutura básica:

- **FROM**: Define a imagem base.
- **WORKDIR**: Define o diretório de trabalho dentro do container.
- **COPY / ADD**: Copia arquivos do host para o container.
- **RUN**: Executa comandos durante a construção da imagem, criando camadas.
- **ENV**: Define variáveis de ambiente disponíveis durante build e execução.
- **CMD / ENTRYPOINT**: Define o comando padrão ou ponto de entrada do container.
- **EXPOSE**: Informa quais portas serão usadas pelo container.
- **VOLUME**: Define volumes para persistência de dados.



