--- 
title: "Määritä mobiililaitteen valikkokohde vastaanotettujen nimikkeiden rekisteröinnille"
description: "Tässä tehtävässä käsitellään mobiililaitteen valikkovaihtoehdon määrittäminen."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 642e2b05c9f9a59f6b47a22f3d92f2f6ae245039
ms.contentlocale: fi-fi
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a>Määritä mobiililaitteen valikkokohde vastaanotettujen nimikkeiden rekisteröinnille

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä tehtävässä käsitellään mobiililaitteen valikkovaihtoehdon määrittäminen. Tällä valikkovaihtoehdolla rekisteröidään ostotilauksilla tilattujen nimikkeiden vastaanotto. 

Voit käyttää tätä opastusta USMF-yrityksen demotiedoissa. Tämä menettely on tarkoitettu varastopäällikölle.


## <a name="create-a-mobile-device-menu-item"></a>Luo mobiililaitteen valikkovaihtoehto
1. Valitse Varastonhallinta > Asetukset > Mobiililaite > Mobiililaitteen valikkovaihtoehdot.
2. Valitse Uusi.
3. Kirjoita arvo Valikkovaihtoehdon nimi -kenttään.
    * Tämä on mobiililaitteen valikkovaihtoehdon yksilöllinen tunnus. Voit esimerkiksi kirjoittaa Oma ostotilausrekisteröinti.  
4. Kirjoita Otsikko-kenttään arvo.
    * Tämä on otsikko, jonka käyttäjä näkee mobiililaitteessa. Voit esimerkiksi kirjoittaa Ostotilausrekisteröinti.  
5. Valitse Tila-kentässä Työ.
    * Ostotilausriville vastaanotettujen käytettävissä olevien määrien rekisteröinti luo työn nimikkeiden siirtämisestä vastaanotosta varastoon. Työtä ei luoda, ennen kuin nimikkeet on rekisteröity.  Tämän vuoksi Käytä nykyistä työtä -asetukseksi jätetään Ei.  
6. Laajenna tai tiivistä Yleiset-osa.
7. Valitse Työn luontiprosessi -kentässä Ostotilausnimikkeen vastaanotto.
    * Ostotilausrivillä on oltava yksilöllinen tunniste, ennen kuin käytettävissä oleva varasto voidaan rekisteröidä varastossa. Tässä skenaariossa mobiililaite rekisteröi ostotilausnumeron ja nimiketunnuksen, minkä ansiosta järjestelmä tunnistaa ostotilausrivin. Poispanotyö luodaan ja toinen työntekijä voi kerätä sen.    Valittu työn luontimenetelmä määrittää, mitä kenttiä Yleiset-välilehdessä on.  
    * Jos valitset Käytä oletustietoja -asetuksen Oletustiedot-painike on käytettävissä. Voit valita tässä näytettäviksi tiedot, joita työntekijän yleensä tarvitsee päivittäisessä työssään. Nämä arvot näkyvät mobiililaitteessa.  
    * Rekisterikilpiryhmitys-parametria käytetään yhdessä sen yksikön sarjaryhmän kanssa, joka on määritetty vastaanotettavalla nimikkeelle. Voit määrittää, ryhmitelläänkö yhtä kuormalavaa pienemmät tai suuremmat yhteen rekisterikilpeen vai jaetaanko jokainen yksikkö erilliselle rekisterikilvelle.  
    * Jos valitset Muodosta rekisterikilpi -vaihtoehdon, yksilöllinen rekisterinumero luodaan numerosarjavalinnan perusteella.   
    * Voit valita mallin, jota käytetään, kun työ on luotu. Jos esimerkiksi jos rekisteröit ostotilauksen nimikkeen, poispanotyö luodaan työmallin perusteella. Jos et valitse työmallia tässä, järjestelmä määrittää mallin malleihin liitettyjen kyselyehtojen perusteella.  
    * Jos käsittelykoodit näytetään mobiililaitteessa, työntekijät voivat arvioida nimikkeiden tilan tai määrän ja valita sopivan koodin. Käsittelykoodin säännöt määrittävät, ovatko nimikkeet muiden varastoprosessien käytettävissä. Säännöt määrittävät myös, mitä sijaintidirektiiviä luoduille töille käytetään.   
    * Jos valitset Erän käsittelykoodit -vaihtoehdon, työntekijät voivat arvioida erän tilan tai määrän ja valita sopivan käsittelykoodin.  Erälle määritetyt käsittelykoodin säännöt määrittävät, onko erä muiden varastoprosessien käytettävissä.  
    * Jos valitset Tulosta etiketit -vaihtoehdon, rekisterikilpietiketti tulostetaan automaattisesti, kun nimikkeet vastaanotetaan.  
8. Valitse Tallenna.
9. Sulje sivu.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Lisää valikkovaihtoehto mobiililaitteen valikkoon
1. Valitse Varastonhallinta > Asetukset > Mobiililaite > Mobiililaitteen valikko.
2. Voit suodattaa pikasuodattimella Nimi-kenttää arvolla saapuva.
3. Valitse Muokkaa.
4. Valitse puussa Valitse käytettävissä olevasta valikosta nimikepuuta aiemmin luotu valikkovaihtoehto.
    * Valitse aiemmin luomasi valikkovaihtoehto.  
5. Napsauttamalla oikealle osoittavaa työtä.
6. Valitse Tallenna.
7. Sulje sivu.


