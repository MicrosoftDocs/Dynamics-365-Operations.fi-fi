---
title: Yhdistäminen ohjejärjestelmään
description: Tämä ohjeaihe sisältää Finance and Operations -sovellusten ohjejärjestelmän osien kuvauksen, niiden yhdistämistapojen yleiskatsauksen ja mukautetun ohjeen yhteenvedon.
author: margoc
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4427388d75c1aef40a978ce35c831d5b714f2562
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006169"
---
# <a name="connect-the-help-system"></a>Yhdistäminen ohjejärjestelmään

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan Finance and Operations -sovellusten, kuten Dynamics 365 Financen, Supply Chain Managementin, Commercen ja Human Resourcesin ohjejärjestelmän komponentteja. Se tarjoaa näiden komponenttien yhdistämistapojen yleiskatsauksen ja mukautetun ohjeen luomisen yhteenvedon.

## <a name="help-architecture"></a>Ohjearkkitehtuuri

Seuraavassa kuvassa on osa ohjejärjestelmästä. Tuotteen ohjejärjestelmä käyttää sivuston https://docs.microsoft.com artikkeleja sekä Lifecycle Servicesin (LCS) liiketoimintaprosessin mallintajaan tallennettuja tehtäväoppaita.

> [!NOTE]
> Jos kaaviossa on ominaisuuden vieressä tähtimerkki (\*), ominaisuutta suunnitellaan mutta se ei ole vielä käytössä.

[![Ohjearkkitehtuuri](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Yhteyden muodostaminen ohjejärjestelmään

> [!NOTE]
> **Tehtäväoppaat**-välilehteä ei ole tällä hetkellä Dynamics 365 Human Resourcesissa tai Commercessa. Tämän toiminnon käyttöönottamista myöhemmissä versiossa ollaan toteuttamassa. Perustoimintoja koskevat Human Resourcesin aloituskokemuksen tehtäväoppaat ovat edelleen käytettävissä. Menettelyohjeet ovat käytettävissä myös docs.microsoft.com-sivustossa sekä Human Resourcesille että Commercelle.

Järjestelmänvalvojat voivat muodostaa **Järjestelmäparametrit**-lomakkeella yhteyden käyttöönotettaviin ohjejärjestelmän osiin.

[![Järjestelmäparametrit-lomake ja ohjeen asetukset](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

Toimi seuraavasti **Järjestelmän parametrit** -sivulla:

> [!IMPORTANT]
> Kun avaat **Ohje**-välilehden ensimmäisen kerran, sinun on muodostettava yhteys Lifecycle Services -palveluun. Valitse lomakkeen keskellä oleva linkki, odota yhteyden muodostumista, sulje valintaikkuna ja nouda **Järjestelmäparametrit**-sivu valitsemalla **OK**.
>
> [![Muodosta yhteys LCS:ään](./media/connect-to-lcs-crop-1024x365.png "Muodosta yhteys LCS:ään")](./media/connect-to-lcs-crop.png)

1. Valitse Lifecycle Services -projekti, johon yhteys muodostetaan.
2. Valitse BPM-kirjastot (valitussa projektissa), josta tehtävätallenteet noudetaan.
3. Määritä BPM-kirjastojen näyttöjärjestys. Tämä asetus määrittää, missä järjestyksessä kirjastojen tehtävätallenteet näkyvät **Ohje**-sivulla.

Kun olet suorittanut nämä vaiheet, voit avata **Ohje**-ruudun ja valita **Tehtäväoppaat**-välilehden, jolla on näkyvissä on avointa Finance and Operations -sivua käsitteleviä tehtäväoppaita. Jos tehtävän ohjauksia ei löydy, tarkenna hakua avainsanoilla.

### <a name="showing-translated-task-guides"></a>Käännettyjen tehtäväoppaiden näyttäminen

Käännetyt tehtäväoppaat toimitettiin toukokuun 2016 yhdistetyssä APQC-kirjastossa ja käytön aloituskirjastossa. Jos haluat avata lokalisoidun tehtäväopasohjeen Finance and Operations -sovelluksissa, varmista, että olet muodostanut yhteyden toukokuun kirjastoon. Kullekin käyttäjälle avautuvan tehtäväoppaan kieli määräytyy kieliasetuksissa, jotka on valittu kohdassa **Asetukset** &gt; **Asetukset**.

> [!NOTE]
> Vaikka useita tehtäväoppaita on käännetty, tehtäväoppaiden nimet eivät näy tällä hetkellä asiakasohjelmassa. Lisäksi vain helmikuussa 2016 julkaistujen tehtäväoppaiden käännökset ovat saatavana toukokuun kirjastossa. Lisää käännöksiä julkaistaan päivitetyssä kirjastossa.
>
> - Jos tehtäväopas on käännetty, tehtäväopas avautuu valitsemallasi kielellä.
> - Jos tehtäväopasta ei ole vielä käännetty, vain osa tekstistä (ohjausobjektien teksti) näkyy valitun kielisenä.

## <a name="creating-custom-help"></a>Mukautetun ohjeen luominen

Voit luoda tehtäväoppaiden avulla mukautetun ohjeen tai yhdistää sivuston Ohje-ruutuun.

### <a name="create-custom-help-with-task-guides"></a>Mukautetun ohjeen luominen tehtäväoppaiden avulla

Voit luoda oman mukautetun Finance-, Supply Chain Management- tai Commerce-ohjeen luomalla sille tehtävätallenteita ja tallentamalla ne LCS:n liiketoimintaprosessien kirjastoon. Talentissa ei voi myöskään luoda mukautettuja tehtäväoppaita Human Resourcesille.

Kumppanit voivat puolestaan siirtää kirjasto yrityskirjastoon ja sisällyttää sen ratkaisuun, jos se halutaan asiakkaiden käyttöön. Voit myös kopioida yhdistetyn yleisen APQC-kirjaston sekä avata oman kopion, avata tehtävätallenteet sieltä, muokata niitä ja tallentaa sitten muutetut tallenteet. Lisätietoja on kohdassa [Tehtävän tallennustoiminnon resurssit](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-site"></a>Mukautetun sivuston yhdistäminen

Microsoftilla on raportti ja näytekoodi, jossa selitetään, miten mukautettu ohjesivusto luodaan ja yhdistetään Ohje-ruutuun. Lisätietoja:

- [Luo mukautettu Ohje Finance and Operations -sovelluksille (tekninen raportti)](https://go.microsoft.com/fwlink/?linkid=2041185)
- [Mukautetun ohjeen GitHub-säilö](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a>Lisäresurssit

[Ohjejärjestelmä](help-overview.md)

[Tehtävän tallennustoiminnon resurssit](../../dev-itpro/user-interface/task-recorder.md)

[Dokumentaation tai koulutuksen luominen tehtävien tallennustoiminnolla](../../dev-itpro/user-interface/task-recorder-training-docs.md)
