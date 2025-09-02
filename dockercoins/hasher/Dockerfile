FROM ruby:3.2.4-slim

WORKDIR /app

# Dependencias del sistema
RUN apt-get update && apt-get install -y build-essential curl git && rm -rf /var/lib/apt/lists/*

# Instalar gems necesarias
RUN gem install sinatra thin rack puma webrick rackup

# Copiar código
COPY hasher.rb .

# Exponer puerto
EXPOSE 80

# Arrancar Sinatra
CMD ["ruby", "hasher.rb"]
