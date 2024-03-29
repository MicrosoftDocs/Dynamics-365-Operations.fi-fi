---
title: TDS-laskutoimitusten kaavojen suunnittelutoiminto
description: Tässä artikkelissa on esimerkki siitä, miten Vero vähennettynä lähteissä (TDS) lasketaan tapahtumaan liitetyn TDS-ryhmän TDS-verokoodin kaavan perusteella.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1196f7258c898a55f3f29ddce7457e6f527185d8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889858"
---
# <a name="formula-designer-for-tds-calculations"></a>TDS-laskutoimitusten kaavojen suunnittelutoiminto

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on esimerkki siitä, miten Vero vähennettynä lähteissä (TDS) lasketaan kullekin TDS-verokoodille määritetyn kaavan perusteella. TDS-verokoodit määritetään tapahtumaan liittyvässä TDS-ryhmässä. Ennen TDS-kaavojen suunnittelua TDS-järjestelmän perusmääritykset on suoritettava seuraavien ohjeiden mukaisesti. 

- Määritä TDS-komponenttiryhmät **Ennakonpidätyksen komponenttiryhmät** -sivulla. 
- Määritä TDS-komponentit ja liitä TDS-komponenttiryhmä TDS-komponentteihin **Ennakonpidätyksen komponentit** -sivua käyttäen. 
- Määritä TDS-verokoodit ja liitä TDS-komponentit verokoodeihin **Ennakonpidätyskoodit**-sivua käyttäen. 
- Määritä TDS-veroryhmät **Ennakonpidätysryhmät**-sivulla. Liitä sitten TDS-verokoodit veroryhmään ja määritä kaava **Kaavan suunnittelutoiminto** -sivulla. 

**Esimerkkikaava**

Tässä esimerkissä TDS-ryhmä Vuokra liitetään toimittajalle A luotuun ostolaskuun. Laskun summa on 100 000 dollaria. Seuraavassa taulukossa on tietoja laskun TDS-laskelmasta.

| TDS-ryhmä                                                   | TDS-ryhmään liitetyt TDS-verokoodit | Arvo              | Veron peruste (kaavan suunnittelutoiminto) | Laskelmalauseke (kaavan suunnittelutoiminto) | Veron peruste | Laskettu TDS-summa |
| ------------------------------------------------------------ | --------------------------------------- | ------------------ | --------------------------------- | :----------------------------------------: | ----------- | --------------------- |
| Vuokra                                                         | TDS  (TDS-komponentti-TDS)                | 10 %                | Bruttosumma                      |                                            | 100,000      | 10,000                 |
| Lisämaksu (TDS-komponentti-lisämaksu)                         | 10 %                                     | Ilman bruttosummaa | +TDS                              |                   10000                    | 1 000        |                       |
| PE-Cess  (TDS-komponentti- PE-Cess)                            | 2 %                                      | Ilman bruttosummaa | +TDS+Lisämaksu                    |                   11000                    | 220         |                       |
| SHE Cess  (TDS-komponentti- SHE Cess)                          | 1 %                                      | Ilman bruttosummaa | +TDS+Lisämaksu                    |                   11000                    | 110         |                       |
| **TDS**-**kokonaissumma**, **joka** **on** **laskettu** **laskulle** | **11,330**                               |                    |                                   |                                            |             |                       |

Tositemerkinnät luodaan seuraavasti:

| Tili           | Veloitus  | Luotto |
| ----------------- | ------ | ------ |
| Vuokra              | 100,000 |        |
| Toimittaja A          |        | 100,000 |
| Toimittaja A          | 11,330  |        |
| TDS-maksettava       |        | 10,000  |
| Lisämaksumaksettava |        | 1 000   |
| PE-Cess -maksettava   |        | 220    |
| SHE-Cess -maksettava  |        | 110    |
