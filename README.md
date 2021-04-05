## Criar um diretório e clonar os 3 repositórios no mesmo nível 

  

$ ```mkdir project && cd project```

docker images 

  

1 - $ ```git clone git@github.com:mayckol/basis-docker.git```

  

  

### docker api 

  

2 - $ ```git clone git@github.com:mayckol/basis-api.git```

  

  

### docker front 

  

3 - $ ```git clone git@github.com:mayckol/basis-front.git```

  

### Instalar dependências 

  

## - Vue 

  

$ ```cd basis-front```

$ ```yarn```

ou 

$ ```pm install```

  

  

## - Laravel 

  

$ ```cd ../basis-docker```

$ ```docker-compose run --rm artisan composer install```

$ ```docker-compose run --rm artisan migrate --seed```

$ ```docker-compose run --rm artisan passport:install --force```

  

$ ```cd ../basis-api``` 

Clonar o arquivo .env.example como .env 

  

$ ```docker-compose run --rm artisan key:generate```

  

Subistituir as keys 

PASSPORT_CLIENT_ID= 

PASSPORT_CLIENT_SECRET= 

Pelos valores gerados no comando de instalação do passport 

  

Encryption keys generated successfully. 

Personal access client created successfully. 

Client ID: 1 

Client secret: FWQPbQwufSFfxdQJ2Y5Ue3lWOC4cDu6a7egHmieG 

Password grant client created successfully. 

Client ID: 2 

Client secret: EKQRtOuys99ieNO9J1Elq0mHQwwuuhqAvsLhlJ6y 


$ ```cd ../basis-docker```
$ ```docker-compose up -d```

Url da aplicação 

http://localhost:8081/ 

$ ```$ docker-compose run --rm artisan```< acessa o artisan dentro do container 
$ ```$ docker-compose run --rm composer```< acessa o composer dentro do container 