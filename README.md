# TOS_Nuxt_Color_Mode

Bonjour et bienvenue dans ce TOS sur Nuxt Color Mode. Cette fonctionnalité vous permet de basculer facilement entre les thèmes sombre et clair ou même des modes daltoniens pour votre application Nuxt.js.

Voici les étapes de base pour mettre en place Nuxt Color Mode :

## Étape 1 : Installation du module
Assurez-vous que votre projet Nuxt.js est créé et fonctionne correctement. Ensuite, installez le module @nuxt/color-mode :

```
npm install --save-dev @nuxt/color-mode
```

## Étape 2 : Configuration dans nuxt.config.js
Ajoutez le module dans la section buildModules de votre fichier nuxt.config.js :

```
// nuxt.config.js
export default {
  buildModules: ['@nuxt/color-mode'],
}
```

## Étape 3 : Utilisation dans votre application
Le module ajoute une classe CSS automatiquement basée sur le thème actuel. Vous pouvez utiliser cette classe pour définir des styles spécifiques pour le thème clair et sombre.

Exemple de fichier de style (CSS ou SCSS) :

```
/* styles/app.css */
body.dark-mode {
  background-color: #2c3e50; /* couleur de fond pour le thème sombre */
  color: #ecf0f1; /* couleur du texte pour le thème sombre */
}

body.light-mode {
  background-color: #ecf0f1; /* couleur de fond pour le thème clair */
  color: #2c3e50; /* couleur du texte pour le thème clair */
}
```

## Étape 4 : Basculement entre les thèmes
Vous pouvez maintenant basculer entre les thèmes en utilisant les méthodes fournies par le module. Par exemple, pour basculer vers le thème sombre, vous pouvez utiliser :

```
this.$colorMode.preference = 'dark'
```

Et pour basculer vers le thème clair :

```
this.$colorMode.preference = 'light'
```

Vous pouvez également définir le thème initial dans votre fichier nuxt.config.js :

```
// nuxt.config.js
export default {
  colorMode: {
    preference: 'light', // ou 'dark'
  },
}
```

## Conclusion

Ainsi, votre application devrait maintenant être capable de basculer entre les thèmes clair et sombre en fonction des préférences de l'utilisateur ou de vos paramètres par défaut. Vous pouvez personnaliser davantage cette configuration en fonction de vos besoins spécifiques. J'espère que ce TOS aura pu vous être utile.

Pour aller plus loin, vous pouvez vous référer à la documentation officielle : https://color-mode.nuxtjs.org/
