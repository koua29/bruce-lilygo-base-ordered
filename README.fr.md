# Lilygo_base_ordered — thème Bruce (version corrigée)

<p align="center">🇺🇸 <a href="README.md">English</a> · 🇫🇷 <b>Français</b></p>

![Aperçu avant/après](docs/preview.png)

Version **corrigée** du thème **`Lilygo_base`** d'[**anonimoKali**](https://github.com/anonimoKali)
pour le firmware [**Bruce**](https://github.com/BruceDevices/firmware)
(LilyGO T-Embed CC1101 et autres appareils compatibles).

> ⚠️ Ce dépôt est un **travail dérivé**. Tout le design, les icônes et le style
> originaux sont l'œuvre d'**anonimoKali**. Voir « Crédits » ci-dessous.

## Le problème corrigé

Dans le thème d'origine, chaque icône est en réalité une **capture de carrousel** :
le menu **précédent** est dessiné en haut de l'image et le menu **suivant** en bas,
autour du gros logo central.

Ces aperçus haut/bas étaient figés sur un **ordre de menu différent** de celui du
firmware Bruce actuel. Résultat à l'écran : les voisins annoncés ne correspondaient
pas au menu réellement atteint en tournant la molette — par exemple **RFID**
affichait *RF / IR* au lieu de *GPS / FILES*. Ce n'est **ni un bug de la molette,
ni du firmware** : la navigation est correcte, seules les images induisaient en erreur.

## La correction

Les **bandes haut et bas** de chaque icône ont été remappées pour refléter l'ordre
réel du menu (**haut = précédent, bas = suivant**) :

```
Config → Wifi → BLE → RF → NRF24 → LORA → FM → IR → ETH → GPS → RFID → FILES → JS → CLOCK → OTHERS → (Config)
```

- Le **logo central** de chaque icône est **inchangé**.
- Seules les mini-étiquettes voisines ont été corrigées, en réutilisant les
  éléments graphiques déjà présents dans le thème (raccords invisibles).
- Corrigé pour les **4 résolutions** : `105px`, `140px`, `180px`, `192px`.

## Installation

| Dossier | Appareil |
|---|---|
| `105px` | M5StickC Plus / Plus 2 |
| `140px` | **LilyGO T-Embed CC1101 / CC1101 Plus** |
| `180px` | Cheap Yellow Display (CYD) / T-Deck |
| `192px` | LilyGO T-LoRa-Pager |

1. Copier le dossier correspondant à ton écran dans `/themes/` de la carte SD
   (créer le dossier `/themes` s'il n'existe pas).
2. Sur l'appareil : **Settings → Themes → `Theme_Lilygo_base_ordered.json`**.

## Crédits

- **Thème original** : [anonimoKali](https://github.com/anonimoKali) —
  dépôt source : [`Bruce-Themes`](https://github.com/anonimoKali/Bruce-Themes),
  thème [`Lilygo_base_By_anonimoKali`](https://github.com/anonimoKali/Bruce-Themes/tree/main/themes/Lilygo_base_By_anonimoKali).
- **Correction de l'ordre des menus** : [koua29](https://github.com/koua29).

## Licence

**GNU GPLv3** — identique à la licence du thème d'origine. Voir [LICENSE](LICENSE).

## 🛒 Matériel

*Liens partenaires Amazon : si vous achetez via ces liens, le projet touche une petite commission, sans surcoût pour vous.*

<table>
<tr>
<td align="center" width="33%">
  <a href="https://www.amazon.fr/dp/B0D45MSMJR?linkCode=ll2&amp;tag=koua29blilygobaseord-21&amp;ref_=as_li_ss_tl"><img src="docs/amazon-B0D45MSMJR.jpg" width="200" alt="Batterie Anker 545 (10 000 mAh)"></a><br>
  <b><a href="https://www.amazon.fr/dp/B0D45MSMJR?linkCode=ll2&amp;tag=koua29blilygobaseord-21&amp;ref_=as_li_ss_tl">Batterie Anker 545 (10 000 mAh)</a></b><br><sub>Pour faire tourner le T-Embed loin d'une prise</sub>
</td>
<td align="center" width="33%">
  <a href="https://www.amazon.fr/dp/B0C1FCZM94?linkCode=ll2&amp;tag=koua29blilygobaseord-21&amp;ref_=as_li_ss_tl"><img src="docs/amazon-B0C1FCZM94.jpg" width="200" alt="Antenne SMA 433 MHz (lot de 2)"></a><br>
  <b><a href="https://www.amazon.fr/dp/B0C1FCZM94?linkCode=ll2&amp;tag=koua29blilygobaseord-21&amp;ref_=as_li_ss_tl">Antenne SMA 433 MHz (lot de 2)</a></b><br><sub>Antenne sub-GHz pour la radio CC1101</sub>
</td>
<td align="center" width="33%">
  <a href="https://www.amazon.fr/dp/B0B7NVMBPL?linkCode=ll2&amp;tag=koua29blilygobaseord-21&amp;ref_=as_li_ss_tl"><img src="docs/amazon-B0B7NVMBPL.jpg" width="200" alt="microSD SanDisk 64 Go (lot de 2)"></a><br>
  <b><a href="https://www.amazon.fr/dp/B0B7NVMBPL?linkCode=ll2&amp;tag=koua29blilygobaseord-21&amp;ref_=as_li_ss_tl">microSD SanDisk 64 Go (lot de 2)</a></b><br><sub>Pour les thèmes, scripts et captures Bruce</sub>
</td>
</tr>
</table>

<sub>En tant que Partenaire Amazon, je réalise un bénéfice sur les achats remplissant les conditions requises.</sub>
