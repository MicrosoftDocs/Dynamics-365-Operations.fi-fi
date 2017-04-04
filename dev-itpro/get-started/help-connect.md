---
title: "Yhdistäminen ohjejärjestelmään"
description: "Tämä aihe sisältää Microsoft Dynamics 365 for Operations -ohjejärjestelmän komponenttien kuvauksen, niiden yhdistämistapojen yleiskatsauksen ja mukautetun ohjeen yhteenvedon."
author: margoc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 5ac5e30cff2239f601778001368fa7aaba478f5c
ms.lasthandoff: 03/31/2017


---

# <a name="connect-the-help-system"></a>Yhdistäminen ohjejärjestelmään

Tässä aiheessa kuvataan ohjeen osia saat toimintoihin Microsoft Dynamics-365. Se on näiden osien yhdistäminen yleiskatsaus ja yhteenveto siitä, miten voit luoda mukautetun ohjeen. 

<a name="help-architecture"></a>Ohjearkkitehtuuri
-----------------

Seuraavassa kuvassa on osien toimintojen avulla järjestelmän Dynamics-365. Tuotteen ohjeen vetää artikkelit Dynamics-365 https://docs.microsoft.com sekä tehtävän apuviivat Business prosessi Modeler Lifecycle Services (LCS) tallennetaan sivuston toimintoja. 
**Huomautus:** ominaisuuksien luettelossa tähdellä kaaviossa (\*) on suunniteltu, mutta eivät ole vielä käytettävissä. [![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Ohjeen yhdistäminen
Käyttämällä **järjestelmäparametrit** -sivulla järjestelmänvalvojat muodostaa kappaletta toteutus ohjetta. [![Järjestelmän parametrit-lomakkeen asetusten Ohje](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) käyttöön **järjestelmäparametrit** -sivulla seuraavasti:

1.  **Tärkeää:**, joka avataan ensimmäisen kerran **Ohje** välilehdessä, sinun on muodostettava yhteys Lifecycle Services. Varmista, että linkki lomakkeen keskelle, odota yhteyden, sulje valintaikkuna ja valitse **OK** pääseminen **järjestelmäparametrit** sivulla. [![LCS muodostaa](./media/connect-to-lcs-crop-1024x365.png "muodostaa LCS")](./media/connect-to-lcs-crop.png)
2.  Valitse Lifecycle Services -projekti, johon yhteys muodostetaan.
3.  Valitse BPM-kirjastot (valitussa projektissa), josta tehtävätallenteet noudetaan.
4.  Määritä BPM-kirjastojen näyttöjärjestys. Tämä asetus määrittää, missä järjestyksessä kirjastojen tehtävätallenteet näkyvät **Ohje**-sivulla.

Kun olet suorittanut nämä vaiheet, voit avata **Ohje**-ruudun ja valita **Tehtävän ohjaukset** -välilehden. Näet nyt tehtävän ohjaukset, jotka liittyvät valittuna olevaan Dynamics 365 for Operations -sivuun. Jos tehtävän ohjauksia ei löydy, tarkenna hakua avainsanoilla.

### <a name="showing-translated-task-guides"></a>Käännettyjen tehtäväoppaiden näyttäminen

Käännetty tehtävän apuviivat toimitettiin ensimmäisen kerran toukokuussa 2016-APQC yhdistetyn kirjastoon ja kirjaston käytön aloittaminen. Jos haluat avata lokalisoidun tehtäväopasohjeen Microsoft Dynamics 365 for Operations, varmista, että olet muodostanut yhteyden toukokuun kirjastoon. Kieli, joka näkyy tehtävän opas ohjaa kunkin käyttäjän kieliasetusten **asetukset**&gt;**asetukset**. **Huomautus:** Vaikka useita tehtäväoppaita on käännetty, tehtäväoppaiden nimet eivät näy tällä hetkellä Dynamics 365 for Operations -asiakasohjelmassa. Vain joka julkaistiin helmikuu 2016 tehtävän apuviivat ovat myös käytettävissä käännös toukokuuta kirjastossa. Lisää käännöksiä julkaistaan päivitetyssä kirjastossa.

-   Jos tehtäväopas on käännetty, tehtäväopas avautuu valitsemallasi kielellä.
-   Jos tehtäväopasta ei ole vielä käännetty, vain osa tekstistä (ohjausobjektien teksti) näkyy valitun kielisenä.

## <a name="creating-custom-help"></a>Mukautetun ohjeen luominen
Voit oman mukautetun ohjeen Dynamics 365 for Operations -toteutuksella luomalla sille tehtävätallenteita ja tallentamalla se LCS:n liiketoimintaprosessien kirjastoon. Kumppanit voivat puolestaan siirtää kirjasto yrityskirjastoon ja sisällyttää sen ratkaisuun, jos se halutaan asiakkaiden käyttöön. Voit myös kopioida yhdistetyn yleisen APQC-kirjaston sekä avata oman kopion, avata tehtävätallenteet sieltä, muokata niitä ja tallentaa sitten muutetut tallenteet. Lisätietoja on ohjeaiheessa [luominen voidaan käyttää tehtävän tallennuksen tai koulutuksen](../user-interface/task-recorder.md).

<a name="see-also"></a>Lisätietoja
--------

[Help overview](help-overview.md)

[Tehtävän tallennus-yleistä](../user-interface/task-recorder.md)

[Dokumentaation tai koulutuksen luominen tehtävätallenteiden avulla](../user-interface/task-recorder-training-docs.md)

[Uusi koulutus kirjastojen luominen Dynamics 365 toimintojen sisällä elinkaari-palveluja käyttämällä tehtävän tallennus (ulkoinen linkki)](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)


