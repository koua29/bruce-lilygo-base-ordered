# Lilygo_base_ordered — Bruce theme (fixed version)

<p align="center">🇺🇸 <b>English</b> · 🇫🇷 <a href="README.fr.md">Français</a></p>

A **fixed** version of the **`Lilygo_base`** theme by [**anonimoKali**](https://github.com/anonimoKali)
for the [**Bruce**](https://github.com/BruceDevices/firmware) firmware
(LilyGO T-Embed CC1101 and other compatible devices).

> ⚠️ This repository is a **derivative work**. All the original design, icons and style
> are the work of **anonimoKali**. See "Credits" below.

## The problem that was fixed

In the original theme, each icon is actually a **carousel snapshot**:
the **previous** menu is drawn at the top of the image and the **next** menu at the bottom,
around the big central logo.

Those top/bottom previews were frozen on a **menu order different** from the one in the
current Bruce firmware. Result on screen: the announced neighbours didn't match
the menu you actually reached by turning the wheel — for example **RFID**
showed *RF / IR* instead of *GPS / FILES*. It's **neither a wheel bug
nor a firmware bug**: navigation is correct, only the images were misleading.

## The fix

The **top and bottom strips** of each icon were remapped to reflect the real
menu order (**top = previous, bottom = next**):

```
Config → Wifi → BLE → RF → NRF24 → LORA → FM → IR → ETH → GPS → RFID → FILES → JS → CLOCK → OTHERS → (Config)
```

- The **central logo** of each icon is **unchanged**.
- Only the small neighbour labels were fixed, reusing the
  graphic elements already present in the theme (invisible seams).
- Fixed for **all 4 resolutions**: `105px`, `140px`, `180px`, `192px`.

## Installation

| Folder | Device |
|---|---|
| `105px` | M5StickC Plus / Plus 2 |
| `140px` | **LilyGO T-Embed CC1101 / CC1101 Plus** |
| `180px` | Cheap Yellow Display (CYD) / T-Deck |
| `192px` | LilyGO T-LoRa-Pager |

1. Copy the folder matching your screen into `/themes/` on the SD card
   (create the `/themes` folder if it doesn't exist).
2. On the device: **Settings → Themes → `Theme_Lilygo_base_ordered.json`**.

## Credits

- **Original theme**: [anonimoKali](https://github.com/anonimoKali) —
  source repository: [`Bruce-Themes`](https://github.com/anonimoKali/Bruce-Themes),
  theme [`Lilygo_base_By_anonimoKali`](https://github.com/anonimoKali/Bruce-Themes/tree/main/themes/Lilygo_base_By_anonimoKali).
- **Menu-order fix**: [koua29](https://github.com/koua29).

## License

**GNU GPLv3** — same as the original theme's license. See [LICENSE](LICENSE).

## 🛒 Hardware

*Amazon affiliate links: if you buy through these links, the project earns a small commission at no extra cost to you.*

<table>
<tr>
<td align="center" width="33%">
  <a href="https://www.amazon.com/dp/B0D45MSMJR?linkCode=ll2&amp;tag=koua29blilygobaseord-20&amp;ref_=as_li_ss_tl"><img src="docs/amazon-B0D45MSMJR.jpg" width="200" alt="Anker 545 power bank (10,000 mAh)"></a><br>
  <b><a href="https://www.amazon.com/dp/B0D45MSMJR?linkCode=ll2&amp;tag=koua29blilygobaseord-20&amp;ref_=as_li_ss_tl">Anker 545 power bank (10,000 mAh)</a></b><br><sub>Keeps the T-Embed running away from an outlet</sub>
</td>
<td align="center" width="33%">
  <a href="https://www.amazon.com/dp/B0C1FCZM94?linkCode=ll2&amp;tag=koua29blilygobaseord-20&amp;ref_=as_li_ss_tl"><img src="docs/amazon-B0C1FCZM94.jpg" width="200" alt="433 MHz SMA antenna (2-pack)"></a><br>
  <b><a href="https://www.amazon.com/dp/B0C1FCZM94?linkCode=ll2&amp;tag=koua29blilygobaseord-20&amp;ref_=as_li_ss_tl">433 MHz SMA antenna (2-pack)</a></b><br><sub>Sub-GHz antenna for the CC1101 radio</sub>
</td>
<td align="center" width="33%">
  <a href="https://www.amazon.com/dp/B0B7NVMBPL?linkCode=ll2&amp;tag=koua29blilygobaseord-20&amp;ref_=as_li_ss_tl"><img src="docs/amazon-B0B7NVMBPL.jpg" width="200" alt="SanDisk 64 GB microSD (2-pack)"></a><br>
  <b><a href="https://www.amazon.com/dp/B0B7NVMBPL?linkCode=ll2&amp;tag=koua29blilygobaseord-20&amp;ref_=as_li_ss_tl">SanDisk 64 GB microSD (2-pack)</a></b><br><sub>For Bruce themes, scripts and captures</sub>
</td>
</tr>
</table>

<sub>As an Amazon Associate I earn from qualifying purchases.</sub>
