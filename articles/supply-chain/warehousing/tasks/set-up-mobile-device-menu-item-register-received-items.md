---
title: Määritä mobiililaitteen valikkokohde vastaanotettujen nimikkeiden rekisteröinnille
description: Tässä aiheessa käsitellään mobiililaitteen valikkovaihtoehdon määrittäminen.
author: ShylaThompson
manager: tfehr
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFMenu, WHSRFDefaultData
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6f9cf258a991b88faa0d2db90cd3c21f9703267
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976960"
---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a>Määritä mobiililaitteen valikkokohde vastaanotettujen nimikkeiden rekisteröinnille

[!include [banner](../../includes/banner.md)]

Tässä aiheessa käsitellään mobiililaitteen valikkovaihtoehdon määrittäminen. Tällä valikkovaihtoehdolla rekisteröidään ostotilauksilla tilattujen nimikkeiden vastaanotto. 

Voit käyttää tätä opastusta USMF-yrityksen demotiedoissa. Tämä menettely on tarkoitettu varastopäällikölle.


## <a name="create-a-mobile-device-menu-item"></a>Luo mobiililaitteen valikkovaihtoehto
1. Siirry siirtymisruudussa kohtaan **Moduulit > Varastonhallinta > Asetukset > mobiililaite > Mobiililaitteen valikkovaihtoehdot**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Valikkovaihtoehdon nimi** -kenttään. Tämä on mobiililaitteen valikkovaihtoehdon yksilöllinen tunnus. Voit esimerkiksi kirjoittaa `My PO registration`.  
4. Kirjoita **Otsikko**-kenttään arvo. Tämä on otsikko, jonka käyttäjä näkee mobiililaitteessa. Voit esimerkiksi kirjoittaa `PO registration`.  
5. Valitse **Tila**-kentässä **Työ**. Ostotilausriville vastaanotettujen käytettävissä olevien määrien rekisteröinti luo työn nimikkeiden siirtämisestä vastaanotosta varastoon. Työtä ei luoda, ennen kuin nimikkeet on rekisteröity. Tämän vuoksi **Käytä nykyistä työtä** -asetukseksi jätetään **Ei**.
6. Valitse **Yleiset**-osan **Työn luontiprosessi** -kentässä **Ostotilausnimikkeen vastaanotto**.
    - Ostotilausrivillä on oltava yksilöllinen tunniste, ennen kuin käytettävissä oleva varasto voidaan rekisteröidä varastossa. Tässä skenaariossa mobiililaite rekisteröi ostotilausnumeron ja nimiketunnuksen, minkä ansiosta järjestelmä tunnistaa ostotilausrivin. Poispanotyö luodaan ja toinen työntekijä voi kerätä sen. Valittu työn luontimenetelmä määrittää, mitä kenttiä **Yleiset**-pikavälilehdessä on.  
    - Jos valitset **Käytä oletustietoja** -vaihtoehdon, **Oletustiedot**-painike otetaan käyttöön. Voit valita tässä näytettäviksi tiedot, joita työntekijän yleensä tarvitsee päivittäisessä työssään. Nämä arvot näkyvät mobiililaitteessa.  
    - **Rekisterikilpiryhmitys**-parametria käytetään yhdessä sen yksikön sarjaryhmän kanssa, joka on määritetty vastaanotettavalle nimikkeelle. Voit määrittää, ryhmitelläänkö yhtä kuormalavaa pienemmät tai suuremmat yhteen rekisterikilpeen vai jaetaanko jokainen yksikkö erilliselle rekisterikilvelle.  
    - Jos valitset **Muodosta rekisterikilpi** -vaihtoehdon, yksilöllinen rekisterinumero luodaan numerosarjavalinnan perusteella.  
    - Voit valita mallin, jota käytetään, kun työ on luotu. Jos esimerkiksi jos rekisteröit ostotilauksen nimikkeen, poispanotyö luodaan työmallin perusteella. Jos et valitse työmallia tässä, järjestelmä määrittää mallin malleihin liitettyjen kyselyehtojen perusteella.  
    - Jos käsittelykoodit näytetään mobiililaitteessa, työntekijät voivat arvioida nimikkeiden tilan tai määrän ja valita sopivan koodin. Käsittelykoodin säännöt määrittävät, ovatko nimikkeet muiden varastoprosessien käytettävissä. Säännöt määrittävät myös, mitä sijaintidirektiiviä luoduille töille käytetään.   
    - Jos valitset **Erän käsittelykoodit** -vaihtoehdon, työntekijät voivat arvioida erän tilan tai määrän ja valita sopivan käsittelykoodin. Erälle määritetyt käsittelykoodin säännöt määrittävät, onko erä muiden varastoprosessien käytettävissä.  
    - Jos valitset **Tulosta etiketit** -vaihtoehdon, rekisterikilpietiketti tulostetaan automaattisesti, kun nimikkeet vastaanotetaan.  
7. Valitse **Tallenna**.
8. Sulje sivu.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Lisää valikkovaihtoehto mobiililaitteen valikkoon
1. Siirry siirtymisruudussa kohtaan **Moduulit > Varastonhallinta > Asetukset > mobiililaite > Mobiililaitteen valikko**.
2. **Pikasuodattimen** avulla voit suodattaa **Nimi**-kentän arvon `inbound` mukaan.
3. Valitse **Muokkaa**.
4. Valitse Käytettävissä olevat valikot ja nimikkeet -puussa aiemmin luotu valikkovaihtoehto.
5. Valitse oikealle osoittava nuoli.
6. Valitse **Tallenna**.
7. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]