---
title: Comment jouer à Project+ ?
date: 2025-03-17
author: Axel CALIXTE
tags:
  - pplus
---

## Pré-requis

1. Avoir un iso de Brawl NTSC via `!iso` sur notre Discord
2. Avoir téléchargé [le dernier build de P+](https://projectplusgame.com/download)
   - Dolphin Windows/Linux pour jouer en Netplay sur l'émulateur Dolphin
   - Offline / Wii ou Wii Lite en fonction de la capacité que vous utilisez avec votre Wii
3. Disposer d'un adaptateur manette GameCube
   - [Celui d'Arte](https://www.input-integrity.com/fr/product-page/adaptateur-sans-perte) <- un gars cool de la commu'
   - Officiels de Nintendo Smash 4 ou Ultimate

## Installations

1. Extraire l'archive de Project+
2. Insérer l'iso de Brawl dans le dossier `games` à l'intérieur de l'archive
3. Démarrer Dolphin.exe
4. Choisir Super Smash Bros. Brawl comme iso par défaut avec un clic droit depuis la liste des jeux

   Désormais, en démarrant Offline ou Online via les `*Launcher.dol`, Project+ est censé démarrer !

### Installer les drivers de l'adaptateur GCC

1. Adaptateur input-integrity
   Les drivers n'ont pas besoin d'être installés.
2. Adaptateurs Officiel Nintendo ([référence](https://fr.dolphin-emu.org/docs/guides/how-use-official-gc-controller-adapter-wii-u/?cr=fr#Using_Zadig))
   1. Installer [zadig.exe](https://github.com/pbatard/libwdi/releases/latest) puis le démarrer
   2. Options -> List All Devices
   3. Sélectionner `WUP-028` et vérifier que l'id USB est `057E 0337`.
   4. Sur la colonne de droite, sélectionner `WinUSB` puis cliquer sur `Replace Driver` et installer le driver au système en cliquant sur `Yes`.
3. Une fois les drivers installés, votre configuration de manettes doit ressembler à ça:
   `img`

## Jouer en Netplay

### Configuration préalable

Dans le menu `Config` puis `Path`:

1. Ajouter le dossier Launcher qui contient les fichiers `*Launcher.dol` de P+
2. Définir l'iso par défaut comme étant votre iso de Brawl téléchargé - Clic droit sur Super Smash Bros. Brawl > Set as default ISO
   > Votre hash doit correspondre à `d18726e6dfdc8bdbdad540b561051087`. Vous pouvez le calculer depuis Dolphin avec un clic-droit sur Super Smash Bros. Brawl > Properties > Info > MD5 Checksum -> Compute.
3. Définir le chemin vers la carte SD

Dans le menu `Controllers`, confirmez que votre Manette GameCube branchée sur le premier port de votre adaptateur est correctement configurée.
En cliquant sur `Configure`, vous devriez voir inscrit _Adapter detected_ avec une fréquence renseignée en Hz.

Dans le menu `Graphics`, on vous conseille de cocher l'option _Use fullscreen_ qui permet d'améliorer légèrement les performances de Dolphin.
Nous n'aborderons pas les paramètres graphiques qui peuvent se révéler complèxes et dépendent de votre ordinateur. Toutefois, nous vous recommandons fortement de ne pas activer le V-Sync.

A l'issue de cette configuration vous devriez pouvoir démarrer Super Smash Bros. Brawl depuis l'interface principale en cliquant sur l'image de Brawl et démarrer Project+ pour la première fois en cliquant sur _Project+ Offline Launcher.dol_ !

### Rejoindre une partie

Les options non mentionnées ne sont pas à modifier pour jouer simplement et sont réservées à un usage plus avancé du netplay de Dolphin.
En cliquant sur `Netplay`, vous accédez à la fenêtre de configuration du Netplay Dolphin qui vous permet de jouer en ligne sur les serveurs de Dolphin _Traversal Server_ ou en hébergeant vous-même des parties sur votre réseau en _Direct Connection_.

1. **Rester en Traversal Server**
1. Renseigner votre `Nickname` ou pseudo
1. Insérer le code de connection de votre adversaire pour le rejoindre. Il s'occupera de configurer le Netplay entre vous et de lancer le jeu !

### Héberger une partie

1. Cliquer sur l'onglet `Host`
2. Sélectionner _Project+ Offline Launcher.dol_ puis cliquer sur `Host` (un double-clic fonctionne également)
3. Transmettre le code de votre `Room` à votre adversaire.
   > Vous verrez apparaître son pseudo, son ping, son `frametime`, son buffer et _Status: ready_ dès qu'il vous rejoindra.

Seul le paramètre du _Minimum Buffer_ est à configurer dans la barre inférieure.
Le buffer doit toujous être >= 4. Un buffer de 4 permet théoriquement d'émuler le jeu sur Wii le plus fidèlement.
La règle est d'ajouter 1ms de buffer pour chaque 8 ms de ping entre vous et votre adversaire. Si vous voyez votre adversaire à 40ms de ping, il faudra donc passer à 5ms de _Minimal Buffer_. Dans les faits, il est habituel de rajouter un peu plus de buffer si la connexion entre vous et votre adversaire est instable. Pensez à jouer en Ethernet si vous le pouvez.

C'est le moment de démarrer le jeu en cliquant sur **Start!**

### Le tchat

A tout moment, même avec le jeu en plein-écran, vous pouvez appuyer sur la touche `t` de votre clavier puis écrire un message à envoyer avec `Entrer`.