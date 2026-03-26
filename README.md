# 💠 Mana MU-Plugin

Plugin de configuration et de White Label pour WordPress.  
Permet de centraliser le branding et la personnalisation de l’interface admin, indépendamment du thème.

---

## 🚀 Installation

1. Se placer dans `wp-content/mu-plugins/`.
2. Cloner le dépôt :

   ```bash
   git clone https://github.com/Maanaaa/mana-wp-mu-plugin .
   ```

3. S'assurer que `mana-mu-plugin.php` est à la racine du dossier `mu-plugins`.

---

## 📁 Structure du projet

- `mana-mu-plugin.php` : Loader principal.  
- `core/assets/icon.svg` : Logo unique (Login, Sidebar, Top Bar).  
- `core/admin-settings.php` : Interface **Configuration** dans l’admin WordPress.  
- `core/config.php` : Logique de verrouillage (Base de données vs constantes).  
- `core/white-label.php` : Injection CSS, nettoyage du header et masquage des menus.

---

## ⚙️ Configuration & Verrouillage

Les menus peuvent être masqués via l’interface **Configuration** du White Label.  
Pour un verrouillage définitif, utiliser les constantes suivantes dans `wp-config.php` :

```php
// Verrouillage des menus (écrase les réglages de l'interface)
define('HIDE_ARTICLES', true);
define('HIDE_PAGES', true);
define('HIDE_PLUGINS', true);
define('HIDE_SETTINGS', true);
define('HIDE_THEMES', true);
define('HIDE_ACF', true);
```

---

## 🛠 Fonctionnalités

- **White Label** : Branding complet (page de login, sidebar et barre d’outils) via `icon.svg`.  
- **Masquage d’ACF** : Dans le White Label, possibilité de cacher l’onglet ACF dans le menu admin.  
- **Sécurité & Nettoyage** : Suppression des emojis, notifications de mise à jour, métas generator et commentaires.  
- **Portabilité** : Les assets sont embarqués dans le plugin pour rester indépendant du thème.  

---

Développépar [**Théo Manya**](https://theo-manya.fr)