## Buildando Django através do Docker
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Django](https://img.shields.io/badge/django-%23092E20.svg?style=for-the-badge&logo=django&logoColor=white)
![Badge](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Badge](https://img.shields.io/badge/CSS-239120?&style=for-the-badge&logo=css3&logoColor=white)
![Badge](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)


Projeto criado para testar a implementação do Docker junto ao Django e PostgreSQL 

### Ferramentas utilizadas

- Django
- Docker
- Python
- PostgreSQL
- JavaScript
- css
- html5

### Para rodar o projeto:

- crie uma pasta para clonar o repositório e execute o comando: git clone 
- caminhe até a pasta onde encontra-se o arquivo docker-compose
- obs: altere as configurações de acesso ao banco de dados no arquvio docker-compose.yaml
- execute o comando: dokcer-compose up -d 
- Acesse seu servidor local: https://localhost:8000

      version: "3.6"

      services:
        web:
          build: .
          command: python manage.py runserver 0.0.0.0:8000
          volumes:
            - .:/code
          ports:
            - 8000:8000
          depends_on:
            - db
        db:
          image: postgres:13
          environment:
            - POSTGRES_USER=postgres
            - POSTGRES_PASSWORD=postgres
          volumes:
            - postgres_data:/var/lib/postgresql/data/

      volumes:
        postgres_data:
      
      
![Captura de tela de 2022-05-20 20-06-49_Easy-Resize com](https://user-images.githubusercontent.com/87938869/169623343-b9b90038-176d-4bc7-8ee3-9d5f0f7b264e.jpg)
