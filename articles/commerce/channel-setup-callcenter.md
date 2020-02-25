---
title: Puhelinkeskuskanavan määrittäminen
description: Tässä ohjeaiheessa käsitellään uuden puhelinkeskuskanavan luontia Microsoft Dynamics 365 Commercessa.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6ec42ab920868f541eeac54556f4f24cb1efaa3a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002447"
---
# <a name="set-up-a-call-center-channel"></a>Puhelinkeskuskanavan määrittäminen


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään uuden puhelinkeskuskanavan luontia Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskatsaus

Dynamics 365 Commerceissa puhelinpalvelukeskus on vähittäismyyntityyppinen kanava, joka voidaan määrittää sovelluksessa. Kun puhelinkeskusentiteeteille määritetään kanava, järjestelmä voi sitoa tietyt tiedot ja tilausten käsittelyn oletukset myyntitilauksiin. Yritys voi määrittää useita puhelinkeskuskanavia Commercessa. 

Varmista, ennen uuden puhelinkeskuskanavan luontia, että [kanava-asetusten edellytykset](channels-prerequisites.md) toteutuvat.

## <a name="create-and-configure-a-new-call-center-channel"></a>Uuden puhelinkeskuskanavan luominen ja määrittäminen

Voit luoda ja määrittää uuden puhelinkeskuskanavan seuraavasti.

1. Valitse siirtymisruudussa **Moduulit \> Kanavat \> Puhelinkeskukset \> Kaikki puhelinkeskukset**.
1. Valitse toimintoruudussa **Uusi**.
1. Kirjoita **Nimi**-kenttään uuden kanavan nimi.
1. Valitse avattavasta luettelosta sopiva **Yritys**.
1. Valitse avattavasta luettelosta sopiva **Varasto**-sijainti.
1. Anna kelvollinen oletusasiakas **Oletusasiakas**-kentässä.
1. Anna kelvollinen sähköpostin ilmoitusprofiili **Sähköposti-ilmoitusprofiili**-kentässä.
1. Anna **Hinnan ohitus** -tietokoodi. Huomaa, että tämä tietokoodi on luotava ensin.
1. Anna **Pitokoodi**-tietokoodi. Huomaa, että tämä tietokoodi on luotava ensin.
1. Anna **Luotto**-tietokoodi. Huomaa, että tämä tietokoodi on luotava ensin.
1. Valitse **Tallenna**.

Seuraavassa kuvassa näytetään, miten uusi puhelinkeskuskanava luodaan.

![Uusi puhelinkeskuskanava](media/channel-setup-callcenter-1.png)

Seuraavassa kuvassa on esimerkki puhelinkeskuskanavasta.

![Esimerkki puhelinkeskuskanavasta](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>Lisäkanavan määrittäminen

Puhelinkeskuskanavan asetuksia varten tarvittavia tehtäviä, kuten maksutapojen ja toimitustapojen määrittäminen.

Seuraavassa kuvassa on **Asetukset**-välilehden **Toimitustavat**- ja **Maksutavat**-asetusvaihtoehdot.

![Puhelinkeskuskanavan lisämääritykset](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a>Maksutapojen määrittäminen

Voit määrittää maksutavan kullekin tässä kanavassa tuetulle maksutyypille seuraavien ohjeiden mukaisesti.

1. Valitse toimintoruudussa ensin **Asetukset**-välilehti ja sitten **Maksutavat**.
1. Valitse toimintoruudussa **Uusi**.
1. Valitse maksutapa siirtymisruudussa.
1. Anna **Yleiset**-osassa **Toiminnon nimi** ja määritä muut mahdolliset asetukset.
1. Määritä tarvittaessa maksutyypin mahdolliset lisäasetukset.
1. Valitse toimintoruudussa **Tallenna**.

Seuraavassa kuvassa näkyy esimerkki käteismaksutavasta.

![Esimerkki maksutavasta](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>Määritä toimitustavat

Määritetyt toimitustavat saadaan näkyviin valitsemalla **Toimitustapa** **toimintoruudun** **Asetukset**-välilehdessä.  

Voit muuttaa toimitustapaa tai lisätä sen seuraavien ohjeiden mukaisesti.

1. Valitse siirtymisruudussa **Moduulit \> Varastonhallinta \> Toimitustavat**.
1. Luo uusi toimitustapa valitsemalla toimintoruudussa **Uusi** tai valitse aiemmin luotu tapa.
1. Lisää kanava valitsemalla **Vähittäismyyntikanava**-osassa **Lisää rivi**. Kanavien lisäämistä voi yksinkertaistaa käyttämällä organisaatiosolmua sen sijaan, että kukin kanava lisättäisiin erikseen.

Seuraavassa kuvassa on esimerkki toimitustavasta.

![Määritä toimitustavat](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a>Lisäresurssit

[Kanava-asetusten edellytykset](channels-prerequisites.md)

[Puhelupalvelukeskuksen myyntitoiminnot](call-center-functionality.md)

[Puhelinkeskuksen tilaustenkäsittelyasetusten määrittäminen](set-up-order-processing-options.md)

[Puhelinpalvelukeskuksen luettelot](call-center-catalogs.md)

[Petoshälytysten määrittäminen ja käyttäminen](set-up-fraud-alerts.md)

[Jatkuvuusohjelmien määrittäminen puhelinkeskuksille](set-up-continuity-program.md)
