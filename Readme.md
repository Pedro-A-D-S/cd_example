<h1>Flask CD Pipeline Simples</h1>

<p>Este repositório contém os passos para configurar uma pipeline de Integração Contínua (CI) e Entrega Contínua (CD) para um aplicativo Flask usando GitHub Actions e DockerHub.</p>

<details>
<summary><strong>Passos</strong></summary>

<ol>
<li><strong>Configurar Conta e Repositório GitHub</strong><br>
Crie uma conta no GitHub, se ainda não tiver uma, e crie um novo repositório. Esse repositório será usado para hospedar o código-fonte do seu aplicativo.</li>

<li><strong>Configurar Conta DockerHub</strong><br>
Crie uma conta no DockerHub, caso ainda não tenha uma. O DockerHub será usado para hospedar as imagens do seu aplicativo.</li>

<li><strong>Criar Ambiente Virtual</strong><br>
Crie um ambiente virtual para isolar as dependências do seu aplicativo Flask.<br>
<code>python3 -m venv env</code></li>

<li><strong>Ativar Ambiente Virtual</strong><br>
Ative o ambiente virtual.<br>
<code>source env/Scripts/activate</code></li>

<li><strong>Instalar Flask</strong><br>
Instale o Flask dentro do ambiente virtual.<br>
<code>pip install flask</code></li>

<li><strong>Gerar Lista de Dependências</strong><br>
Crie um arquivo <code>requirements.txt</code> para listar as dependências instaladas.<br>
<code>pip freeze > requirements.txt</code></li>

<li><strong>Configurar Variáveis Secretas</strong><br>
No GitHub, vá para as Configurações do Repositório e adicione suas variáveis secretas: <code>DOCKER_USERNAME</code>, <code>DOCKER_PASSWORD</code> e <code>DOCKERHUB_REPO</code>. Isso permitirá que a pipeline acesse seu DockerHub.</li>

<li><strong>Configurar Fluxo de Trabalho CI/CD</strong><br>
No repositório do GitHub, vá para a aba "Actions" e configure um novo fluxo de trabalho. Escolha a opção "Publish Python package" e siga as instruções para configurar o arquivo de fluxo de trabalho.</li>

<li><strong>Adicionar Arquivo de Configuração CD</strong><br>
No arquivo de descrição do fluxo de trabalho, adicione o conteúdo do arquivo <code>cd_config.yml</code> para definir a etapa de entrega contínua.</li>

<li><strong>Enviar Alterações para o Repositório</strong><br>
Envie as alterações para o repositório usando os comandos git.<br>
<code>git add .</code><br>
<code>git commit -m "adicionado código do app"</code><br>
<code>git push</code></li>

<li><strong>Verificar a Imagem no DockerHub</strong><br>
Acesse o DockerHub para verificar a imagem recém-criada e servida do seu aplicativo Flask!</li>
</ol>

<p>Siga esses passos para configurar uma pipeline completa de CD para o seu aplicativo Flask. Isso permitirá que você automatize a construção, testes e implantação do seu aplicativo, tornando o processo de desenvolvimento mais eficiente e confiável.</p>

</details>
