---
title: Ylläpidon tarkistuslistat
description: Tässä artikkelissa kuvataan ylläpidon tarkistuslistoja resurssien hallinnassa.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderChecklist, EntAssetMobileWorkOrderLineChecklistDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 70b83de50105cf664bbc6b6095203d01d83cd79b
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016678"
---
# <a name="maintenance-checklists"></a>Ylläpidon tarkistuslistat

[!include [banner](../../includes/banner.md)]



Ylläpidon tarkistusluettelot määritetään ylläpitotöiden tyypeille. Ylläpidon tarkistuslistojen täyttäminen on osa työtilauksen täyttämisprosessia. Lisätietoja ylläpitotyötyyppejä koskevien ylläpidon tarkistuslistojen määrittämisestä **Ylläpitotöiden tyyppien oletukset** -sivulla esitetään kohdassa [Ylläpitotöiden tyyppiluokat ja ylläpitotöiden tyypit, ylläpitotöiden tyyppien variantit, ylläpitotöiden toimialat ja ylläpidon tarkistuslistat](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

Kun käsittelet ylläpidon tarkistuslistoja työtilauksessa, voit täyttää valmiiksi määritetyt ylläpidon tarkistuslistat, jotka liittyvät ylläpitotyötyyppeihin. Voit myös lisätä lisää ylläpidon tarkistuslistoja


## <a name="fill-in-a-maintenance-checklist"></a>Ylläpidon tarkistuslistan täyttäminen

1. Valitse **Resurssien hallinta** > **Työtilaukset** > **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.

2. Valitse työtilaus luettelosta ja sitten toimintoruudun **Työtilaus**-välilehden **Rivit**-ryhmässä **Ylläpidon tarkistuslista**.

3. **Työtilauksen ylläpitotöiden tarkistuslista** -kohdassa näkyvät kaikkien työtilaustehtävien ylläpidon tarkistusluettelot. Jos työtilaustehtävillä on erilaiset ylläpitotyölajit, ylläpidon tarkistuslistat voivat olla erilaiset jokaisessa työtilaustehtävässä Valitse työtilaustyö, jota käytetään liittyvän huollon tarkistusluettelon kanssa. Valitun ylläpidon tarkistusluettelorivin tiedot näkyvät **Rivin tiedot** -pikavälilehdessä.

4. Täytä kaikki ylläpidon tarkistusluettelon rivit yksi kerrallaan siinä järjestyksessä, jossa ne näkyvät. Täytät ylläpidon tarkistusluettelorivin täyttämällä **Rivin tiedot** -pikavälilehden kentät. Rivin täyttämiseen tarvittavat tiedot voivat vaihdella rivityypin mukaan. Esimerkiksi **Teksti**-tyypin riville lisäät huomautuksen, joka selittää tarkistuksen tuloksen. **Mittaus**-tyypin riville syötät laitteesta luetun laskurin arvon ja voit lisätä tarpeen mukaan myös huomautuksen. Ylläpidon tarkistuslistan riviä, jonka tyyppi on **Otsikko**, käytetään sen alla olevien ylläpidon tarkistusluettelorivien ryhmittelemiseen. Sinun ei tarvitse antaa otsikkoa. Muissa ylläpidon tarkistuslistan tyypeissä lisätään huomautus **Otsikko**-tyypin riville.

5. Jos ohjeet liittyvät huollon tarkistusluetteloriviin, **Ohjeet**-valintaruutu valitaan. Lue valitun ylläpidon tarkistusluettelorivin ohjeet **Rivin tiedot** -pikavälilehden **Ohjeet**-kentästä.

6. Kun olet täyttänyt ylläpidon tarkistusluettelorivin, merkitse se valmiiksi valitsemalla rivillä oleva **Tarkistettu**-valintaruutu. Jos haluat hylätä ylläpidon tarkistusluettelorivin, koska se ei ole oleellinen työtilauksen työn kannalta, valitse rivin **Ei saatavilla** -valintaruutu. Jos ylläpidon tarkistusluettelorivillä **Tarkistus**-valintaruutu on valittuna, sinun on valittava joko **Valittu**-valintaruutu tai **Ei saatavilla** -valintaruutu.

>[!NOTE]
>Kunnossapitoluettelon rekisteröintejä voi päivittää vain, jos työtilaus on [aktiivisessa](../setup-for-work-orders/work-order-lifecycle-states.md) elinkaaritilassa.  


## <a name="add-a-maintenance-checklist-line"></a>Huollon tarkistusluettelorivin lisääminen

Ylläpidon tarkistusluettelot luodaan ylläpitotyön tyypin määrityksestä oletusarvon mukaan ja siirretään työtilaustehtävään. Tarvittaessa voit lisätä ylläpidon tarkistusluettelorivejä työtilaustehtävään. Manuaalisesti lisätyt ylläpidon tarkistusluettelorivit saavat viitteen **Manuaalinen**.

1. Valitse **Työtilauksen ylläpitotöiden tarkistuslista** -sivulla työtilaustehtävä, jolle haluat lisätä ylläpidon tarkistusluettelon.

2. Valitse ylläpidon tarkistusluettelorivi **Ylläpidon tarkistusluettelorivit** -pikavälilehdessä. Lisää sitten uusi rivi valitun rivin alle painamalla **Alanuoli**-näppäintä. **Rivinumero**-kenttään täytetään automaattisesti järjestyksessä seuraava numero. Valitsemalla **Lisää rivi** voit lisätä uuden rivin ennen valittua riviä. 

3. Kirjoita **Nimi**-kenttään ylläpidon tarkistuslistarivin nimi.

4. Kirjoita **tyyppi**-kenttään ylläpiton tarkistuslistan rivin tyyppi. **Rivin tiedot** -pikavälilehti sisältää kuhunkin ylläpidon tarkistusluettelotyyppiin liittyviä kenttiä.
    - **Teksti** – Tällä tyypillä voit lisätä ylläpidon tarkistusluettelorivin, jossa kuvataan tekstillä, mitä on tehtävä. Voit käyttää tätä tyyppiä esimerkiksi, jos työntekijä haluaa tarkistaa jotain, mutta et odota tiettyä (mitattavaa) tulosta. Kun olet valinnut tämän tyypin, kirjoita **Rivin tiedot**-pikavälilehden **Ohjeet**-kenttään teksti siitä, mitä on tehtävä.
    - **Otsikko** – Tämän tyypin ylläpidon tarkistusluetteloa käytetään sen alla olevien ylläpidon tarkistusluettelorivien ryhmittelemiseen. Tästä tyypistä on hyötyä, jos sinulla on useita huollon tarkistusluettelon rivejä, jotka voidaan jakaa tiettyihin alueisiin. Kun olet valinnut tämän tyypin, kirjoita kuvaava nimi **Nimi** -kenttään.
    - **Malli** – Tämä tyyppi ei ole käytettävissä, kun ylläpidon tarkistusluettelorivi lisätään työtilaustehtävään manuaalisesti.  
    - **Muuttuja** – Tämän tyypin avulla määritetään mahdollinen tulos ylläpidon tarkistusluettelorivin arvoalueella. Lisätietoja ylläpidon tarkistuslistojen muuttujien määrittämisestä annetaan kohdassa [Ylläpitotöiden tyyppiluokat ja ylläpitotöiden tyypit, ylläpitotöiden tyyppien variantit, ylläpitotöiden toimialat ja ylläpidon tarkistuslistat](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md). Kun olet valinnut tämän tyypin, kirjoita muuttujaa kuvaava nimi **Nimi** -kenttään. Valitse muuttuja **Rivitiedot**-pikavälilehden **Muuttuja**-kentässä. Kirjoita **Ohjeet** -kenttään kuvaus siitä, mitä on tehtävä.
    - **Mittaus** – Tätä tyyppiä käytetään tietyn mittaustuloksen tallentamiseen ylläpidon tarkistusluetteloriville. Kun olet valinnut tämän tyypin, kirjoita mallin nimi **Nimi**-kenttään. Valitse asianmukaiset arvot **Rivitiedot**-pikavälilehden kentissä **Laskuri** ja **Yksikkö**. Kirjoita **Ohjeet** -kenttään kuvaus siitä, mitä on tehtävä.

5. Kun olet lisännyt manuaalisesti halulamasi ylläpidon tarkistusluettelorivit, täytä rivit edellä osassa **Ylläpidon tarkistuslistan täyttäminen** kuvatulla tavalla.

>[!NOTE]
>**Työtilauksen ylläpitotöiden tarkistuslista** -sivulla ei voi poistaa ylläpidon tarkistusluettelorivejä, joilla on viite **Työtyyppi**. Voit poistaa vain ylläpidon tarkistusluettelorivejä, jotka sinä tai muu ylläpitotyöntekijä on luonut manuaalisesti ja joilla on viite **Manuaalinen**.

Alla olevassa kuvassa näkyy esimerkki ylläpidon tarkistuslistasta.

![Kuva 1.](media/14-work-orders.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]