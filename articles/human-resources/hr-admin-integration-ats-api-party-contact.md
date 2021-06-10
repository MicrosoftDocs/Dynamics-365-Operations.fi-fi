---
title: Osapuolen yhteyshenkilö
description: Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Osapuolen yhteyshenkilö -yksikköä.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b37910f10c0d89e2659aa0bfbdc601c3592f896c
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053800"
---
# <a name="party-contact"></a>Osapuolen yhteyshenkilö

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Osapuolen yhteyshenkilö -yksikköä.

Fyysinen nimi: mshr_dirpartycontactentities

## <a name="description"></a>kuvaus

Tämä yksikkö kuvaa hakijan yhteystiedot, kuten puhelimen, sähköpostin ja sosiaalisen median tilit.

## <a name="json-representation"></a>JSON-esitys

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_type": Int,
    "mshr_countryregioncode": "String",
    "mshr_locator": "String",
    "mshr_locatorextension": "String",
    "mshr_purpose": "String",
    "mshr_ismobilephone": Int,
    "mshr_isinstantmessage": Int,
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "String",
    "mshr_dirpartycontactentityid": "String"
}
```

## <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Osapuolen yhteyshenkilön yksikön tunnus**<br>mshr_dirpartycontactentityid<br>*Merkkijono* | Vain luku<br>Vaadittu | Järjestelmän luoma yksikkötietueen yksilöivä tunnus. |
| **Osapuolinumero**<br>mshr_partynumber<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Liittyvän osapuolen (henkilön) tietueen tunnus. |
| **Henkilötunnuksen arvo**<br>_mshr_fk_person_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_dirpersonentity-yksikön mshr_dirpersonentityid | Järjestelmän luoma osapuolen (henkilön) yksikkötietueen tunnus. |
| **Sijainnin tunnus**<br>mshr_locationid<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Osoitetietueen sijaintitunnus. Määirtä mshr_logisticspostaladdresslocationcdsentity-yksikössä. |
| **Kuvaus**<br>mshr_description<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Yhteystietojen kuvaus. |
| **Laji**<br>mshr_type<br>*mshr_logisticselectronicaddressmethodtype-asetusjoukko* | Luku/Kirjoitus<br>Vaadittu | Yhteyshenkilön erittelytyyppi. |
| **Maa-/aluekoodi**<br>mshr_countryregioncode<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Osoitteen maa tai alue. |
| **Paikannin**<br>mshr_locator<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Yhteystiedon tiedot. Jos tyyppi on esimerkiksi **Sähköpostiosoite**, tämä kenttä sisältää hakijan sähköpostiosoitteen. |
| **Paikantimen laajennus**<br>mshr_locatorextension<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Paikantimen laajennus. Jos tyyppi on esimerkiksi **Puhelin**, tämä ominaisuus sisältää puhelinnumeron alanumeron. |
| **On matkapuhelin**<br>mshr_ismobile<br>*mshr_noyes-asetusjoukko* | Luku/Kirjoitus<br>Vaadittu | Määrittää, onko puhelinnumero matkapuhelinnumero. |
| **On pikasanoma**<br>mshr_isinstantmessage<br>*mshr_noyes-asetusjoukko* | Luku/Kirjoitus<br>Vaadittu | Määrittää, onko puhelimessa käytössä pikaviestipalvelu. |
| **On ensisijainen**<br>mshr_isprimary<br>*mshr_noyes-asetusjoukko* | Luku/Kirjoitus<br>Vaadittu | Määrittää yhteyshenkilötyypin ensisijaisen yhteyshenkilön. Yhteyshenkilötyyppiä kohti on oltava vain yksi ensisijainen tietue. |
| **On yksityinen**<br>mshr_isprivate<br>*mshr_noyes-asetusjoukko* | Luku/Kirjoitus<br>Vaadittu | Määrittää, onko tämä osoite henkilön yksityinen osoite. |
| **Tarkoitus**<br>mshr_purpose<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Yhteystietojen tarkoitus/rooli. |
| **Ensisijainen kenttä**<br>mshr_primaryfield<br>*Merkkijono* | Vain luku<br>Vaadittu | Kenttä, jota käytetään yksikkötietueen ensisijaisena tunnuksena. Osapuolen numeron, tyypin, kuvauksen ja paikantimen yhdistelmä. |

## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely palkattavalle hakijalle](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]