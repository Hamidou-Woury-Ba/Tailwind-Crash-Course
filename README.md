npm init -y : pour installer le fichier json
npm i -D tailwindcss : Installer Tailwind en tant que dépendances de développement
npx tailwindcss init : créer un config file
    Un fichier tailwind.config.js est créé et dans ce fichier au niveau de  :
        content: ['./*.html'], : pour dire que le tailwind s'applique à tout les fichiers html se trouvant à la racine
On créé un fichier input.css pour ajoutez les directives @tailwind pour chacune des couches de Tailwind à votre fichier CSS principal.

Démarrer le processus de génération de l’interface de ligne de commande Tailwind
Dans le fichier package.json puis dans script on change : 
    "test": "echo \"Error: no test specified\" && exit 1" par :
    "build": "tailwindcss -i ./input.css -o ./css/main.css" => Cette commande prend un fichier d'entrée ./input.css, qui contient probablement les directives Tailwind CSS, et compile le CSS généré dans un fichier de sortie ./css/main.css.
    Puis on ajoute cette ligne :
    "watch": "tailwindcss -i ./input.css -o ./css/main.css --watch" => L'option --watch indique à Tailwind CSS de surveiller les modifications dans le fichier d'entrée ./input.css et de recompiler automatiquement le fichier de sortie ./css/main.css chaque fois que des modifications sont détectées.
    npm run build : Cette commande est utile pour générer un fichier CSS prêt à être utilisé dans votre projet, en particulier avant de déployer votre site ou application.