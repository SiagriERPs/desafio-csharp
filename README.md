# Desafio C# - Siagri ERPs

Quer fazer parte da transformação do campo ~~escrevendo~~ codando o futuro do agronegócio?

Se deseja participar do nosso processo seletivo, siga as instruções deste desafio e execute os seguintes passos: 

* Nos mande sua resolução em um *pull request* neste repositório.

* Deixe a aplicação disponível publicamente em imagem docker em qualquer host. Na descrição do PR passe o link para que consigamos usar sua imagem.

* Por último, caso você ainda não esteja no processo seletivo, envie um email para [murilo.silva@siagri.com.br](mailto:murilo.silva@siagri.com.br) com seu CV anexado e o link da aplicação (se já estiver no processo seletivo, não precisa);

  

# Sobre a Siagri

O [Grupo Siagri](https://www.siagri.com.br/) está entre as maiores empresas de software para agronegócio do país. Nascemos no agro e somos especialistas em levar tecnologia para gestão de empresas e propriedades rurais.

Estamos com nossos clientes, pra fazer o campo acontecer. Temos orgulho de ajudar a construir o presente e o futuro do agronegócio.


# O desafio

Crie um microsserviço capaz de aceitar solicitações RESTful que recebam como parâmetro o nome da cidade ou as coordenadas (*latitude e longitude*), faça persistência da temperatura da cidade naquele dia em um banco de dados MSSQL e retorne a temperatura atual e se houver, o histórico de temperaturas do último mês.


## Requisitos

1. Ter um endpoint que receba o nome da cidade, faça persistência do resultado e retorne a temperatura atual;
2. Ter um endpoint que receba a latitude e longitude, faça persistência do resultado e retorne a temperatura atual;
3. Tem um endpiont que receba o nome da cidade ou a latitude e longitude, e retorne o histórico de temperaturas para a localidade no último mês;

## Requisitos não funcionais

- Como este serviço será um sucesso mundial, ele deve estar preparado para ser tolerante a falhas, responsivo e resiliente.

- Use qualquer ferramenta e estrutura com as quais se sinta confortável e elabore brevemente sua solução, detalhes de arquitetura, escolha de padrões e estruturas.

- Será considerado ponto extra: 
  - se sua aplicação tiver sua imagem publicada no [Docker Hub](https://hub.docker.com);
  - se sua aplicação tiver mais de 60% de cobertura de testes unitários usando xUnit;
  - se você colocar no seu projeto uma pasta com as colections do Postmann prontas para serem executadas;
  - se sua aplicação tiver documentada no swagger no seguinte endpoint: /api/documentation;
  - se seu projeto vir com um docker compose com sua aplicação e sql server configurados e funcionando;
  
Obs.: Não se preocupe com os pontos extras, faça-os se você se sentir confortável e se tiver tempo, consideraremos seu código **desclassificado se seu projeto não estiver funcionando** ou se não tiver os requisitos básicos implementados e funcionais.

## Dicas

- Você pode usar a API do *[OpenWeatherMaps](https://openweathermap.org)* para buscar dados de temperatura;
- Não é necessário ter um banco de dados hospedado, você pode usar SQL Server InMemory ou rodar o sql server em um container (neste caso, deixe documentado no readme.md como executar os dois containers);
- Se tiver dificuldades em usar o SQL Server InMemory, pode persistir de qualquer outra forma que se sentir confortável;
- Certifique-se que sua imagem está funcionando perfeitamente com um simples: `docker run -d --name desafio-csharp -port 5000:5000 [seu_docker_hub]/desafio-csharp`, isso te dará pontos extras;

## Recomendações

* Utilize C#;
* Utilize .NET Core 3.1;
* Utilize docker;
* Utilize boas práticas de codificação, isso será avaliado;
* Código limpo, organizado e documentado (quando necessário);
* Use e abuse de:
  * SOLID;
  * Criatividade;
  * Performance;
  * Manutenabilidade;
  * Testes Unitários
  * ... pois avaliaremos tudo isso!
