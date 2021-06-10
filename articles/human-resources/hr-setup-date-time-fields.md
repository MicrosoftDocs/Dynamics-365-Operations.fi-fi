---
title: Ymmärrä päivämäärä- ja kellonaikakentät
description: Tietoja siitä, mitä tapahtuu, kun Päivämäärä- ja Aika-kenttiä käytetään Microsoft Dynamics 365 Human Resourcesissa.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b7e5726f7e4beea1584b9a8e142212531ba1db56
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051734"
---
# <a name="understand-date-and-time-fields"></a>Ymmärrä päivämäärä- ja kellonaikakenttiä

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Päivämäärä- ja Aika-** kentät ovat Dynamics 365 Human Resourcesin peruskäsitteitä. On tärkeää ymmärtää, miten **Päivämäärä ja aika** -tietoja käytetään lomakkeissa, Dataversessä ja ulkoisissa lähteissä.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Tietoja Päivämäärä- ja Päivämäärä ja aika -tietotyyppien eroista

**Päivämäärä ja aika** -kentissä on aikavyöhyketietoja, joita ei ole **Päivämäärä**-kentissä. **Päivämäärä**-kentät näyttävät samat tiedot kaikissa sijainneissa. Kun **Päivämäärä**-kenttään annetaan tietoja, henkilöstöhallinto kirjoittaa saman päivämäärän tietokantaan.

Kun tiedot näytetään **Päivämäärä ja aika** -kentässä, henkilöstöhallinto mukauttaa päivämäärää ja aikaa **Käyttäjän asetukset** -lomakkeessa (**Yleinen > Asetukset > Käyttäjän asetukset**) määritettyjen käyttäjän aikavyöhykkeen perusteella. Kenttään annetut päivämäärä- ja aikatiedot eivät välttämättä ole samat kuin tietokantaan kirjoitettavat tiedot.

[![Käyttäjän asetukset -lomake](./media/useroptionsform.png)](./media/useroptionsform.png)

## <a name="understanding-date-and-time-fields-in-forms"></a>Tietoja lomakkeiden Päivämäärä ja aika -kentistä 

Näytössä näkyvät **Päivämäärä ja aika** -tiedot eivät ole samoja kuin tietokantaan tallennetut tiedot, jos käyttäjän vyöhykkeeksi ei ole määritetty UTC (Coordinated Universal Time) -aika. **Päivämäärä ja aika** -kenttien tiedot tallennetaan aina UTC-aikana.

[![Työntekijä-lomake – UTC](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Tietoja tietokannan Päivämäärä ja aika -kentistä 

Kun henkilöstöhallinto kirjoittaa **Päivämäärä ja aika** -arvon tietokannan, se tallentaa tiedot UTC-ajassa. Tällä tavoin käyttäjät näkevät **Päivämäärä ja aika** -tiedot suhteessa käyttäjän asetuksissa määritettyyn aikavyöhykkeeseen.
 
Edellä olevassa esimerkissä aloitusaika on ajankohta, ei tietty päivämäärä. Kun kirjautuneen käyttäjän aikavyöhyke muutetaan siten, että GMT +12:00 on nyt GMT UTC, samassa tietueessa näkyy 04/30/2019 12:00:00 eikä 05/01/2019 12:00:00.
  
Jäljempänä olevassa esimerkissä työntekijän 000724 työsuhde aktivoituu samaan aikaan aikavyöhykkeestä riippumatta. Työntekijä aktivoituu 04/30/2019 GMT-aikavyöhykkeellä, mikä on sama kuin 05/01/2019 GMT+12:00 -aikavyöhykkeellä. Kumpikin viittaa samaan ajankohtaan eikä tiettyyn päivämäärään. 

[![Työntekijä-lomake – GMT](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a>Data Management Frameworkin, Excelin, Dataversen ja Power BI:n päivämäärä ja aikatiedot 

Data Management Framework, Excel-lisäosa, Dataverse ja Power BI -raportointi on suunniteltu käyttämään tietoja suoraan tietokantatasolla. Koska mikään asiakas ei muuta **Päivämäärä ja aika** -tietoja käyttäjän aikavyöhykkeen mukaiseksi, kaikki **Päivämäärä ja aika** -tiedot ilmoitetaan UTC-aikoina, mikä voi saada aikaan virheellisiä olettamuksia tietoja annettaessa tai tarkasteltaessa.  
 
Tietokanta olettaa, että DMF:n, Excelin tai Dataversen kautta lähetettävien **Päivämäärä ja aika** -tiedot ovat UTC-aikoja. Tämä voi aiheuttaa sekaannusta, kun lähetetty **Päivämäärä ja aika** -arvo ei näy odotetusti, koska tietoja tarkastelevan käyttäjän aikavyöhykkeeksi ei ole määritetty UTC-aikaa. 
 
Näin voi käydä (käänteisesti) myös tietoja vietäessä. Viedyn DMF-yksikön **Päivämäärä ja aika** -tiedot voivat olla erilaiset kuin Dynamics-asiakasohjelmassa näkyvät tiedot. 
 
Kun tietojen katsomiseen ja luomiseen käytetään ulkoisia lähteitä, kuten DMF:tä, kannattaa muistaa, että **Päivämäärä ja aika** -arvojen oletetaan olevan oletusarvoisesti UTC-arvoja riippumatta siitä, mikä on käyttäjän tietokoneen aikavyöhyke tai mitkä ovat nykyisen käyttäjän aikavyöhykeasetukset. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Esimerkkejä saman tietueen näkymisestä eri tuotantoalueilla 

**Henkilöstöhallinto, kun käyttäjän aikavyöhykkeeksi on määritetty UTC**

[![Työntekijä-lomake, jonka ajaksi on määritetty UTC](./media/worker-form3.png)](./media/worker-form3.png)

**Henkilöstöhallinto, kun käyttäjän aikavyöhykkeeksi on määritetty GMT +12:00** 

[![Työntekijä-lomake, jonka ajaksi on määritetty GMT](./media/worker-form4.png)](./media/worker-form4.png)

**Excel ODatan kautta**

[![Excel ODatan kautta](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMF-vaiheet**

[![DMF-vaiheet](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMF-vienti**

[![DMF-vienti](./media/DMFexport.png)](./media/DMFexport.png)

**Excel Dataversen kautta**

[![Excel Dataversen kautta](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Lisätietoja

[Päivämäärä ja aikatiedot](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Käyttäjän ensisijaiset aikavyöhykkeet](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]