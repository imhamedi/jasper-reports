# Jasper Reports POC with Java and Spring Boot

## 🗜️ Description

Ce projet est une **Proof of Concept (POC)** visant à démontrer comment générer des rapports avec **JasperReports**, **Java** et **Spring Boot**.  
Il comprend des exemples de création de rapports PDF, Excel, ainsi que la gestion de modèles dynamiques.

---

## 📋 Features

- Génération de rapports PDF, Excel, etc.
- Utilisation de **JasperReports** avec des templates pré-conçus.
- Configuration avec **Spring Boot** pour l'intégration fluide.
- Exemples d'extraction de données depuis une base de données ou un service REST.
- Export des rapports vers différents formats : PDF, Excel, CSV, HTML.

---

## 🛠️ Technologies utilisées

- **Java** (version recommandée : 11 ou plus)
- **Spring Boot** (version 2.5+)
- **JasperReports** (version 6.XX)
- **Jaspersoft Studio** pour la création et l’édition de rapports
- **Maven** ou **Gradle** pour la gestion des dépendances

---

## 📦 Prérequis

Assurez-vous d'avoir les outils suivants installés :

- [Java 11+](https://www.oracle.com/java/technologies/javase-downloads.html)
- [Maven](https://maven.apache.org/download.cgi) ou [Gradle](https://gradle.org/install/)
- [Git](https://git-scm.com/)
- Un IDE compatible (ex. IntelliJ IDEA, Eclipse, Visual Studio Code)
- **Jaspersoft Studio** (voir ci-dessous pour les instructions de téléchargement)

---

## 🖋️ Téléchargement et installation de Jaspersoft Studio

**Jaspersoft Studio** est l'outil graphique officiel pour créer et modifier des fichiers JasperReports (`.jrxml`). Suivez les étapes ci-dessous pour l'obtenir :

1. Accédez à la page de téléchargement officielle :  
  https://community.jaspersoft.com/project/jaspersoft-studio/releases](https://community.jaspersoft.com/download-jaspersoft/download-jaspersoft/

2. Téléchargez la version appropriée pour votre système d'exploitation (Windows, macOS ou Linux).

3. Installez le logiciel en suivant les instructions de l'assistant d'installation.

4. Ouvrez **Jaspersoft Studio**, puis commencez à créer ou modifier vos fichiers `.jrxml`.

5. Exportez le rapport compilé sous forme de fichier `.jasper` si nécessaire. Le fichier compilé peut être utilisé directement par l'application Spring Boot.

---

## 🚀 Démarrage rapide

### 1. Cloner le projet

```bash
git clone https://github.com/imhamedi/jasper-reports.git
cd jasper-reports
```

### 2. Importer le projet dans votre IDE

Vous pouvez importer le projet comme un projet **Maven** ou **Gradle**, selon votre gestionnaire de dépendances préféré.

### 3. Construire le projet

#### Avec Maven :

```bash
mvn clean install
```

#### Avec Gradle :

```bash
gradle build
```

### 4. Lancer l'application

```bash
mvn spring-boot:run
```

Ou avec Gradle :

```bash
gradle bootRun
```

L'application sera accessible à l'adresse : [http://localhost:8080](http://localhost:8080)

---

## 📄 Configuration des rapports Jasper

Les fichiers JasperReports (`.jrxml`) sont stockés dans le dossier `src/main/resources/reports`.  
Vous pouvez les personnaliser ou en ajouter de nouveaux selon vos besoins.

---

## 🗂️ Structure du projet

```
jasper-reports/
├── src/
│   ├── main/
│   │   ├── java/                # Code source Java
│   │   ├── resources/
│   │   │   ├── application.yml  # Configuration Spring Boot
│   │   │   ├── reports/         # Modèles JasperReports (.jrxml)
│   │   │   └── templates/       # Templates statiques HTML ou autres
│   └── test/                    # Tests unitaires et d'intégration
├── pom.xml                      # Dépendances Maven
└── README.md                    # Documentation du projet
```

---

## 🔧 Configuration personnalisée

### 1. Base de données

Si vous utilisez une base de données, modifiez le fichier `application.yml` pour configurer l'URL, le nom d'utilisateur et le mot de passe de la base de données :

```yaml
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/ma_base_de_donnees
    username: root
    password: secret
  jpa:
    hibernate:
      ddl-auto: update
```

### 2. Paramètres des rapports

Vous pouvez définir les paramètres des rapports directement dans le contrôleur ou via un fichier de configuration.

---

## 📚 Documentation et ressources utiles

- [Documentation officielle JasperReports](https://community.jaspersoft.com/documentation)
- [Spring Boot Documentation](https://docs.spring.io/spring-boot/docs/current/reference/html/)
- [Tutoriel JasperReports avec Spring Boot](https://www.baeldung.com/spring-boot-jasper)

---

## 📢 Comment contribuer ?

Nous accueillons les contributions !  
Si vous souhaitez contribuer, veuillez suivre les étapes ci-dessous :

1. Forker le dépôt.
2. Créer une branche pour votre fonctionnalité (`git checkout -b feature/nom-de-la-fonctionnalite`).
3. Committer vos modifications (`git commit -m 'Ajout de fonctionnalité'`).
4. Pousser vos modifications (`git push origin feature/nom-de-la-fonctionnalite`).
5. Ouvrir une **pull request**.

---

## 🔎 Rapport de bugs

Si vous rencontrez un problème, veuillez créer une **issue** dans le dépôt en fournissant les détails du problème, les logs d'erreurs, et les étapes pour reproduire le bug.

---

## 📃 Licence

Ce projet est sous licence **MIT**. Vous êtes libre de l'utiliser, le modifier et le redistribuer. Consultez le fichier [LICENSE](LICENSE) pour plus d'informations.
