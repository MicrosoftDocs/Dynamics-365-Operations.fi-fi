---
title: "Yhdistäminen ohjejärjestelmään"
description: "Tämä ohjeaihe sisältää Microsoft Dynamics 365 for Finance and Operations -ohjejärjestelmän komponenttien kuvauksen, niiden yhdistämistapojen yleiskatsauksen ja mukautetun ohjeen yhteenvedon."
author: margoc
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: acb832c422ccb5ddb98d6ddd6b69d2e2c3e11057
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---

# <a name="connect-the-help-system"></a>Yhdistäminen ohjejärjestelmään

[!include[banner](../includes/banner.md)]


Tämä ohjeaihe kuvaa Finance and Operationsin ohjejärjestelmän komponentit. Se tarjoaa näiden komponenttien yhdistämistapojen yleiskatsauksen ja mukautetun ohjeen luomisen yhteenvedon. 

## <a name="help-architecture"></a>Ohjearkkitehtuuri
Seuraavassa kuvassa on osa Finance and Operationsin ohjejärjestelmästä. Tuotteen ohjejärjestelmä käyttää Dynamics 365 for Finance and Operations -sivuston (https://docs.microsoft.com) artikkeleja sekä Lifecycle Servicesin (LCS) liiketoimintaprosessin mallintajaan tallennettuja tehtäväoppaita. 
> [!NOTE]
> Jos kaaviossa on ominaisuuden vieressä tähtimerkki (\*), ominaisuutta suunnitellaan mutta se ei ole vielä käytössä. [![Ohjearkkitehtuuri](./media/help-architecture.png)](./media/help-architecture.png)


## <a name="connecting-the-help-system"></a>Yhteyden muodostaminen ohjejärjestelmään
> [!NOTE]
> **Tehtäväoppaat**-välilehti ei ole tällä hetkellä käytettävissä Microsoft Dynamics 365 for Talentissa ja Microsoft Dynamics 365 for Retailissa. Tämän toiminnon käyttöönottamista myöhemmissä versiossa ollaan toteuttamassa. Perustoimintoja koskevat Talentin aloituskokemuksen tehtäväoppaat ovat edelleen käytettävissä. Retailin ja Talentin menettelyohje on saatavana myös docs.microsoft.com-sivustossa ([docs.microsoft.com/dynamics365/operations](/dynamics365/unified-operations/fin-and-ops/index)).
 

Järjestelmänvalvojat voivat muodostaa **Järjestelmäparametrit**-lomakkeella yhteyden käyttöönotettaviin ohjejärjestelmän osiin. [![Järjestelmäparametrit-lomake ja ohjeen asetukset](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) Toimi seuraavasti **Järjestelmän parametrit** -sivulla:

> [!IMPORTANT]
> Kun avaat **Ohje**-välilehden ensimmäisen kerran, sinun on muodostettava yhteys Lifecycle Services -palveluun. Valitse lomakkeen keskellä oleva linkki, odota yhteyden muodostumista, sulje valintaikkuna ja nouda **Järjestelmäparametrit**-sivu valitsemalla **OK**. [![Yhdistä LCS:ään](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)

1.  Valitse Lifecycle Services -projekti, johon yhteys muodostetaan.
2.  Valitse BPM-kirjastot (valitussa projektissa), josta tehtävätallenteet noudetaan.
    - Valitse Finance and Operationsissa Microsoft-sisältöä varten helmikuun 2017 QPC Unified Library for Microsoft Dynamics 365 for Finance and Operations. 
    - Retail-kirjasto julkaistaan heinäkuussa. 
    - Talent-kirjastoa ei tarvitse valita, sillä järjestelmä muodostaa yhteyden oikeaan kirjastoon puolestasi. 

3.  Määritä BPM-kirjastojen näyttöjärjestys. Tämä asetus määrittää, missä järjestyksessä kirjastojen tehtävätallenteet näkyvät **Ohje**-sivulla.

Kun olet suorittanut nämä vaiheet, voit avata **Ohje**-ruudun ja valita **Tehtävän ohjaukset** -välilehden. Näet nyt sitä sivua koskevat tehtäväoppaat, jolla nyt olet Finance and Operationsissa. Jos tehtävän ohjauksia ei löydy, tarkenna hakua avainsanoilla.

### <a name="showing-translated-task-guides"></a>Käännettyjen tehtäväoppaiden näyttäminen

Käännetyt tehtäväoppaat toimitettiin toukokuun 2016 yhdistetyssä APQC-kirjastossa ja käytön aloituskirjastossa. Jos haluat avata lokalisoidun tehtäväoppaan ohjeen Finance and Operationsissa, varmista, että olet muodostanut yhteyden toukokuun kirjastoon. Kullekin käyttäjälle avautuvan tehtäväoppaan kieli määräytyy kieliasetuksissa, jotka on valittu kohdassa **Asetukset** &gt; **Asetukset**. 

> [!NOTE]
> Vaikka useita tehtäväoppaita on käännetty, tehtäväoppaiden nimet eivät näy tällä hetkellä Finance and Operationsin asiakasohjelmassa. Lisäksi vain helmikuussa 2016 julkaistujen tehtäväoppaiden käännökset ovat saatavana toukokuun kirjastossa. Lisää käännöksiä julkaistaan päivitetyssä kirjastossa.
> -   Jos tehtäväopas on käännetty, tehtäväopas avautuu valitsemallasi kielellä.
> -   Jos tehtäväopasta ei ole vielä käännetty, vain osa tekstistä (ohjausobjektien teksti) näkyy valitun kielisenä.

## <a name="creating-custom-help"></a>Mukautetun ohjeen luominen
Voit luoda oman mukautetun Finance and Operations- ja Retail -ohjeen luomalla sille tehtävätallenteita ja tallentamalla ne LCS:n liiketoimintaprosessien kirjastoon. Mukautettuja tehtäväoppaita ei voi luoda Talentissa. 

Kumppanit voivat puolestaan siirtää kirjasto yrityskirjastoon ja sisällyttää sen ratkaisuun, jos se halutaan asiakkaiden käyttöön. Voit myös kopioida yhdistetyn yleisen APQC-kirjaston sekä avata oman kopion, avata tehtävätallenteet sieltä, muokata niitä ja tallentaa sitten muutetut tallenteet. Lisätietoja on artikkelissa [Ohjeistuksena tai koulutuksena käytettävien tehtävätallenteiden luominen](../user-interface/task-recorder.md).

<a name="see-also"></a>Lisätietoja
--------

[Yleistä Ohjeesta](help-overview.md)

[Tehtävän tallennustoiminnon yleiskatsaus](../user-interface/task-recorder.md)

[Dokumentaation tai koulutuksen luominen tehtävätallenteiden avulla](../user-interface/task-recorder-training-docs.md)





