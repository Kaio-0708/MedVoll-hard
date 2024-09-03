# Projeto Voll.med API

A API Voll.med é uma aplicação desenvolvida em Java usando Spring Boot que fornece funcionalidades para gerenciar médicos e pacientes em um sistema de saúde. A aplicação inclui segurança baseada em JWT e interações com o banco de dados usando JPA/Hibernate.

## Estrutura do Projeto

### Pacotes e Classes

- **`med.voll.api.domain.medico`**: Contém classes e registros relacionados a médicos.
  - `DadosAtualizacaoMedico`: Dados para atualizar informações de um médico.
  - `DadosCadastroMedico`: Dados para cadastrar um novo médico.
  - `DadosListagemMedico`: Dados para listar médicos.
  - `DadosDetalhamentoMedico`: Dados para detalhar um médico.
  - `Especialidade`: Enum que define as especialidades médicas.
  - `Medico`: Entidade JPA representando um médico.
  - `MedicoRepository`: Interface JPA para operações CRUD em médicos.

- **`med.voll.api.domain.paciente`**: Contém classes e registros relacionados a pacientes.
  - `DadosAtualizacaoPaciente`: Dados para atualizar informações de um paciente.
  - `DadosCadastroPaciente`: Dados para cadastrar um novo paciente.
  - `DadosDetalhamentoPaciente`: Dados para detalhar um paciente.
  - `DadosListagemPaciente`: Dados para listar pacientes.
  - `Paciente`: Entidade JPA representando um paciente.
  - `PacienteRepository`: Interface JPA para operações CRUD em pacientes.

- **`med.voll.api.domain`**: Contém classes de domínio geral.
  - `ValidacaoException`: Exceção personalizada para validação.

- **`med.voll.api.infra.exception`**: Contém classes para tratamento de exceções.
  - `TratadorDeErros`: Controlador global para tratar exceções e erros de validação.

- **`med.voll.api.infra.security`**: Contém classes relacionadas à segurança e autenticação.
  - `DadosTokenJWT`: Registro para armazenar o token JWT.
  - `SecurityConfigurations`: Configurações de segurança Spring.
  - `SecurityFilter`: Filtro de segurança para validação de tokens JWT.
  - `TokenService`: Serviço para gerar e validar tokens JWT.

## Funcionalidades

### Médico

- Cadastro, atualização e listagem de médicos.
- Detalhamento de médicos.
- Escolha de médicos disponíveis para consultas com base em especialidade e data.
- Exclusão lógica de médicos.

### Paciente

- Cadastro, atualização e listagem de pacientes.
- Detalhamento de pacientes.
- Exclusão lógica de pacientes.

### Segurança

- Autenticação baseada em JWT.
- Proteção de endpoints com filtros de segurança.
- Configurações para desativar CSRF e gerenciar sessões de forma estateless.

## Configuração

### Dependências

O projeto utiliza as seguintes dependências:

- Spring Boot
- Spring Security
- Spring Data JPA
- JWT (Auth0)
- PostgreSQL

### Propriedades de Configuração

As propriedades de configuração do projeto estão localizadas no arquivo `application.properties`. Certifique-se de definir o segredo do token JWT e as configurações do banco de dados.

### Exemplos de Configuração

```properties
api.security.token.secret=YOUR_SECRET_KEY
spring.datasource.url=jdbc:postgresql://localhost:5432/yourdb
spring.datasource.username=yourusername
spring.datasource.password=yourpassword
```

## Execução

Para executar o projeto, siga os passos abaixo:

1. Clone o repositório:

    ```bash
    git clone https://github.com/seu-usuario/seu-repositorio.git
    ```

2. Navegue até o diretório do projeto:

    ```bash
    cd seu-repositorio
    ```

3. Compile e execute a aplicação:

    ```bash
    ./mvnw spring-boot:run
    ```

## Contribuições

Sinta-se à vontade para contribuir com melhorias, correções de bugs ou novas funcionalidades por meio de pull requests.

## Autor

Kaio Vitor - [GitHub](https://github.com/Kaio-0708)
