---
title: "Saapuvien asiakirjojen jäsentäminen Microsoft Excelissä"
description: "Tässä ohjeaiheessa on tietoja sähköisen raportoinnin (ER) muotojen suunnittelusta, jotta se voi jäsentää sisältöä saapuvissa Microsoft Excel -tiedostoissa."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 001e287590b9f43ed38de803bcace3a25a6f6637
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2018

---

# <a name="parse-incoming-microsoft-excel-files"></a>Saapuvien Microsoft Excel -tiedostojen jäsentäminen

[!include[banner](../includes/banner.md)]

Voit suunnitella sähköisen raportoinnin (ER) muodot jäsentämään saapuvia Microsoft Excel -tiedostoja, jotka edustavat tietoja Microsoft Excel -työkirjoissa (XLSX-tiedostot). Sitten voit käyttää näiden tiedostojen sisältöä sovelluksen tietojen päivittämiseen. Tämä on hyödyllistä, kun esimerkiksi:

-   Suunnittelet uutta mallia ja muotoa ja haluat testata niitä suorituksen aikana. Tässä tapauksessa Excel simuloi todellisia sovellustietoja.
-   Hallita soveluksen ulkopuolisia tietoja Excelissä ja tuoda nämä tiedot lähettäksesi tietyn raportin.

Saat lisätietoja tästä ominaisuudesta toistamalla tehtäväoppaat **ER - Tuo tiedot Microsoft Excel -tiedostosta (osa 1: Muodon suunnittelu)** ja **ER -tuo tiedot Microsoft Excel -tiedostosta (osa 2: tietojen tuominen)** (osia 7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677) -liiketoimintaprosessissa). Nämä tehtäväoppaat käyvät läpi, kuinka saapuva Excel-tiedosto voidaan jäsentää käyttäen ER-muotoa, jotta voidaan tuoda tietoja saapuvista asiakirjoista ja päivittää sovellustiedot. Voit ladata tehtäväoppaan tiedostot [Microsoft Download Centeristä](https://go.microsoft.com/fwlink/?linkid=874684).

Lataa seuraavat tiedostot suorittaaksesi yo. tehtäväoppaat:

| Sisällön kuvaus                        | Tiedosto                                                                       |
---------------------------------------------|----------------------------------------------------------------------------|
| Saapuva tiedosto .XLSX-muodossa - malli   | [1099import-template.xlsx](https://go.microsoft.com/fwlink/?linkid=862266)  |
| Saapuva tiedosto .XLSX-muodossa - näytetiedot| [1099import-data.xlsx](https://go.microsoft.com/fwlink/?linkid=862266)     |

Jos et ole vielä toistanut tehtäväopasta [ER – Luo vaaditut konfiguraatiot tietojen tuomiseksi ulkoisesta tiedostosta](./tasks/er-required-configurations-import-data.md) nykyisessä Dynamics 365 for Finance and Operations -sovelluksessa, lataa seuraava tiedosto.

| Sisällön kuvaus                        | Tiedosto                                                                       |
---------------------------------------------|----------------------------------------------------------------------------|
| ER_mallin määritys                     | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=862266)            |


