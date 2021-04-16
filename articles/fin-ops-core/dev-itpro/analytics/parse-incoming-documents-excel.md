---
title: Saapuvien asiakirjojen jäsentäminen Excel-muodossa
description: Tässä ohjeaiheessa on tietoja sähköisen raportoinnin (ER) muotojen suunnittelusta, jotta se voi jäsentää sisältöä saapuvissa Microsoft Excel -tiedostoissa.
author: NickSelin
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 0c41a062d817307adb2889d3678764f1ea4066e2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755177"
---
# <a name="parse-incoming-documents-in-excel-format"></a>Saapuvien asiakirjojen jäsentäminen Excel-muodossa

[!include[banner](../includes/banner.md)]

Voit suunnitella sähköisen raportoinnin (ER) muodot jäsentämään saapuvia Microsoft Excel -tiedostoja, jotka edustavat tietoja Microsoft Excel -työkirjoissa (XLSX-tiedostot). Sitten voit käyttää näiden tiedostojen sisältöä sovelluksen tietojen päivittämiseen. Tämä on hyödyllistä, kun esimerkiksi:

- Suunnittelet uutta mallia ja muotoa ja haluat testata niitä suorituksen aikana. Tässä tapauksessa Excel simuloi todellisia sovellustietoja.
- Hallita soveluksen ulkopuolisia tietoja Excelissä ja tuoda nämä tiedot lähettäksesi tietyn raportin.

Saat lisätietoja tästä ominaisuudesta toistamalla tehtäväoppaat **ER - Tuo tiedot Microsoft Excel -tiedostosta (osa 1: Muodon suunnittelu)** ja **ER - Tuo tiedot Microsoft Excel -tiedostosta (osa 2: tietojen tuominen)** (osia 7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677) -liiketoimintaprosessissa). Nämä tehtäväoppaat käyvät läpi, kuinka saapuva Excel-tiedosto voidaan jäsentää käyttäen ER-muotoa, jotta voidaan tuoda tietoja saapuvista asiakirjoista ja päivittää sovellustiedot. Voit ladata tehtäväoppaan tiedostot [Microsoft Download Centeristä](https://go.microsoft.com/fwlink/?linkid=874684).

Lataa seuraavat tiedostot suorittaaksesi yo. tehtäväoppaat:

| Sisällön kuvaus                         | Tiedosto                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| Saapuva tiedosto .XLSX-muodossa - malli    | [1099import-template.xlsx](https://go.microsoft.com/fwlink/?linkid=862266) |
| Saapuva tiedosto .XLSX-muodossa - näytetiedot | [1099import-data.xlsx](https://go.microsoft.com/fwlink/?linkid=862266)     |

Jos et ole vielä toistanut tehtäväopasta [ER Luo vaaditut konfiguraatiot tietojen tuomiseksi ulkoisesta tiedostosta](./tasks/er-required-configurations-import-data.md) nykyisessä Finance and Operations -sovelluksessa, lataa seuraava tiedosto.

| Sisällön kuvaus    | Tiedosto                                                            |
|------------------------|-----------------------------------------------------------------|
| ER_mallin määritys | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=862266) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]