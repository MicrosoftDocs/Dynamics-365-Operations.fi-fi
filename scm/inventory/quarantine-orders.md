---
title: Karanteenitilaukset
description: "Tässä artikkelissa kuvataan varaston käytön estämistä karanteenitilauksilla."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 394276e6908f2c1f6bc72eea061facc3afe701e9
ms.lasthandoff: 03/31/2017


---

# <a name="quarantine-orders"></a>Karanteenitilaukset

Tässä artikkelissa kuvataan varaston käytön estämistä karanteenitilauksilla. 

Varaston käyttö voidaan estää karanteenitilauksilla. Haluat ehkä esimerkiksi syistä laadunvalvonnan kohteet karanteeniin. Varasto, joka on karanteeniin siirretään karanteenivarastoon. **Huomautus:** Jos käytät varaston lisähallintaprosesseja (Varastonhallinnassa), karanteenitilauksen käsittelyä käytetään vain palautusmyyntitilauksille.

## <a name="quarantine-onhand-inventory-items"></a>Onhand-varastonimikkeiden karanteeniin
Kun siirrät nimikkeitä karanteeniin, voit joko luoda karanteenitilauksen manuaalisesti tai määrittää järjestelmän luomaan karanteenitilaukset automaattisesti saapuvien käsittelyn aikana. Jos haluat luoda karanteenitilauksia automaattisesti, valitse **Karanteeninhallinta**-vaihtoehto **Nimikemalliryhmät**-sivun **Varastokäytännöt**-välilehdestä. Sinun täytyy myös määrittää oletuskaranteenivarasto vastaanottavien varastojen **Karanteenivarasto**-kentässä. Karanteeniin siirretyt nimikkeet siirretään Dynamics 365 for Operations -järjestelmässä automaattisesti karanteenivarastoon, kun fyysinen käytettävissä oleva varasto kirjataan ostotilauksen tai tuotantotilauksen kautta. Siirto tapahtuu, koska karanteenitilauksen tilaksi muuttuu **Aloitettu**. Luodessasi karanteenitilauksia manuaalisesti ei ole tarpeen määrittää nykyistä nimikettä karantiinihallintaa varten liitetyssä nimikemalliryhmässä. Tässä prosessissa sinun täytyy määrittää käytettävissä oleva varasto, joka on asetettava karanteeniin, sekä käytettävä karanteenivarasto. Voit käyttää prosessin suunnittelussa apuna karanteenitilauksen tiloja.

## <a name="quarantine-order-statuses"></a>Karanteenitilausten tilat
Karanteenitilauksilla voi olla seuraavanlaisia tiloja:

-   Luotu
-   Aloitettu
-   Ilmoitettu valmiiksi
-   Päättynyt

### <a name="created"></a>Luotu

Kun karanteenitilaus on luotu manuaalisesti, mutta nimikettä ei ole vielä sijoitettu karanteenivarastoon, karanteenitilauksen tilana on **Luotu**. Järjestelmä luo kaksi varastotapahtumaa. Yksi tapahtumista on ottotapahtuma, jonka tila voi olla **Tilauksessa**, **Varattu fyysinen** tai **Keräilty**. Toinen on vastaanottotapahtuma, jonka tilana karanteenivarastossa voi olla **Tilattu** tai **Rekisteröity**. Voit varata, keräillä ja rekisteröidä varaston päivityksiä käyttämällä tavanomaisia prosesseja.

### <a name="started"></a>Aloitettu

Kun karanteenitilauksen tilana on **Aloitettu**, varasto siirretään tavallisesta varastosta karanteenivarastoon, ja järjestelmä luo kaksi varastotapahtumaa. Yhdellä tapahtumalla on tila **Toimitettu**, ja toisella tapahtumalla on tila **Vastaanotettu**. Samalla luodaan kaksi varastotapahtumaa palautussiirron käsittelyä varten. Näitä tapahtumia ei päivätä. Yhdellä tapahtumalla on tila **Varattu fyysinen**, ja toisella tapahtumalla on tila **Tilattu**.

### <a name="reported-as-finished"></a>Ilmoitettu valmiiksi

Valitsemalla **Ilmoita valmiiksi**, voit ilmoittaa aloitetun karanteenitilauksen valmiiksi. Nimike vapautetaan karanteenista, mutta sitä ei siirretä vielä tavalliseen varastoon. Siirto takaisin tavalliseen varastoon voidaan käsitellä nimikkeen saapumisen kirjauskansiossa, joka voidaan alustaa Ilmoita valmiiksi -prosessin aikana.

### <a name="ended"></a>Päättynyt

Kun karanteenitilaus on päättynyt, nimike siirretään karanteenivarastosta takaisin tavalliseen varastoon. Nimiketapahtuman tilaksi asetetaan karanteenivarastossa **Myyty** ja tavallisessa varastossa **Ostettu**.

## <a name="quarantine-order-scrap"></a>Karanteenitilausten hävikki
Karanteenitilausprosessin aikana varastoa voidaan määrittää hävikiksi. Hävikkiä käsiteltäessä varaston tilaksi asetetaan **Myyty** ottotapahtumalla karanteenivarastosta.

<a name="see-also"></a>Lisätietoja
--------

[Inventory blocking](inventory-blocking.md)


