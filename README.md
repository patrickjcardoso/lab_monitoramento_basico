> Status: Developing 


## Descrição do laboratório:

Este é um laboratório básico para compreender como fazer a monitoração de recursos de um servidor linux.


## Technologies Used:

* Linux (Ubuntu based)
* Docker
* Prometheus
* Grafana


## Como rodar o laboratório:

1. Configuração do ambiente:

   * Em um servidor ou máquina Linux, você precisa ter instalado o Docker e o Docker Compose para subir os containers.

2. Clone o repositório:

    * Utilize o comando abaixo para clonar o repositório:
  
        `git clone https://github.com/patrickjcardoso/lab_monitoramento_basico.git`

3. Acesse o diretório e liste os arquivos:

        cd lab_monitoramento_basico
        ls -l

4. Inicialize os containers:

        `docker-compose up -d`

5. Acessar o Prometheus

    * Abra um navegador da web e acesse http://localhost:9090.
    * Você será redirecionado para a interface do Prometheus.

6. Configurar o Grafana

   * Abra um navegador da web e acesse http://localhost:3000.
   * Faça login no Grafana usando as credenciais padrão (usuário: admin, senha: admin).
   * Você será solicitado a alterar a senha após o primeiro login.
   * Após fazer login e alterar a senha, você será redirecionado para a interface do Grafana.

7. Adicionar o Prometheus como uma fonte de dados no Grafana

   * Na interface do Grafana, clique em "Configuration" (no ícone de engrenagem) e selecione "Data Sources".
   * Clique em "Add data source".
   * Selecione "Prometheus" como o tipo de fonte de dados.
   * Em "HTTP URL", insira http://prometheus:9090 e clique em "Save & Test".

8. Importar uma dashboard no Grafana

   * Após fazer login no Grafana e acessar a interface, você verá uma barra lateral à esquerda. Role a barra lateral até o topo e você encontrará o ícone "+" no canto superior direito. Clique nesse ícone para criar um novo painel.
   * Na nova página, você verá uma opção para importar uma dashboard. Clique em "Import".
   * Agora você tem duas opções para importar a dashboard: carregar um arquivo JSON ou inserir o ID da dashboard.
   * Se você tiver um arquivo JSON com a definição da dashboard pronta, clique em "Upload .json file" e selecione o arquivo no seu computador.
   * Se preferir utilizar um dashboard pronto da comunidade Grafana, você pode buscar no Grafana Dashboard Library em https://grafana.com/grafana/dashboards.
   * Após escolher e baixar a dashboard desejada, volte à interface do Grafana e clique novamente no ícone "+" para criar um novo painel. Em seguida, clique em "Import" e selecione a opção de carregar um arquivo JSON.
   * No campo "Upload .json file", clique em "Upload JSON file" e selecione o arquivo JSON da dashboard que você baixou.
   * O Grafana irá analisar e importar a dashboard. Em seguida, você pode personalizar o painel, configurar os painéis e gráficos de acordo com suas necessidades específicas. 