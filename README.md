InvestBot - Chatbot para Consultoria sobre Investimentos
Descrição
O InvestBot é um chatbot desenvolvido em Python utilizando a biblioteca Flask para fornecer informações sobre investimentos. Ele usa um modelo de aprendizado de máquina treinado com dados sobre várias opções de investimento no Brasil, como Tesouro Direto, CDI, previdência privada, entre outros. O bot é capaz de interagir com os usuários e fornecer respostas úteis para perguntas comuns relacionadas a finanças e investimentos.

Funcionalidades
Resposta Automática: O chatbot responde automaticamente às perguntas dos usuários sobre investimentos.
Integração com Flask: O chatbot é servido através de uma aplicação web em Flask.
Modelo de ML: Utiliza um modelo de aprendizado de máquina treinado para entender e responder a uma variedade de consultas financeiras.
Estrutura do Projeto
app.py: Arquivo principal que inicia o servidor Flask e processa as interações dos usuários.
trainning.py: Script utilizado para treinar o modelo de aprendizado de máquina, que é salvo em model.h5.
invest.json: Arquivo JSON contendo os dados de treinamento e as intenções usadas pelo chatbot.
templates/index.html: Interface de usuário simples para interagir com o chatbot via web.
Requisitos
Certifique-se de ter as seguintes dependências instaladas antes de executar o projeto:

Python 3.6 ou superior
Flask
Keras
NLTK
NumPy
Gunicorn (para execução em produção)
Você pode instalar as dependências necessárias com o seguinte comando:

bash
Copiar código
pip install -r requirements.txt
Configuração e Execução
Passo 1: Clonar o Repositório
Clone este repositório para a sua máquina local:

bash
Copiar código
git clone https://github.com/seu-usuario/investbot.git
cd investbot
Passo 2: Treinar o Modelo
Se você precisar treinar o modelo novamente, execute o seguinte comando:

bash
Copiar código
python3 trainning.py
Isso gerará os arquivos model.h5, texts.pkl, e labels.pkl, que serão usados pelo chatbot para responder às perguntas.

Passo 3: Executar a Aplicação Flask
Para rodar o servidor Flask em modo de desenvolvimento, execute:

bash
Copiar código
python3 app.py
Isso iniciará o servidor em http://localhost:5000.

Passo 4: Servir o Aplicativo em Produção
Para rodar o chatbot em um ambiente de produção, é recomendado usar Gunicorn:

bash
Copiar código
gunicorn -w 4 -b 0.0.0.0:8081 app:app
Você pode então configurar um servidor web como Nginx para atuar como proxy reverso, servindo o chatbot em um domínio específico.

Interface de Usuário
A interface de usuário é construída em HTML e CSS, com interações realizadas através de JavaScript e jQuery. A UI é simples e intuitiva, permitindo aos usuários interagir com o bot diretamente no navegador.

Exemplo de Uso
Acesse o chatbot através do endereço http://investbot.tech e faça perguntas como:

"O que é Tesouro Direto?"
"Como investir no Tesouro Direto?"
"Quais são as opções de investimento?"
O bot responderá com informações úteis baseadas nos dados de treinamento.

Contribuição
Contribuições são bem-vindas! Se você tiver sugestões, melhorias ou quiser corrigir algum bug, sinta-se à vontade para abrir um Pull Request ou uma Issue.

Passos para Contribuir
Fork o Repositório
Crie um Branch: git checkout -b minha-nova-funcionalidade
Faça as Modificações e Commit: git commit -m 'Adicionei uma nova funcionalidade'
Envie para o Branch: git push origin minha-nova-funcionalidade
Abra um Pull Request
Licença
Este projeto é licenciado sob os termos da licença MIT. Veja o arquivo LICENSE para mais detalhes.

