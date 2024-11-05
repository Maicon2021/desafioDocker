# Usa uma imagem base com Python
FROM python:3.10.0

# Definir o diretório de trabalho dentro do conteiner
WORKDIR /app

#Copia o arquivo de dependencias
COPY requirements.txt .

#Executa instalação das dependencias 
RUN pip install -r requirements.txt

#Copia todo para o projeto /app
COPY . /app/

#Configura porta onde sera exposta a aplicação 
EXPOSE 5000

#Comandos de geração
CMD [ "gunicorn", "--bind", "0.0.0.0:5000", "app:app" ]
