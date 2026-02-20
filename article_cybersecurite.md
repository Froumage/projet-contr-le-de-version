

# **Modèle de sécurité Git**





#### Git est l'un des systèmes de contrôle de version les plus populaires, utilisé par les développeurs et les non développeurs pour suivre les modifications, collaborer sur des projets et gérer des bases de code. Si Git est apprécié pour son efficacité en matière de contrôle de version, ses fonctionnalités de sécurité sont tout aussi robustes, garantissant ainsi la protection de votre code et de vos données.

#### 

#### Dans cet article, nous explorerons le modèle de sécurité de Git , en abordant la manière dont il protège vos données, les principales fonctionnalités de sécurité qu'il offre et les meilleures pratiques pour maintenir la sécurité de vos dépôts Git.

#### 

### **Comprendre le modèle de sécurité de Git**



#### Le modèle de sécurité de Git est conçu pour garantir l'intégrité et l'authenticité des données qu'il gère. Ceci est réalisé grâce à une combinaison de techniques cryptographiques, de mécanismes de contrôle d'accès et de bonnes pratiques de gestion des dépôts.

#### 

**------------------------------------------------------------------------------**



##### **1. Intégrité des données**



###### L'une des principales caractéristiques de sécurité de Git est l'intégrité des données. Git garantit que les données stockées dans les dépôts ne peuvent être altérées sans être détectées. Ceci est rendu possible grâce à l'utilisation du hachage cryptographique.





* ###### **Hachage SHA-1** : Git utilise SHA-1 (Secure Hash Algorithm 1) pour générer un hachage unique pour chaque commit, fichier et objet du dépôt. Ce hachage agit comme une empreinte numérique, garantissant qu’une modification, même minime, des données entraîne un hachage totalement différent.



* ###### **Objets immuables** : dans Git, une fois qu’un objet (comme un commit ou un fichier) est créé, il ne peut plus être modifié. Si son contenu change, un nouvel objet avec un nouveau hachage est créé.

**---------------------------------------------**



##### **2. Authentification et autorisation**



###### Git utilise plusieurs méthodes d'authentification pour garantir que seuls les utilisateurs autorisés puissent accéder à un dépôt et le modifier. Les méthodes d'authentification les plus courantes sont les suivantes :





* ###### **Clés SSH** : Les clés SSH (Secure Shell) offrent une méthode sécurisée d’authentification des utilisateurs. Une clé publique est stockée dans le dépôt, et seuls les utilisateurs possédant la clé privée correspondante peuvent y accéder.



* ###### **Jetons d'accès personnels** : des plateformes comme GitHub et GitLab proposent des jetons d'accès personnels, qui servent d'alternative aux mots de passe.



* ###### **OAuth** : Certaines plateformes Git prennent en charge OAuth, permettant aux utilisateurs de s’authentifier via des services tiers comme Google, GitHub ou GitLab. Cela simplifie la gestion des utilisateurs et réduit le besoin de stocker les mots de passe.



**----------------------------------**



###### L'autorisation contrôle ce que les utilisateurs authentifiés peuvent faire au sein du référentiel :



* ###### **Contrôle d'accès basé sur les rôles (RBAC)** : les utilisateurs peuvent se voir attribuer des rôles, tels que propriétaire, responsable de la maintenance ou contributeur, qui déterminent leur niveau d'accès et leurs autorisations au sein du dépôt.



* ###### **Règles de protection des branches** : ces règles permettent de restreindre les personnes autorisées à apporter des modifications aux branches critiques, telles que la branche principale, ajoutant ainsi un niveau de contrôle supplémentaire sur les modifications autorisées.







##### **3. Signatures cryptographiques**



###### Git permet aux utilisateurs de signer les commits et les étiquettes à l'aide de clés GPG (GNU Privacy Guard). Un commit ou une étiquette signé(e) contient une signature cryptographique qui authentifie l'auteur du commit, garantissant ainsi l'authenticité des modifications. Ceci est particulièrement important dans les environnements collaboratifs où il est essentiel de connaître la source des modifications.

###### 

* ###### **Commits signés** : En signant leurs commits, les développeurs peuvent prouver que les modifications proviennent bien d’eux. Cela contribue à prévenir les modifications malveillantes issues de sources inconnues.

###### 

* ###### **Étiquettes signées** : Les étiquettes peuvent également être signées, offrant ainsi une couche de vérification supplémentaire pour les versions ou les points importants de l’historique du dépôt.



**----------------------------------**



##### 

##### **5. Sécurité de l'hébergement du dépôt**

###### De nombreux utilisateurs hébergent leurs dépôts Git sur des plateformes comme GitHub, GitLab ou Bitbucket. Ces plateformes offrent des fonctionnalités de sécurité supplémentaires pour protéger vos dépôts :



* ###### **Authentification à deux facteurs (2FA)** : L'authentification à deux facteurs ajoute une couche de sécurité supplémentaire en exigeant que les utilisateurs fournissent une deuxième forme de vérification, telle qu'un code envoyé sur leur téléphone, en plus de leur mot de passe.

###### 

* ###### **Liste blanche d'adresses IP** : certaines plateformes permettent aux administrateurs de restreindre l'accès aux référentiels en fonction des adresses IP, garantissant ainsi que seuls les utilisateurs de réseaux spécifiques puissent accéder aux données.

###### 

* ###### **Journaux d'audit** : Les plateformes d'hébergement fournissent des journaux d'audit détaillés qui enregistrent toutes les actions effectuées au sein du dépôt, notamment les personnes y ayant accédé et les modifications apportées. Ces journaux sont essentiels pour surveiller les activités suspectes et y réagir.



**----------------------------------------**

#### 

##### **Bonnes pratiques pour sécuriser vos dépôts Git**

###### Bien que le modèle de sécurité de Git fournisse une base solide, il est important de suivre les bonnes pratiques pour maintenir la sécurité de vos dépôts :



* ###### Utilisez des méthodes d'authentification fortes : privilégiez toujours les méthodes d'authentification robustes telles que les clés SSH ou les jetons d'accès personnels. Évitez d'utiliser des mots de passe, en particulier les mots de passe partagés, car ils sont vulnérables au phishing et à d'autres attaques.

###### 

* ###### Activez l'authentification à deux facteurs (2FA) : lorsque cela est possible, activez la 2FA sur vos plateformes d'hébergement Git. Cela ajoute une couche de protection supplémentaire et réduit considérablement le risque d'accès non autorisé.

###### 

* ###### Vérifiez régulièrement les autorisations d'accès : examinez périodiquement les autorisations des utilisateurs qui ont accès à vos référentiels.

###### 

* ###### Protéger les branches critiques : configurez des règles de protection des branches pour empêcher toute modification non autorisée des branches critiques telles que main ou master. Exigez des revues de code et assurez-vous que les modifications sont signées et vérifiées avant fusion.

###### 

* ###### Signez vos commits et vos tags : privilégiez l’utilisation des signatures GPG pour vos commits et vos tags. Cela garantit cryptographiquement l’identité de l’auteur et assure l’intégrité des modifications.

###### 

* ###### Surveillez et traitez les alertes de sécurité : les plateformes d’hébergement Git émettent régulièrement des alertes de sécurité signalant les vulnérabilités de vos dépôts, telles que des secrets exposés ou des dépendances obsolètes. Surveillez ces alertes et intervenez rapidement pour corriger tout problème.

###### 

* ###### Chiffrez les données sensibles : évitez de stocker des informations sensibles, telles que les clés API ou les mots de passe, directement dans vos référentiels. Utilisez des variables d’environnement ou des outils de gestion des secrets pour gérer les données sensibles en toute sécurité.

###### 

* ###### Utilisez des protocoles de communication sécurisés : privilégiez toujours des protocoles de communication sécurisés tels que SSH ou HTTPS pour accéder à vos dépôts Git. Cela garantit le chiffrement et la sécurité des données transmises entre votre environnement local et le serveur.



























