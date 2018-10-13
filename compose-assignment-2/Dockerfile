# - Use official Drupal 8.2 from Dockecr Hub
FROM drupal:8.2

# - Install git using: apt-get update && apt-get install -y git
RUN apt-get update && apt-get install -y git \
    && rm -rf /var/lib/apt/lists/*

# - Cahnge working directory to /var/www/html/themes
WORKDIR /var/www/html/themes

# - Clone bootstrap template to Drupal and chane ownership to www-data user
RUN git clone --branch 8.x-3.x --single-branch --depth 1 https://git.drupal.org/project/bootstrap.git \
    && chown -R www-data:www-data bootstrap

# - Change working directory back to default path
WORKDIR /var/www/html
