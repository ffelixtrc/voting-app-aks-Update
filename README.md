# voting-app-aks-Update #

Criei este repositório como parte do repositório https://github.com/ffelixtrc/voting-app-aks.
No primeiro repositório ficou a implantação da infraestrutura e neste aqui a parte de atualização da aplicação.
Para simular esta atualização, alterei o arquivo de configuração da aplicação que antes mostrava na interface animais e troquei para cores.
Após isso, "buildei" dois novos conteiners (um com o frontend e o outro com o backend) e hospedei no docker hub de forma publica.
Neste repositório de atualização, usando os dados em base 64 do kubectl que foi gerado do deploy da infra via terraform, usei essa informação do arquivo para conseguir atualizar o cluster com os novos conteiners, reimplantando o script deployment.yaml, subtituindo a imagem da Microsoft que estava rodando do primeiro deploy pela imagem personalizada hospedada no docker hub.
