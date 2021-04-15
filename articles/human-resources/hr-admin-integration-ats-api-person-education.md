---
title: Henkilön koulutus
description: Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Henkilön koulutus -yksikköä.
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
ms.openlocfilehash: e615947ad327136d2a260ee3784a4f5728612795
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798102"
---
# <a name="person-education"></a>Henkilön koulutus

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Henkilön koulutus -yksikköä.

Fyysinen nimi: mshr_hcmpersoneducationentity

## <a name="description"></a>kuvaus

Tämä yksikkö sisältää hakijan koulutushistorian. Koulutus linkitetään henkilötietueeseen, jonka ansiosta koulutus voidaan liittää henkilölle hakijan tietueen lisäksi luotuihin muihin rooleihin (työntekijä, alihankkija ja niin edelleen).

## <a name="json-representation"></a>JSON-esitys

```json
{
    "mshr_creditbasis": Int,
    "mshr_creditscompleted": Decimal,
    "mshr_creditsearned": Decimal,
    "mshr_creditsneeded": Decimal,
    "mshr_description": "String",
    "mshr_duration": Decimal,
    "mshr_durationunit": Int,
    "mshr_educationdisciplineid": "String",
    "mshr_educationinstitutionid": "String",
    "mshr_educationlevelid": "String",
    "mshr_enddate": "Date",
    "mshr_gradepointaverage": Decimal,
    "mshr_gradescale": "String",
    "mshr_notes": "String",
    "mshr_secondaryemphasis": "String",
    "mshr_startdate": "Date",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_educationinstitution_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmpersoneducationentityid": "Guid"
}
```

## <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Henkilön koulutuksen yksikkötunnus**<br>mshr_hcmpersoneducationentityid<br>*GUID* | Vain luku<br>Vaadittu | Järjestelmän luoma henkilön koulutuksen yksikkötietueen yksilöivä tunnus. |
| **Osapuolinumero**<br>mshr_partynumber<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Hakijan osapuolen (henkilön) tietueen yksilöivä tunnus. |
| **Henkilötunnuksen arvo**<br>_mshr_fk_person_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_dirpersonentity-yksikön mshr_dirpersonentityid | Järjestelmän luoma hakijan henkilötietueen yksilöivä tunnus. |
| **Opintoyksikön perusta**<br>mshr_creditbasis<br>*mshr_hcmeducationcreditbasis-asetusjoukko* | Luku/Kirjoitus<br>Valinnainen | Koulutuksen tutkinnon opintoyksikön peruste. |
| **Valmiit opintoyksiköt**<br>mshr_creditscompleted<br>*Desimaali* | Luku/Kirjoitus<br>Valinnainen | Koulutuksessa suoritettujen opintoyksiköiden määrä. |
| **Saadut opintoyksiköt**<br>mshr_creditsearned<br>*Desimaali* | Luku/Kirjoitus<br>Valinnainen | Kesken olevan tutkinnon koulutustietueen ansaitut opintoyksiköt. |
| **Tarvittavat opintoyksiköt**<br>mshr_creditsneeded<br>*Desimaali* | Luku/Kirjoitus<br>Valinnainen | Käynnissä olevaa tutkintoa varten tarvittavien opintoyksiköiden määrä. |
| **Kuvaus**<br>mshr_description<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Hakijan tutkinnon kuvaus. |
| **Koulutustason tunnus**<br>mshr_educationlevelid<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Koulutustason tunnus. | 
| **Koulutustason tunnuksen arvo**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | Vain luku<br>Valinnainen<br>Viiteavain: mshr_hcmeducationdegreeentity-yksikön mshr_hcmeducationdegreeentityid | Järjestelmän luoma koulutustutkintotietueen tunnus. Tämä tunnus määrittää organisaatiolle määritetyt tutkinnot ja koulutustasot. |
| **Koulutusalan tunnus**<br>mshr_educationdisciplineid<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu<br>Viiteavain: EducationDiscipline | Koulutusalan tunnus. |
| **Koulutusalan tunnuksen arvo**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | Vain luku<br>Vaadittu<br>Viiteavain: mshr_hcmeducationdisciplineentity-yksikön mshr_hcmeducationdisciplineentityid | Järjestelmän luoma koulutustietueen koulutusalan yksilöivä tunnus. |
| **Toissijainen painotus**<br>mshr_secondaryemphasis<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Ansaitun tutkinnon toissijainen painotus. |
| **Koulutuslaitoksen tunnus**<br>mshr_educationinstitutionid<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Oppilaitoksen tunnus. |
| **Koulutuslaitoksen tunnuksen arvo**<br>_mshr_fk_educationinstitution_id_value<br>*GUID* | Vain luku<br>Valinnainen<br>Viiteavain: mshr_hcmeducationinstitutionentity-yksikön mshr_hcmeducationinstitutionentityid | Järjestelmän luoma oppilaitoksen tunnus. |
| **Aloituspäivä**<br>mshr_startdate<br>*Datetime* | Luku/Kirjoitus<br>Valinnainen | Ansaitun tutkinnon koulutuksen aloituspäivä. |
| **Päättymispäivä**<br>mshr_enddate<br>*Datetime* | Luku/Kirjoitus<br>Vaadittu | Päivä, jolloin ansio myönnettiin. |
| **Kesto**<br>mshr_duration<br>*Desimaali* | Luku/Kirjoitus<br>Valinnainen | Koulutustietueen kesto. |
| **Keston yksikkö**<br>mshr_durationunit<br>*mshr_periodunit-asetusjoukko* | Luku/Kirjoitus<br>Valinnainen | Koulutustietueen kestoon liittyvä aikayksikkö. |
| **Arvosanojen keskiarvo**<br>mshr_gradepointaverage<br>*Desimaali* | Luku/Kirjoitus<br>Valinnainen | Tutkinnon arvosanojen keskiarvo. |
| **Arvostelusteikko**<br>mshr_gradescale<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Tutkinnon arvosanojen keskiarvon asteikko. |
| **Muistiinpanot**<br>mshr_notes<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Muistiinpanot rekrytoijan tai työhönottopäällikön käyttöön. |
| **Ensisijainen kenttä**<br>mshr_primaryfield<br>*Merkkijono* | Vain luku<br>Vaadittu | Kenttä, jota käytetään yksikkötietueen toisena ensisijaisena tunnuksena. Osapuolen numeron, koulutusalan tunnuksen, koulutuslaitostunnuksen ja koulutustason tunnuksen yhdistelmä. |

## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely palkattavalle hakijalle](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]