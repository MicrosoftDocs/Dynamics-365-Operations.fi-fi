---
title: Varmenteen tyyppi
description: Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Todistuksen tyyppi -yksikköä.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fe5713b6b5f38ad7f6857b36c6b2f63a1dc0c320
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798390"
---
# <a name="certificate-type"></a>Varmenteen tyyppi

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Todistuksen tyyppi -yksikköä.

Fyysinen nimi: mshr_hcmcertificatetypeentity

## <a name="description"></a>kuvaus

Tämä yksikkö määrittää Human Resourcesissa määritettyjen ammatillisten todistustyyppien luettelon. Yksikkö ei ole yrityskohtainen.

## <a name="json-representation"></a>JSON-esitys

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Todistuksen tyypin yksikkötunnus**<br>mshr_hcmcertificatetypeentityid<br>*GUID* | Vain luku<br>Vaadittu 
Järjestelmän luoma | Todistustyypin yksilöivä ensisijainen tunnus. |
| **Todistuksen tyyppi**<br>mshr_certificatetype<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Käyttäjän luettava todistustyypin yksilöivä tunnus. |
| **Kuvaus**<br>mshr_description<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Todistustyypin kuvaus. |
| **Pakollinen uudistaminen**<br>mshr_requirerenewal<br>*mshr_noyes-asetusjoukko* | Luku/Kirjoitus<br>Valinnainen | Osoittaa, vaatiiko todistus uusimista. |

## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely palkattavalle hakijalle](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]