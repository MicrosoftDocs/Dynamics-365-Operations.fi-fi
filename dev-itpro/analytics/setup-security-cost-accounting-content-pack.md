---
title: "Kustannuslaskennan analyysi BI virran sisällön suojauksen määrittäminen"
description: "Tässä ohjeaiheessa kerrotaan, miten access-suojauksen kustannuslaskennan rivitason Microsoft Power BI-suojaus voi levitä. Tämä toiminto auttaa takaamaan, että käyttäjät näkevät vain virtaa BI-tiedot, jotka heille on myönnetty pääsy."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 1e42622e7621c645d7eda3299f78c34c7e41a251
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Kustannuslaskennan analyysi BI virran sisällön suojauksen määrittäminen

Tässä ohjeaiheessa kerrotaan, miten access-suojauksen kustannuslaskennan rivitason Microsoft Power BI-suojaus voi levitä. Tämä toiminto auttaa takaamaan, että käyttäjät näkevät vain virtaa BI-tiedot, jotka heille on myönnetty pääsy.

<a name="overview"></a>Yleiskuvaus
--------

**Kustannuslaskennan analyysi** Microsoft Power BI sisältö käyttää virtaa BI rivitason security voit rajoittaa käyttäjän oikeudet. Suojaus perustuu käyttöoikeustason organisaation hierarkian, joka on määritetty Kustannuslaskenta-parametrit. Lisätietoja **kustannuslaskennan analyysi** sisältöä, katso BI virran [kustannuslaskennan analyysin sisältöä virtaa BI](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Luo perustiedot
Käyttöoikeustason vakuuden BI virran välittämiseen BI virran sisällön omistajan on tehtävä nämä toimet. **Huomautus:** käyttäjä, joka julkaisee **kustannuslaskennan analyysi** BI virran sisältö muuttuu automaattisesti omistajalle. Vain omistaja voi määrittää BI virran suojauksen. Lisäksi, kunnes omistaja Lisää muut käyttäjät PowerBI.com, kukaan paitsi omistaja voi nähdä tietoja **kustannuslaskennan analyysi** virtaa BI-sisältöä.

1.  Julkaise määritystiedoston BI virran.
2.  Kirjaudu PowerBI.com.
3.  Dataset-Etsi **kustannuslaskennan analyysi** virtaa BI-sisältöä.
4.  Avaa Suojaus-välilehti. 

    [![Suojaus-sivun avaaminen](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)

5.  **Kustannusten objektin ohjauskoneen** rooli on jo luotu. Lisätä muita jäseniä, jotka ovat osa kustannuslaskennan käyttöoikeustason organisaation hierarkian. 

    [![Jäsenten lisääminen](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)

Käyttäjille, jotka lisätään **kustannusten objektin ohjauskoneen** roolin näkevät vain ne tiedot, he voivat tarkastella kustannuslaskennan käyttöoikeustason organisaatiohierarkian määritelmän mukaan. **Huomautus:** rivitason suojaus koskee laatat ja Microsoft Dynamics-365 toiminnot, jotka on upotettu Power BI-raportteihin.

## <a name="updating-security"></a>Suojauksen päivittäminen
Jos päivitykset tehdään Accessin käyttäjätason suojauksen kustannuslaskennan ja haluat Power BI näitä päivityksiä, sinun on päivitettävä yksikön säilöön **kustannuslaskennan analyysi** virtaa BI-sisältöä. Kun työvaiheiden 365 Dynamics yksikön myymälän päivitys on valmis, Päivitä palvelutiedot, PowerBI.com. Katso lisätietoja yksikön myymälän päivityksen tekemisestä [päivitys yksikön myymälä](power-bi-integration-entity-store.md#update-entity-store). Omistaja **kustannuslaskennan analyysi** virtaa BI sisältöä myös Tee yksikön säilöä päivitystä, jos uusille käyttäjille myönnetään käyttöoikeudet organisaation hierarkian. Lisäksi omistajan täytyy lisätä uusia käyttäjiä **kustannusten objektin ohjauskoneen** roolin PowerBI.com, joten niitä käytetään kyseisen rivin suojauksen.

## <a name="disabling-security"></a>Suojauksen poistaminen käytöstä
Oletetaan, että organisaatiosi haluaa rajoittaa tietojen käyttö. Jos jostain syystä on poistettu käytöstä suojausparametreja, kun suoritat kustannuslaskennan, omistaja on lisättävä käyttäjiä **Kustannuslaskija** virtaa BI-roolin sijaan. Jos muutat suojaus käytössä-tila käytöstä poistettua, kannattaa poistaa käyttäjiä **kustannusten objektin ohjauskoneen** rooli. Ja päinvastoin, jos otat suojauksen uudelleen. Käyttäjät voivat kuulua molempia rooleja. Yhteinen käyttö on unionin molempia rooleja. On kyse **kustannuslaskennan analyysi** virtaa BI sisällön käyttäjät, joilla on yhteinen käyttö on rajoittamaton tietojen käytön. Jos haluaa käyttää käyttöoikeuksia on rajoitettu, käyttäjille on määritettävä ainoastaan **kustannusten objektin ohjauskoneen** rooli. Rivitason nämä tietoturvapäivitykset tulevat voimaan heti. Haavoittuvuuden käyttäjät olisi päivittää selaimillaan.

## <a name="additional-resources"></a>Lisäresurssit
Katso lisätietoja BI virran rivi suojauksen [virtaa BI-mallissa suojausvyöhykkeet](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).


