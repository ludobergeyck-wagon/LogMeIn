# Utiliser une image Python légère
FROM python:3.11-slim

# Définir le dossier de travail dans le conteneur
WORKDIR /app

# Installer les dépendances système requises pour PostgreSQL
RUN apt-get update && apt-get install -y \
    gcc \
    libpq-dev \
    && rm -rf /var/lib/apt/lists/*

# Copier les dépendances et les installer (optimisation du cache)
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copier tout le reste du code (y compris app.py et les tests)
COPY . .

# Exposer le port 5000
EXPOSE 5000

# Commande de démarrage
CMD ["python", "app.py"]
