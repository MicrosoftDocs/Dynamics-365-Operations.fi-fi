---
title: Toiminnallisen sijainnin elinkaaren tilat
description: Tässä ohjeaiheessa kuvataan, miten toiminnalliset sijaintitilat ja elinkaarimallit määritetään resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationLifecycleModel, EntAssetFunctionalLocationLifecycleState
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3eedc21dde32671b4f5539ac4e798a8e1329c191
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427372"
---
# <a name="functional-location-lifecycle-states"></a>Toiminnallisen sijainnin elinkaaren tilat

[!include [banner](../../includes/banner.md)]

 

Tässä ohjeaiheessa kuvataan, miten toiminnallisten sijaintien elinkaaritilat ja elinkaarimallit määritetään resurssien hallinnassa. Toiminnallisen sijainnin elinkaaritilat määrittävät tilat, jotka toiminnallinen sijainti voi käydä läpi, esimerkiksi, Luotu, Aktiivinen ja Päättynyt. **Kaikki toiminnalliset sijainnit**- luettelosivulla voit tarkastella kaikkia toiminnallisia sijainteja riippumatta niiden elinkaaren tilasta. Voit muuttaa toiminnallisen sijainnin tilaa valitsemalla sen **Kaikki toiminnalliset sijainnit** -luettelosivulla ja valitsemalla **Päivitä toiminnallisen sijainnin tila.**

## <a name="set-up-functional-location-lifecycle-states"></a>Toiminnallisen sijainnin elinkaaren tilojen määrittäminen

1. Valitse **rRsurssien hallinta** > **Asetukset** > **Toiminnalliset sijainnit** > **Elinkaaren tilat**.
2. Luo uusi toiminnallisen sijainnin tila valitsemalla **Uusi**.
3. Lisää tilan tunnus tunnus **Elinkaaren tila**-kenttään ja toiminnallisen sijainnin tilan nimi **Nimi**-kenttään. **Elinkaarimallit**-kentässä on toiminnallisen sijainnin elinkaarimallien määrä, jotka käyttävät toiminnallisen sijainnin tilaa.
4. Valitse **Yleiset** -pikavälilehden **Aktiivinen**-vaihtopainikkeessa Kyllä, jos toiminnallinen sijainti on aktiivinen tässä tilassa.
5. Valitse Kyllä **Luo resurssit** -vaihtopainikkeessa, jos haluat luoda automaattisesti resurssin, jolla on sama nimi kuin toiminnallisella sijainnilla, ja asentaa sen toiminnalliseen sijaintiin, joka on tässä tilassa.  
>[!NOTE]
>Tämä vaihto painike liittyy **resurssityyppi**-kenttään **Yleiset**-pikavälilehdessä **toiminnallisen sijainnin tyypit** -lomakkeella (**resurssien hallinta** > **Asetukset** > **Toiminnalliset sijainnit** > **Toiminnalliset sijaintityypit**).
6. Valitse Kyllä **Nimeä sijainti uudelleen**-vaihtopainikkeessa, jos tämän tilan toiminnallisen sijainnin nimeä pitäisi olla mahdollista muuttaa.
7. Valitse Kyllä **Uudet alisijainnit**-vaihtopainikkeessa, jos tämän tilan toiminnalliseen sijaintiin pitäisi olla mahdollista lisätä uusia alisijainteja.
8. Valitse Kyllä **Resurssien asentaminen**-vaihtopainikkeessa, jos tämän tilan toiminnallisessa sijainnissa pitäisi olla mahdollista asentaa resursseja.
9. Valitse Kyllä **Poista toiminnallinen sijainti**-vaihtopainikkeessa, jos tämän tilan toiminnallinen sijainti pitäisi olla mahdollista poistaa.
10. Valitse resurssin tila **Elinkaaren tila** -kentässä, jos haluat, että kaikkien toiminnalliseen sijaintiin asennettujen resurssien elinkaaren tila päivitetään automaattisesti tässä tilassa. Esimerkki: Jos suljet toiminnallisen sijainnin ja määrität toiminnallisen sijainnin elinkaaren tilan arvoksi Päättynyt, haluat ehkä muuttaa kyseiseen toiminnalliseen sijaintiin asennettujen resurssien elinkaaren tilaksi automaattisesti Ei käytössä.


>[!NOTE]
>Toiminnallisen sijainnin elinkaaren tilat, elinkaarimallit ja tyypit liittyvät toisiinsa ja niitä käytetään samalla tavalla kuin työtilauksen elinkaaritiloja, työtilauksen elinkaarimalleja ja Työtilauksen tyyppejä. 

## <a name="set-up-functional-location-lifecycle-models"></a>Toiminnallisen sijainnin elinkaarimallien määrittäminen

Kun olet luonut toiminnallisten sijaintien edellyttämät elinkaariilat, ne voidaan jakaa ryhmiin. Tämä tehdään, kun luodaan elinkaarimallin virtaus, jota voidaan käyttää erityyppisissä toiminnallisissä sijainneissa. Vähintään yksi toiminnallisen sijainnin vakioelinkaarimalli on luotava.

1. Valitse **Resurssien hallinta** > **Asetukset** > **Toiminnalliset sijainnit** > **Elinkaarimallit**.
2. Luo uusi elinkaarimalli valitsemalla **Uusi**.
3. Lisää elinkaarimallin tunnus **Elinkaarimalli**-kenttään ja elinkaarimallin nimi **Nimi**-kenttään. **Toiminnalliset sijaintityypit**- ja **Elinkaaren tilat** -kentissä voi nähdä niiden toiminnallisten sijainti tyyppien määrän, jotka käyttävät elinkaarimallia ja elinkaarimalliin valittujen tilojen määrän.
4. Valitse **Elinkaaren tilat** -pikavälilehdessä ne tilat, jotka sisällytetään malliin. Tämä tehdään napsauttamalla tilaa **Jäljellä olevat elinkaaren tilat** -osassa ja napsauttamalla ![eteenpäin osoittavaa nuolta](media/02-setup-for-functional-locations.png) -painiketta.
5. Jos haluat valita mallin kaikki käytettävissä olevat tilat, napsauta ![Valitse kaikki käytettävissä olevat vaiheet](media/03-setup-for-functional-locations.png) -painiketta. Kaikki tilat siirretään **Valitut elinkaaren tilat** -osioon.
6. Jos haluat poistaa valitun tilan mallista, valitse tila **Valitut elinkaaren tilat** -osassaja valitse sitten ![takaisin-nuoli](media/04-setup-for-functional-locations.png) -painike.
7. Valitse **Elinkaaren tilan päivitykset** määrittääksesi, mitkä elinkaaren tilat voivat seurata valittua tilaa.
