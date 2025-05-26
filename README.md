## Documentação 📚

## Visão geral do produto 🖥️

Chronos é uma aplicação web que simplifica o gerenciamento de ponto online, oferecendo funcionalidades completas para controle de jornada de trabalho.
Permite o registro de ponto online, cálculo automático de horas, gestão de ausências e geração de relatórios detalhados.
A interface intuitiva do Chronos facilita o acompanhamento da jornada de trabalho.

---

## Problema do cliente 👔

### Desafios Atuais:

* Controle manual de ponto, sujeito a erros e fraudes.
* Dificuldade no cálculo preciso de horas trabalhadas e extras.
* Falta de visibilidade sobre a jornada de trabalho dos funcionários.
* Processos burocráticos para gestão de ausências.
* Dificuldade na geração de relatórios para análise de dados.
* Não conformidade com a legislação trabalhista.

### Necessidades:

Automatizar o controle de ponto para aumentar a precisão e reduzir erros.
Obter cálculos precisos e automáticos de horas trabalhadas.
Melhorar a visibilidade da jornada de trabalho dos funcionários.
Simplificar a gestão de ausências com fluxos de aprovação.
Gerar relatórios personalizados para análise de dados.
Garantir a conformidade com a legislação trabalhista.

---

## Objetivo do produto 🎯

* Desenvolver uma aplicação web intuitiva e eficiente para o gerenciamento de ponto online.
* Permitir o registro preciso de ponto com diferentes opções.
* Oferecer cálculos automáticos de horas trabalhadas e extras.
* Simplificar a gestão de ausências com fluxos de aprovação.
* Fornecer relatórios detalhados.
* Garantir a segurança dos dados e a conformidade com a legislação.
* permitir o acesso remoto para funcionários e gestores.

---

## Relatório e detalhes de cada Sprint 📅

- Sprint 1: [Acessar](https://github.com/Tico1606/chronos-documentation/blob/main/documentation/sprints-reports/sprint-1.md)
- Sprint 2: [Acessar](https://github.com/Tico1606/chronos-documentation/blob/main/documentation/sprints-reports/sprint-2.md)
- sprint-3: [Acessar](https://github.com/Tico1606/chronos-documentation/blob/main/documentation/sprints-reports/sprint-3.md)

---

## Documentos do Produto

- Manual do Usuário: [Acessar](https://github.com/Tico1606/chronos-documentation/blob/main/documentation/documents/chronos-manual-de-usuario.doc)

- Documento do Produto: [Acessar](https://github.com/Tico1606/chronos-documentation/blob/main/documentation/documents/documento-do-produto.docx)

---

## Como Executar Localmente no Windows 🖥️

### Pré-requisitos

Antes de começar, certifique-se de que você tem o seguinte instalado em sua máquina Windows:

1. **Node.js**: Baixe e instale o Node.js a partir de [nodejs.org](https://nodejs.org/). Isso também instalará o npm (Node Package Manager).
2. **Git**: Baixe e instale o Git a partir de [git-scm.com](https://git-scm.com/).
3. **Um editor de código**: Você pode usar qualquer editor de código, mas o Visual Studio Code é recomendado. Baixe-o em [code.visualstudio.com](https://code.visualstudio.com/).
4. **Maven**: Caso você não tenha extensões no Visual Studio Code, você pode usar um compilador para conseguir rodar o projeto, como o Maven.
5. **Docker**: É necessário ter o docker desktop para rodar o projeto, apenas com ele isntalado no computador e iniciado será o suficiente.

### Passo 1: Clonar os Repositórios

Abra o seu prompt de comando (cmd) ou PowerShell e execute o seguinte comando para clonar os repositórios:

```bash
git clone https://github.com/CtrI-Alt-Del/chronos-frontend.git
git clone https://github.com/CtrI-Alt-Del/chronos-backend.git
```

### Passo 2: Navegar até o Diretório do Projeto

Mude para o diretório do projeto:

```bash
cd chronos-frontend
cd chronos-backend
```

Obs: É necessário rodar os 2 repositórios juntos.

### Passo 3: Instalar Dependências no Frontend

Execute o seguinte comando para instalar as dependências necessárias no repositório do frontend:

```bash
npm install
```

### Passo 4: Configurar Variáveis de Ambiente do SERVIDOR e do CLIENTE:

1. **Localize o arquivo `.env.example`** na raiz do seu diretório do projeto. Este arquivo contém exemplos de variáveis de ambiente que você precisa configurar.
2. **Crie um novo arquivo chamado `.env`** no mesmo diretório que o `.env.example`.
3. **Copie o conteúdo do `.env.example`** para o novo arquivo `.env`.
4. **Atualize os valores** no arquivo `.env` de acordo com sua configuração local. Aqui está um exemplo de como o arquivo `.env` pode parecer:

#### Variáveis de Ambiente do SERVIDOR:

```
DATABASE_SOURCE_URL=
DATABASE_USERNAME=
DATABASE_PASSWORD=
WEB_APP_URL=
JWT_SECRET=
```

#### Variáveis de Ambiente do CLIENTE:

```
NEXT_PUBLIC_WEB_APP_URL=
NEXT_PUBLIC_SERVER_APP_URL=
```

Certifique-se de substituir os valores de espaço reservado pelos seus dados reais.


### Passo 5: Executar o Projeto

Após configurar as variáveis de ambiente, você pode executar o projeto usando o seguinte comando na pasta `chronos-backend`:

```bash
docker compose up -d
```

Obs: Se for sua primeira vez rodando o container, abra o application.properties, que está dentro de resources, dentro de main e subustita a configuração dessas 2 linhas para essas:

spring.jpa.hibernate.ddl-auto=create
database.seed.enabled=true

```bash
mvnw.cmd spring-boot:run
```

Se estiver no PowerShell:

```bash
./mvnw.cmd spring-boot:run
```

Obs: Se precisar apenas compilar o projeto antes de rodá-lo, use:

```bash
./mvnw.cmd compile
```

Na pasta `chronos-frontend`:

```bash
npm run dev
```

Este comando iniciará a aplicação, e você deverá ver uma saída indicando que a aplicação cliente e servidor está em execução.

### Passo 6: Acessar a Aplicação

Abra seu navegador e navegue até `http://localhost:3000` (ou a porta que você especificou no arquivo `.env`) para acessar a aplicação web.
Ou abra o navegador e navegue até `http://localhost:8080` (ou a porta que você especificou no arquivo `.env`) para acessar o servidor.

### Solução de Problemas

- Se você encontrar algum problema, verifique a saída do console para mensagens de erro.
- Certifique-se de que todas as variáveis de ambiente estão configuradas corretamente no arquivo `.env` tanto do cliente quanto do servidor.
- Verifique se seu banco de dados e quaisquer outros serviços estão em execução, caso sua aplicação dependa deles.
