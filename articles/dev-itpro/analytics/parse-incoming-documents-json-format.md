---
title: Saapuvien asiakirjojen jäsentäminen JSON-muodossa
description: Tässä ohjeaiheessa käsitellään tapaa, jolla sähköisen raportoinnin (ER) muodot jäsentävät saapuvat asiakirjat JavaScript Object Notation (JSON) -muodossa.
author: kfend
manager: AnnBe
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 92ef83bc1783b00a4d7d9739ca1c17e863c7ff44
ms.sourcegitcommit: f6581bab16225a027f4fbfad25fdef45bd286489
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/27/2019
ms.locfileid: "1703918"
---
# <a name="parse-incoming-documents-in-json-format"></a>Saapuvien asiakirjojen jäsentäminen JSON-muodossa

[!include[banner](../includes/banner.md)]

Voit suunnitella sähköisen raportoinnin (ER) muodot jäsentämään saapuvat sähköiset asiakirjat, jotka viittaavat JavaScriptiin perustuviin tekstimuotoisiin tietoihin (eli JavaScript Object Notation \[JSON\] -muotoisiin tiedostoihin).

Saat lisätietoja tästä toiminnosta lataamalla seuraavan taulukon tiedostot ja toistamalla sitten tehtäväoppaan ER Muotokonfiguraation luominen tietojen ulkoisesta JSON-tiedostosta tuontia varten. Tämä tehtäväopas osoittaa, miten ER-muodon avulla saapuva JSON-tiedosto voidaan jäsentää päivittämään sovellustiedot.

| Titteli                                  | Tiedostonimi |
|----------------------------------------|-----------|
| ER-muodon konfigurointi                | [Toimittajien trans_JSON.xml-tiedoston tuonnin muoto](https://go.microsoft.com/fwlink/?linkid=874111) |
| Saapuvan .csv-muotoinen näytetiedosto | [1099entries_JSON. txt](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a>Tarpeet

Seuraava vaatimus on toteutettava ennen ER Muotokonfiguraation luominen tietojen ulkoisesta JSON-tiedostosta tuontia varten -tehtäväoppaan suorittamista:

- JSON-tiedoston pääelementit voivat olla vain objektielementtejä.
- Objektin sisäkkäisten elementtien on oltava ominaisuuselementtejä, jotta kelvollinen JSON-rakenne voidaan luoda.
- JSON-taulukot voivat olla vain objektin ominaisuuselementtien sisäkkäisiä elementtejä.
- JSON-taulukot voivat sisältää vain JSON-objekteja. Ne eivät voi sisältää suoria merkkijonoja tai numeroarvoja eivätkä sisäkkäisiä taulukoita. Näiden taulukoiden elementit jäsennetään muodossa määritetyssä järjestyksessä. Kunkin JSON-objektin monimuotoisuusasetukset otetaan huomioon.

Lisäksi on suoritettava [ER Luo vaaditut konfiguraatiot tietojen tuomiseksi ulkoisesta tiedostosta sähköistä raportointia varten](tasks/er-required-configurations-import-data.md) -tehtäväopas, jos sitä ei ole vielä suoritettu. Suorita tehtäväopas lataamalla seuraava tiedosto.

| Titteli                  | Tiedostonimi |
|------------------------|-----------|
| ER_mallin määritys | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=874111) |
