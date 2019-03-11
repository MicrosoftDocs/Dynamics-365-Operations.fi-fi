---
title: Yhdistäminen ohjejärjestelmään
description: Tämä ohjeaihe sisältää Microsoft Dynamics 365 for Finance and Operationsin ohjejärjestelmän osien kuvauksen, niiden yhdistämistapojen yleiskatsauksen ja mukautetun ohjeen yhteenvedon.
author: margoc
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 673b01648127fe1d19fb3c75c4d6812c4f22c761
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "317726"
---
# <a name="connect-the-help-system"></a>Yhdistäminen ohjejärjestelmään

[!include [banner](../includes/banner.md)]

Tämä ohjeaihe sisältää Microsoft Dynamics 365 for Finance and Operationsin ohjejärjestelmän osien kuvauksen. Se tarjoaa näiden komponenttien yhdistämistapojen yleiskatsauksen ja mukautetun ohjeen luomisen yhteenvedon.

## <a name="help-architecture"></a>Ohjearkkitehtuuri

Seuraavassa kuvassa on osa Finance and Operationsin ohjejärjestelmästä. Tuotteen ohjejärjestelmä käyttää Dynamics 365 for Finance and Operations -sivuston (https://docs.microsoft.com) artikkeleja sekä Lifecycle Servicesin (LCS) liiketoimintaprosessin mallintajaan tallennettuja tehtäväoppaita.

> [!NOTE]
> Jos kaaviossa on ominaisuuden vieressä tähtimerkki (\*), ominaisuutta suunnitellaan mutta se ei ole vielä käytössä.

[![Ohjearkkitehtuuri](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Yhteyden muodostaminen ohjejärjestelmään

> [!NOTE]
> **Tehtäväoppaat**-välilehteä ei ole tällä hetkellä Microsoft Dynamics 365 for Talentissa ja Microsoft Dynamics 365 for Retailissa. Tämän toiminnon käyttöönottamista myöhemmissä versiossa ollaan toteuttamassa. Perustoimintoja koskevat Talentin aloituskokemuksen tehtäväoppaat ovat edelleen käytettävissä. Retailin ja Talentin menettelyohje on saatavana myös docs.microsoft.com-sivustossa ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)).

Järjestelmänvalvojat voivat muodostaa **Järjestelmäparametrit**-lomakkeella yhteyden käyttöönotettaviin ohjejärjestelmän osiin.

[![Järjestelmäparametrit-lomake ja ohjeen asetukset](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

Toimi seuraavasti **Järjestelmän parametrit** -sivulla:

> [!IMPORTANT]
> Kun avaat **Ohje**-välilehden ensimmäisen kerran, sinun on muodostettava yhteys Lifecycle Services -palveluun. Valitse lomakkeen keskellä oleva linkki, odota yhteyden muodostumista, sulje valintaikkuna ja nouda **Järjestelmäparametrit**-sivu valitsemalla **OK**.
>
> [![Yhdistäminen LCS:ään](./media/connect-to-lcs-crop-1024x365.png "Yhdistäminen LCS:ään")](./media/connect-to-lcs-crop.png)

1. Valitse Lifecycle Services -projekti, johon yhteys muodostetaan.
2. Valitse BPM-kirjastot (valitussa projektissa), josta tehtävätallenteet noudetaan.

    - Valitse Finance and Operationsissa Microsoft-sisältöä varten uusimman APQC Unified Library for Finance and Operations.
    - Retail-kirjasto julkaistaan pian.
    - Talent-kirjastoa ei tarvitse valita, sillä järjestelmä muodostaa yhteyden oikeaan kirjastoon puolestasi.

3. Määritä BPM-kirjastojen näyttöjärjestys. Tämä asetus määrittää, missä järjestyksessä kirjastojen tehtävätallenteet näkyvät **Ohje**-sivulla.

Kun olet suorittanut nämä vaiheet, voit avata **ohjeruudun** ja valita **Tehtäväoppaat**-välilehden, jolla on näkyvissä on avointa Finance and Operations -sivua käsitteleviä tehtäväoppaita. Jos tehtävän ohjauksia ei löydy, tarkenna hakua avainsanoilla.

### <a name="showing-translated-task-guides"></a>Käännettyjen tehtäväoppaiden näyttäminen

Käännetyt tehtäväoppaat toimitettiin toukokuun 2016 yhdistetyssä APQC-kirjastossa ja käytön aloituskirjastossa. Jos haluat avata lokalisoidun tehtäväoppaan ohjeen Finance and Operationsissa, varmista, että olet muodostanut yhteyden toukokuun kirjastoon. Kullekin käyttäjälle avautuvan tehtäväoppaan kieli määräytyy kieliasetuksissa, jotka on valittu kohdassa **Asetukset** &gt; **Asetukset**.

> [!NOTE]
> Vaikka useita tehtäväoppaita on käännetty, tehtäväoppaiden nimet eivät näy tällä hetkellä Finance and Operationsin asiakasohjelmassa. Lisäksi vain helmikuussa 2016 julkaistujen tehtäväoppaiden käännökset ovat saatavana toukokuun kirjastossa. Lisää käännöksiä julkaistaan päivitetyssä kirjastossa.
>
> - Jos tehtäväopas on käännetty, tehtäväopas avautuu valitsemallasi kielellä.
> - Jos tehtäväopasta ei ole vielä käännetty, vain osa tekstistä (ohjausobjektien teksti) näkyy valitun kielisenä.

## <a name="creating-custom-help"></a>Mukautetun ohjeen luominen

Voit luoda tehtäväoppaiden avulla mukautetun ohjeen tai yhdistää sivuston Ohje-ruutuun.

### <a name="create-custom-help-with-task-guides"></a>Mukautetun ohjeen luominen tehtäväoppaiden avulla

Voit luoda oman mukautetun Finance and Operations- ja Retail -ohjeen luomalla sille tehtävätallenteita ja tallentamalla ne LCS:n liiketoimintaprosessien kirjastoon. Mukautettuja tehtäväoppaita ei voi luoda Talentissa.

Kumppanit voivat puolestaan siirtää kirjasto yrityskirjastoon ja sisällyttää sen ratkaisuun, jos se halutaan asiakkaiden käyttöön. Voit myös kopioida yhdistetyn yleisen APQC-kirjaston sekä avata oman kopion, avata tehtävätallenteet sieltä, muokata niitä ja tallentaa sitten muutetut tallenteet. Lisätietoja on artikkelissa [Ohjeistuksena tai koulutuksena käytettävien tehtävätallenteiden luominen](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-site"></a>Mukautetun sivuston yhdistäminen

Microsoftilla on raportti ja näytekoodi, jossa selitetään, miten mukautettu ohjesivusto luodaan ja yhdistetään Ohje-ruutuun. Lisätietoja:

- [Finance and Operationsin mukautetun ohjeen luominen (raportti)](https://go.microsoft.com/fwlink/?linkid=2041185)
- [Mukautetun ohjeen GitHub-säilö](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a>Lisäresurssit

[Ohjeen yleiskatsaus](help-overview.md)

[Tehtävän tallennustoiminnon yleiskatsaus](../../dev-itpro/user-interface/task-recorder.md)

[Dokumentaation tai koulutuksen luominen tehtävätallenteiden avulla](../../dev-itpro/user-interface/task-recorder-training-docs.md)
