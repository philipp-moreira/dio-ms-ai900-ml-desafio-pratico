# dio-ms-ai900-ml-desafio-pratico
Repositório contendo roteiro passo-a-passo para criar um Modelo de previsão usando o Azure Machine Learning Studio.

## Objetivo

## Pré-requisito

Como pré-requisito é necessário possuir uma conta criada e funcional na [Azure](https://portal.azure.com/?quickstart=True#home).

Como criar a sua conta (gratuíta) ?<br>

  01 - Acesse a [página](https://azure.microsoft.com/pt-br/free/search/?ef_id=_k_CjwKCAiA8YyuBhBSEiwA5R3-EyxckFGkfk85I8455z8A8V9SEQ4rDamiBh29pzPeSy5ADC1geYuP7hoCVIAQAvD_BwE_k_&OCID=AIDcmmzmnb0182_SEM__k_CjwKCAiA8YyuBhBSEiwA5R3-EyxckFGkfk85I8455z8A8V9SEQ4rDamiBh29pzPeSy5ADC1geYuP7hoCVIAQAvD_BwE_k_&gad_source=1&gclid=CjwKCAiA8YyuBhBSEiwA5R3-EyxckFGkfk85I8455z8A8V9SEQ4rDamiBh29pzPeSy5ADC1geYuP7hoCVIAQAvD_BwE)

  02 - Clique em **Experimente gratuitamente**
![image](https://github.com/philipp-moreira/dio-ms-ai900-ml-desafio-pratico/assets/17642499/08bfb1e9-14d1-43a4-bcb4-61c64b24c900)

  03 - Você será redirecionado para [página\(abaixo\)](https://login.microsoftonline.com/organizations/oauth2/v2.0/authorize?client_id=8e0e8db5-b713-4e91-98e6-470fed0aa4c2&response_type=code%20id_token&scope=openid%20profile&state=OpenIdConnect.AuthenticationProperties%3DtgIM8fUAqWeFNuvBd5GgL10awhlqhovrf_LeaF_V98VPjWvVVvh2l9wKa-TrmbYJkc5Qc0FyajfyI5oeDXhqUK3jq3J9KPIMVyBIqbDpKgLZ9OiladetOb9xfipP-LuLXa1ZvHmnx5VVmbWufDcTnUHnKZi842K2G2KMO3NoPmdYptG07X_VQuMEe0PBVLCv4wCg2402VAfBdrlkj4Zmj4XlXttNbbzLpEVUazwaUiF7pyLsphYwL6yukZglxfwmOrsLM143q55SR8rcde7Bl7onUiPYDMnODPWXibG8KhX8es6YLk-ETzUhQevJ4iSOmkpXRr9eC6r05WWRMe79zP-7qtfuuNcjcRQ3gBoehTjy92nVEImQBeFUueuTwuRBzIcwmLamlq0q7rlaNfYxhlR3HdRkTLu9J5kIWVxLi_7cuo9jG0sZgxJkSU9E3l67t7eI-HwiwGcLqkgFyNeKzGFYJ8SOC6luw27lLZ9KJ2XOWWWsZCsMpHJNaRPZna-kscK7tQRLAbJF-TH2OAOJoeypVbeWkvvS9yDOz6lORRrTvjTiBDC61jAZN0ZVXBhgw0sA61h8CO4ikIG_dMASZfC73qW12-u6QuLOoIHODOgmBxPsbzLT2cwTagbMufnr14hY4Dw2J1YomUKAE400RYrUxloEbh5xwZ5ifFSUuVLeixYtnON7bckL9eDqJ9CDc60xdnRF6HvFSWA_FxoK3zWCAxkF6z6FT8XJ068z8RWK0EpCZhKvhB-nKPsitDminmf5nwgdkY6m01Mnv7EAvZD4-OMzAND_14gNhN8B--nZrqKE1GEqiKfupkUtQWf94y7tXzlmBSEGe2uCBdmZkVe2UN9jxLR7ZRMzWGsVyKU5K3Ibw-HGcYaZDctMXRFrDaJF5N6OaN9tiTQ279Qb5PdNsb6nK0W2JrAgZkMo6txZIXhjQ1Z3r57W-vwU7AvpYNB4p9E3b17v-7LPZ_5QJILZaJZ_s_sf1mHh62hAINGfEpsuZKDrQ9-9rILdKX1JQiQlYietTOmKzF3bHk747LYWqtRy5sOayt1fyQgF5IvfiDVMz2KOsnOZGBH1R1FNTBKKZLt8fPDXw01sWsnsByhbmSuWTAQoRSWPJOy_gLx-tFBCI0DrTx2mFp_JuopusiE0J6bBm-coigEQBfUa57k-3endmqockVvi1892dPxvUHSS3pE4Bv8aB0nhq5s1pMjaCTVRosZncZfwkpapUg-joaWGaJ1xoO_rxXXocrjdaMKC3ko0l7YGhuCSmbr2-5pjITW6MmUBOdX0kymnpGNVWiTXC75a3d9UlKQOBe_z3Z9gPhHayCZDlMqzttja8ehvRid36s08fAf9er5Wz4As6NZgXBYfY1YXe4mWEn9PBcf7Tzya1c76qNIPlgj5LwqMqwOZDUUrbjooTRbrKg&response_mode=form_post&nonce=638429565329591794.NjVhYzg0ZjItM2U0My00MDY1LWEyODAtMzI3ZjZkNzQ5YmI4ZDgxNzA2NWYtODhmZS00MGQ2LTkxZWQtNGQ4ZDJmOTY1NTgy&redirect_uri=https%3A%2F%2Fsignup.azure.com%2Fapi%2Fuser%2Flogin&max_age=86400&post_logout_redirect_uri=https%3A%2F%2Fsignup.azure.com%2Fsignup%3Foffer%3Dms-azr-0044p%26appId%3D102%26ref%3D%26redirectURL%3Dhttps%3A%2F%2Fazure.microsoft.com%2Fget-started%2Fwelcome-to-azure%2F%26l%3Dpt-br%26srcurl%3Dhttps%3A%2F%2Fazure.microsoft.com%2Ffree%2Fsearch%2F%3Fef_id%3D_k_cjwkcaia8yyubhbseiwa5r3-eyxckfgkfk85i8455z8a8v9seq4rdamibh29pzpesy5adc1geyup7hocviaqavd_bwe_k_%26ocid%3Daidcmmzmnb0182_sem__k_cjwkcaia8yyubhbseiwa5r3-eyxckfgkfk85i8455z8a8v9seq4rdamibh29pzpesy5adc1geyup7hocviaqavd_bwe_k_%26gad_source%3D1%26gclid%3Dcjwkcaia8yyubhbseiwa5r3-eyxckfgkfk85i8455z8a8v9seq4rdamibh29pzpesy5adc1geyup7hocviaqavd_bwe&x-client-SKU=ID_NET472&x-client-ver=6.34.0.0), onde você vai ter as opções de loggin utilizando:

  - Sua conta de e-mail microsoft/outlook
  - Sua conta github

  Selecione a opção desejada e prossiga com seu login.
![image](https://github.com/philipp-moreira/dio-ms-ai900-ml-desafio-pratico/assets/17642499/40758dd3-93bc-46ee-ab6d-839ca04f62ac)

  04 - Logo após a autenticaçào, você vai visualizar duas opções, onde a primeira pede sua confirmação (marcando o checkbox) para o termos de planos do Azure e o segundo pede sua confirmação se deseja permitir à Microsoft compartilhar seu e-mail com parceiros comerciais e que provem produtos via plataforma da Azure, este segundo não é um item obrigatório, assim, fica a seu critério de como deseja seguir;

  05 - Mais abaixo dos dois checkbox citados no passo anterior, você irá visualizar o campo para selecionar ou cadastrar um cartão de crédito, no qual será feito a cobrança\*<br>
  Clique em "Criar Conta" e prossiga.
_\***Cobrança**: Com a conta gratuita você irá receber um bonus da Microsoft Azure +/- no valor de $ 200,00 e caso este saldo seja totalmente consumido pelos seus recursos criados o valor sobressalente será debitado no cartão cadastrado e selecionado._

  06 - Sua conta e cadastro serão criado e você deve ser redirecionado para Painel de gestão dos seus recursos Azure, como demontrado abaixo.
  No caso como esta conta é uma conta gratuita e com propósito de aprendizagem não possuo nenhum recurso criado.
  ![image](https://github.com/philipp-moreira/dio-ms-ai900-ml-desafio-pratico/assets/17642499/9d9ddacd-c202-4881-a8e4-1a35727e2151)

  
## Passo-a-Passo

  01 - Uma vez com acesso ao Azure
  ![image](https://github.com/philipp-moreira/dio-ms-ai900-ml-desafio-pratico/assets/17642499/fa4b7804-9c65-4b72-85a2-2a13fc232502)
  
  
  02 - Você pode escolher algumas preferências dentre elas :<br>
      
      2.1 - O tema (padrão de cores da interface);
        2.1.1 - Clique na [engrenagem] do lado direito superior;
        2.1.2 - Clique na [Appearance + startup views] do lado esquerdo, segunda opção;
        2.1.3 - Selecione o esquema que mais agradar e clique em [Apply/Aplicar];
![image](https://github.com/philipp-moreira/dio-ms-ai900-ml-desafio-pratico/assets/17642499/ecbe6c2a-5ad9-47e8-a17c-aaebd89b0601)

     
      2.1 - A língua (Interface)
        2.1.1 - Clique na [engrenagem] do lado direito superior;
        2.1.2 - Clique na [Language + region] do lado esquerdo, terceira opção;
        2.1.3 - Selecione a língua desejada e a formatação (para informações como data e hora) que mais agradar e clique em [Apply/Aplicar];
    
  03 - De volta ao painel de gestão de recursos
  ![image](https://github.com/philipp-moreira/dio-ms-ai900-ml-desafio-pratico/assets/17642499/23896344-1644-43c7-8f4a-e089d2c2d114)

  04 - Abaixo de **Azure Services**, clique em [Create Resource/Criar Recurso] e será redirecionado para a tela abaixo
  ![image](https://github.com/philipp-moreira/dio-ms-ai900-ml-desafio-pratico/assets/17642499/ec8165f3-ada8-4b8a-817e-ce1dae3b0045)

  
  05 - Digite na caixa de pesquisa {Azure Machine Learning} e aperte [ENTER] no seu teclado
  ![image](https://github.com/philipp-moreira/dio-ms-ai900-ml-desafio-pratico/assets/17642499/848088de-a814-4719-8ccb-a48295010e33)

  
  06 - Selecione a primeira opção/serviço [Azure Machine Learning] e depois clique em [Create]
  ![image](https://github.com/philipp-moreira/dio-ms-ai900-ml-desafio-pratico/assets/17642499/549d5251-5e84-4c80-80c0-54c73077e83f)
 
  
  07 - Na tela exibida preencha os campos **Resource Group**, **Name** e **Region**
  **Resource Group**: Nome do Resource group sob o qual será criado o serviço que estamos configurando
  **Name**: O nome do recurso própriamente dito
  **Region**: Região onde será criado o recurso. Aqui utilizado uma região nos estados unidos visando deixar o custo um pouco mais em conta
  ![image](https://github.com/philipp-moreira/dio-ms-ai900-ml-desafio-pratico/assets/17642499/3c14b175-4538-4ca2-96ec-44f88fe4ff09)

  Caso deseje, dicas de como nomear cada recurso, vide este [doc da própia microsoft](https://learn.microsoft.com/pt-br/azure/cloud-adoption-framework/ready/azure-best-practices/resource-naming-and-tagging-decision-guide)

  08 - Clique em [Review + Create] e depoisem [Create]
  
  09 - Aguarde alguns minutos e receber a notificação em tela de que todos os recursos foram criados, você será redirecionado para tela
  ![image](https://github.com/philipp-moreira/dio-ms-ai900-ml-desafio-pratico/assets/17642499/f45eec65-2193-45ca-b38f-3029146f9caf)

  10 - Clique em [Launch Studio] para abrir o Azure Micrososft Learning
  
  11 - 
  ![image](https://github.com/philipp-moreira/dio-ms-ai900-ml-desafio-pratico/assets/17642499/3e88815a-8cad-4719-a21e-f52109655c3b)

  
## Resultados

### Arquivo(s)
