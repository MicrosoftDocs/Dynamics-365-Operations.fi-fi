---
title: Varmenteen tyyppi
description: Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Todistuksen tyyppi -yksikköä.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1d2d53a628ef43d50bd83fd6b62807f44eddd653
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125710"
---
# <a name="certificate-type"></a>Varmenteen tyyppi

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