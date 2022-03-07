---
title: Tapahtuman keskeyttäminen ja jatkaminen myyntipisteessä
description: Tässä ohjeaiheessa kerrotaan, miten käyttäjä voi keskeyttää meneillään olevat tapahtumat ja jatkaa niitä sitten myöhemmin tai toisessa kassakoneessa Dynamics 365 Commercessa.
author: jblucher
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2efc88cfa7a8cede50969484d275c6fdbb2204dd2f29b3f8c7340d02cb61a79c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737551"
---
# <a name="suspend-and-resume-a-transaction-in-the-point-of-sale-pos"></a>Tapahtuman keskeyttäminen ja jatkaminen myyntipisteessä

[!include [banner](includes/banner.md)]


Myyntipisteen käyttäjät voivat keskeyttää meneillään olevat tapahtumat ja jatkaa niitä sitten myöhemmin tai toisessa kassakoneessa. Tapahtumat keskeytetään usein sen vuoksi, että kassakoneella voi tehdä jonkin muun tehtävän. Jos näin tehdään, nykyinen tapahtuma jää keskeytyskohtaan odottamaan jatkamista. Vaikka myymälän myyjä voi esimerkiksi aloittaa asiakkaan tapahtuman käsittelyn mobiililaitteessa, hän tarvitsee sen viimeistelyyn kuitenkin kassakoneen. Myyjä voi tässä tapauksessa keskeyttää tapahtuman mobiililaitteessa ja jatkaa sitä sitten kassakoneessa.

## <a name="configure-suspend-and-resume-functionality"></a>Keskeytys- ja jatkamistoimintojen määrittäminen

### <a name="pos-operations"></a>POS-toiminnot

Kahden [myyntipistetoiminnon](pos-operations.md) ansiosta myyntipiste tukee keskeytys- ja jatkamisskenaarioita. Voit määrittää nämä toiminnot [painikeruudukkoihin](pos-screen-layouts.md) tapahtuma- tai aloitussivulla.

- 503: Keskeytä tapahtuma
- 504: Jatka tapahtumaa

### <a name="receipt-template"></a>Kuittimalli

Myyntipiste voidaan määrittää luomaan tulostettu luettelo, kun tapahtuma keskeytetään. Tapahtuma voidaan sitten myöhemmin tunnistaa ja uudelleenkutsua nopeasti tämän luettelon avulla.

Myyntipiste voi tulostaa luettelon, kun **Keskeytetty tapahtuma** -kuittimuoto on lisätty myymälän kuittiprofiiliin. Voit suunnitella kuitin muodon siten, että se joko sisältää tietyt tapahtumaa koskevat tiedot tai että ne jäävät pois. Muoto voi sisältää esimerkiksi lukemista tukevan viivakoodin.

### <a name="receipt-numbering"></a>Kuitin numerointi

Muiden tulostetun kuitin luovien myyntipisteen tapahtumatyyppien tavoin keskeytetyille tapahtumille voi määrittää numerosarjan myymälän toimintoprofiilin **Kuitin numerointi** -osassa.

### <a name="void-when-closing-shift"></a>Mitätöi, kun vuoro suljetaan

Voit edellyttää **Mitätöi, kun vuoro suljetaan** -asetuksen avulla, että käyttäjät joko viimeistelevät tai mitätöivät kaikki keskeytetyt toiminnot ennen vuoron sulkemista. Myyntipiste pyytää **Sulje vuoro** -toiminnon aikana, että käyttäjät joko tarkastelevat tai mitätöivät keskeneräiset keskeytetyt tapahtumat.

## <a name="suspend-and-resume-a-transaction"></a>Tapahtuman keskeyttäminen ja jatkaminen

### <a name="suspend-a-transaction"></a>Tapahtuman keskeyttäminen

Jos käyttäjällä on riittävät oikeudet ja jos hänen näyttöasetteluunsa sisältyy **Keskeytä tapahtuma** -toiminto, käyttäjä voi keskeyttää tapahtuman siten, että se voidaan kutsua myöhemmin uudelleen tai että sitä voidaan käyttää toisessa kassakoneessa.

Tapahtumat voidaan keskeyttää vain, jos niissä **ei** ole seuraavia rivityyppejä:

- Aktiiviset maksurivit
- Lahjakorttirivit (joko lahjakortin myöntämiseen tai lahjakorttisaldoon lisäämiseen)

Keskeytetty tapahtuma ei vaikuta myymälän myyntitietoihin tai käytettävissä olevan varaston tietoihin.

### <a name="resume-a-suspended-transaction"></a>Keskeytetyn tapahtuman jatkaminen

Kuka tahansa saman myymälän käyttäjä, jolla on riittävät oikeudet, voi kutsua keskeytetyt tapahtumat uudelleen ja jatkaa niitä. Lisäksi kyseisellä käyttäjällä on oltava näyttö. jossa on **Jatka tapahtumaa** -toiminto.

Keskeytettyä tapahtumaa voi jatkaa nopeasti ja kätevästi lukemalla viivakoodin tulostetussa luettelossa samalla, kun tarkastelet **Jatka tapahtumaa** -toiminnon tapahtumaluetteloa.

### <a name="considerations-for-offline-mode"></a>Offline-tilaa koskevia huomautuksia

- Jos tapahtuma on keskeytetty, kun myyntipiste on online-tilassa, sitä ei voi jatkaa offline-tilassa, sillä tietoja ei ole synkronoitu offline-tietokantaan.
- Jos keskeytät tapahtuman, kun myyntipiste on offline-tilassa, voit jatkaa sitä offline-tilassa, kunhan kyseinen myyntipiste ei ole siirtynyt missään vaiheessa takaisin online-tilaan tapahtuman keskeytyksen aikana. Kun myyntipiste siirtyy takaisin online-tilaan, keskeytettyjen tapahtumien tiedot siirretään online-tietokantaan ja poistetaan offline-tietokannasta. Tämän vuoksi tapahtumia voidaan jatkaa vain online-tilassa. Jos myyntipiste siirretään takaisin offline-tilaan, kyseisiä keskeytettyjä tapahtumia ei voi jatkaa, koska ne on jo poistettu offline-tietokannasta.

### <a name="void-a-suspended-transaction"></a>Keskeytetyn tapahtuman mitätöinti

Voit mitätöidä keskeytetyt tapahtumat joko jatkamalla tapahtumaa ja suorittamalla sitten **Mitätöi tapahtuma** -toiminnon tai valitsemalla tapahtuman **Jatka tapahtumaa** -luettelossa ja valitsemalla sitten sovelluspalkissa **Mitätön**. Myymälä voidaan määrittää myös pyytämään käyttäjät mitätöimään keskeytetyt tapahtumat vuoron sulkemisen yhteydessä.


[!INCLUDE[footer-include](../includes/footer-banner.md)]