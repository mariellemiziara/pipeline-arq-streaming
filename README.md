# pipeline-arq-streaming

Provisionamento de Infraestrutura 
Automatizada (3)
 Objetivo: Criar e gerenciar a infraestrutura da PetAdota de forma automatizada 
usando Terraform e Ansible.
 Tarefas do Exercício:
 Criar um bucket no GCP para armazenar imagens dos animais.
 Provisionar uma máquina virtual Linux para hospedar o banco de dados.
 Instalar e configurar um banco MySQL na VM automaticamente via Ansible.
 Criar o banco de dados Pet_Adota e a tabela animais_disponiveis com as colunas:
 • id (identificador único)
 • raca (raça do animal)
 • url (URL da imagem armazenada no S3)
 • tipo (cachorro ou gato)
 Criar um usuário de consulta que pode ler os dados mas não alterar.
 Validar a estrutura do banco acessando via MySQL console.
Pipeline de Imagens da API para o Banco (3)
 Objetivo: Construir um pipeline automatizado para baixar imagens de animais, armazenar 
no S3 e registrar no banco MySQL.
 Tarefas do Exercício:
 Consultar as APIs de cães e gatos (Dog API e Cat API).
 Baixar as imagens e nomeá-las com um contador por raça (labrador_01.jpg).
 Salvar as imagens no S3, organizando por raça e tipo:
 • s3://pet-adota-imagens/cachorro/labrador/labrador_01.jpg
 • s3://pet-adota-imagens/gato/persa/persa_01.jpg
 Registrar os metadados no banco MySQL (Pet_Adota > animais_disponiveis).
 Criar um DAG no Airflow para rodar esse pipeline a cada 30 segundos.
Processamento de Interações de 
Usuários em Tempo Real (4)
 Objetivo: Criar um sistema de monitoramento de tendências de adoção em tempo 
real, utilizando Kafka e Spark Streaming.
 Tarefas do Exercício:
 Simular eventos de interação de usuários clicando nos perfis de animais no site.
 Publicar eventos no Kafka, contendo:
 • usuario_id (quem interagiu)
 • raca (raça do animal visualizado)
 • tipo (cachorro ou gato)
 • timestamp (horário da interação)
 Processar os eventos com Spark Streaming, identificando tendências:
 •Animais mais procurados no último minuto.
 •Horário de pico de visualizações.
 Salvar estatísticas no banco MySQL para análise futura.
 Criar um DAG no Airflow para visualizar as tendências a cada 30 segundos
