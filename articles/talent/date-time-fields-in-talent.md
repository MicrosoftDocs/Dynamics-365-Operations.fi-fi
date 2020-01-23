---
title: Päivämäärän ja ajan käyttäminen Microsoft Dynamics 365 Talentissa
description: Tietoja siitä, mitä tapahtuu, kun Päivämäärä- ja Aika-kenttiä käytetään Microsoft Dynamics 365 Talentissa. Saat tietää, mitä on odotettavissa, kun päivämäärä- ja aikatietoja käytetään Talentin lomakkeessa, ulkoisessa lähteessä tai Common Data Servicessä.
author: Darinkramer
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5f5bb3432ba3e57a4ef08dfa3c25cb61705efc33
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898755"
---
# <a name="work-with-date-and-time-in-microsoft-dynamics-365-talent"></a>Päivämäärän ja ajan käyttäminen Microsoft Dynamics 365 Talentissa

**Päivämäärä- ja Aika-** kentät ovat Dynamics 365 Talentin peruskäsitteitä. On tärkeää ymmärtää, miten **Päivämäärä ja aika** -tietoja käytetään Dynamics 365 -lomakkeessa, Common Data Servicessä ja ulkoisissa lähteissä.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Tietoja Päivämäärä- ja Päivämäärä ja aika -tietotyyppien eroista

**Päivämäärä ja aika** -kentissä on aikavyöhyketietoja, joita ei ole **Päivämäärä**-kentissä. **Päivämäärä**-kentät näyttävät samat tiedot kaikissa sijainneissa. Kun **Päivämäärä**-kenttään annetaan tietoja, Talent kirjoittaa saman päivämäärän tietokantaan.

Kun tiedot näytetään **Päivämäärä ja aika** -kentässä, Talent mukauttaa päivämäärää ja aikaa **Käyttäjän asetukset** -lomakkeessa (**Yleinen > Asetukset > Käyttäjän asetukset**) määritettyjen käyttäjän aikavyöhykkeen perusteella. Kenttään annetut päivämäärä- ja aikatiedot eivät välttämättä ole samat kuin tietokantaan kirjoitettavat tiedot.

[![Käyttäjän asetukset -lomake](./media/useroptionsform.png)](./media/useroptionsform.png)

## <a name="understanding-date-and-time-fields-in-forms"></a>Tietoja lomakkeiden Päivämäärä ja aika -kentistä 

Kun tietoja annetaan **Päivämäärä ja aika** -kentässä, näytössä näkyvät tiedot eivät ole samoja kuin tietokantaan tallennetut tiedot, jos käyttäjän vyöhykkeeksi ei ole määritetty UTC (Coordinated Universal Time) -aika. **Päivämäärä ja aika** -kenttien tiedot tallennetaan aina UTC-aikana.

[![Työntekijä-lomake](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Tietoja tietokannan Päivämäärä ja aika -kentistä 

Kun Talent kirjoittaa **Päivämäärä ja aika** -arvon tietokannan, se tallentaa tiedot UTC-ajassa. Tällä tavoin käyttäjät näkevät **Päivämäärä ja aika** -tiedot suhteessa käyttäjän asetuksissa määritettyyn aikavyöhykkeeseen.
 
Edellä olevassa esimerkissä aloitusaika on ajankohta, ei tietty päivämäärä. Kun kirjautuneen käyttäjän aikavyöhyke muutetaan siten, että GMT +12:00 on nyt GMT UTC, samassa juuri luodussa tietueessa näkyy 04/30/2019 12:00:00 eikä 05/01/2019 12:00:00.
  
Jäljempänä olevassa esimerkissä työntekijän 000724 työsuhde aktivoituu samaan aikaan aikavyöhykkeestä riippumatta. Työntekijä aktivoituu 04/30/2019 GMT-aikavyöhykkeellä, mikä on sama kuin 05/01/2019 GMT+12:00 -aikavyöhykkeellä. Kumpikin viittaa samaan ajankohtaan eikä tiettyyn päivämäärään. 

[![Työntekijä-lomake](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a>Data Management Frameworkin, Excelin, Common Data Servicen ja Power BI:n päivämäärä ja aikatiedot 

Data Management Framework, Excel-lisäosa, Common Data Service ja Power BI -raportointi on suunniteltu käyttämään tietoja suoraan tietokantatasolla. Koska mikään asiakas ei muuta **Päivämäärä ja aika** -tietoja käyttäjän aikavyöhykkeen mukaiseksi, kaikki **Päivämäärä ja aika** -tiedot ilmoitetaan UTC-aikoina, mikä voi saada aikaan virheellisiä olettamuksia tietoja annettaessa tai tarkasteltaessa.  
 
Tietokanta olettaa, että DMF:n, Excelin tai Common Data Servicen kautta lähetettävien **Päivämäärä ja aika** -tiedot ovat UTC-aikoja. Tämä voi aiheuttaa sekaannusta, kun lähetetty **Päivämäärä ja aika** -arvo ei näy odotetusti, koska tietoja tarkastelevan käyttäjän aikavyöhykkeeksi ei ole määritetty UTC-aikaa. 
 
Näin voi käydä (käänteisesti) myös tietoja vietäessä. Viedyn DMF-yksikön **Päivämäärä ja aika** -tiedot voivat olla erilaiset kuin Dynamics-asiakasohjelmassa näkyvät tiedot. 
 
Kun tietojen katsomiseen ja luomiseen käytetään ulkoisia lähteitä, kuten DMF:tä, on tärkeää muistaa, että **Päivämäärä ja aika** -arvojen oletetaan olevan oletusarvoisesti UTC-arvoja riippumatta siitä, mikä on käyttäjän tietokoneen aikavyöhyke tai mitkä ovat nykyisen käyttäjän aikavyöhykeasetukset. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Esimerkkejä saman tietueen näkymisestä eri tuotantoalueilla 

**Talent, kun käyttäjän aikavyöhykkeeksi on määritetty UTC**

[![Työntekijä-lomake](./media/worker-form3.png)](./media/worker-form3.png)

**Talent, kun käyttäjän aikavyöhykkeeksi on määritetty GMT +12:00** 

[![Työntekijä-lomake](./media/worker-form4.png)](./media/worker-form4.png)

**Excel ODatan kautta**

[![Excel ODatan kautta](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMF-vaiheet**

[![DMF-vaiheet](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMF-vienti**

[![DMF-vaiheet](./media/DMFexport.png)](./media/DMFexport.png)

**Excel Common Data Servicen kautta**

[![Excel Common Data Servicen kautta](./media/ExcelCDS.png)](./media/ExcelCDS.png)

### <a name="see-also"></a>Lisätietoja

[Päivämäärä ja aikatiedot](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Käyttäjän ensisijaiset aikavyöhykkeet](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
