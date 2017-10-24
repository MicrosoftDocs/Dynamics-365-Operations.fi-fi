---
title: "Vähittäismyyntikanavien määrittäminen ja ylläpitäminen"
description: "Tämä artikkeli sisältää perinteisten myymälöiden määrittämisprosessin yleiskatsauksen. Perinteisiä myymälöitä kutsutaan Microsoft Dynamics 365 for Retailissa vähittäismyymälöiksi. Artikkeli sisältää myös tietoja tehtävistä, jotka on suoritettava ennen vähittäismyymälän määrittämistä ja sen jälkeen."
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 700b8868a68be7f0172202d737b4f1ae9813ecf3
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="define-and-maintain-retail-channels"></a>Vähittäismyyntikanavien määrittäminen ja ylläpitäminen

[!include[banner](includes/banner.md)]


Tämä artikkeli sisältää perinteisten myymälöiden määrittämisprosessin yleiskatsauksen. Perinteisiä myymälöitä kutsutaan Microsoft Dynamics 365 for Retailissa vähittäismyymälöiksi. Artikkeli sisältää myös tietoja tehtävistä, jotka on suoritettava ennen vähittäismyymälän määrittämistä ja sen jälkeen.

Dynamics 365 for Retail tukee useita vähittäismyynnin kanavia, kuten verkkokauppoja, puhelinkeskuksia ja perinteisiä myymälöitä. Perinteistä myymälöitä kutsutaan vähittäismyymäläksi. Jokaisella vähittäismyymälällä voi olla omat maksuvälineet, hintaryhmät, kassakoneet, tulo- ja kulutilit sekä oma henkilökunta. Vähittäismyymälälle on määritettävä kaikki edellä luetellut elementit, ennen kuin se voidaan luoda. Kun olet luonut vähittäismyymälän, voit määrittää myymälän tuotteet. Voit myös liittää työntekijät, kassapäätteet ja asiakkaat myymälään. Lopuksi lisäät uuden myymälän organisaatiohierarkiaan.

## <a name="setting-up-retail-stores"></a>Vähittäismyynnin varastojen määrittäminen
Ennen kuin voit määrittää Dynamics 365 for Retailin vähittäismyymälän, edellytetyt tehtävät on tehtävä ensin. Tämän jälkeen voit luoda vähittäismyymälän ja lisätä tiedot.

### <a name="prerequisites"></a>Edellytykset

Ennen kuin voit määrittää vähittäismyymälän, sinun on suoritettava seuraavat tehtävät:

1.  Määritä organisaatiorakenne ja organisaation hierarkiat vähittäismyynnin valikoimille, täydennyksille ja raportointia varten.
2.  Määritä varasto, joka vastaa vähittäismyyntiliikettä.
3.  Vähittäismyynnin myymälöiden numerosarjojen, myymälän laskelmien ja laskelman tositteiden määrittäminen.
4.  Määritä Retail-parametrit.
5.  Määritä maksutapoja, jotka myymälä hyväksyy.
6.  Voit myös määrittää maksupalvelut prosessoimaan luottokorttitapahtumat Retail POS -kassakoneissa.
7.  Määritä arvonlisäveroryhmät.
8.  Aseta vähittäismyyntituotteet. Tässä tehtävässä määritetään myös vähittäismyyntituotteiden hierarkiat, tuotevariantit ja tuotevalikoimat.
9.  Voit määrittää tuotehintaryhmät.
10. Määritä vähittäismyynnin tuotteiden hinnoittelu. Tässä tehtävässä määritetään myös hinnanoikaisut, alennukset ja alennuskaudet.
11. Henkilökunnan jäsenten määrittäminen. **Huomautus:** Määritä myös työntekijöille soveltuvat käyttöoikeudet, joiden avulla he voivat kirjautua Dynamics 365 for Retailin Retail POS -järjestelmään ja suorittaa siellä tehtäviä.
12. Määritä myymälään liitettävät Retail POS -profiilit. Tämä tehtävä sisältää useita tehtäviä, kuten kassapäätteiden määrittäminen, offline profiilien määrittäminen ja kuitin muodon ja profiilien määrittäminen.

Tarkastele kaikkia näihin edellytyksiin sisältyviä tehtäviä ja suorita vain tehtävät, jotka koskevat sinua.

### <a name="set-up-a-retail-store"></a>Aseta vähittäismyyntiliike

Kun olet tehnyt edellytettävät toimet, määritä vähittäismyymälän tiedot suorittamalla nämä tehtävät:

1.  Luo vähittäismyymälä.
2.  Määritä arvonlisäveroryhmä myymälälle.
3.  Määritä hyväksytyt maksutavat myymälälle.
4.  Lisää tietoja niiden tuotteiden tuotekuvauksiin, joita myyt myymälöissäsi. Voit esimerkiksi lisätä rtf-tekstiä ja kuvia. Nämä tuotetiedot näkyvät useissa paikoissa, kuten myyntipisteen kassakoneella ja tulostetuissa etiketeissä.
5.  Lisää myymälä oletusorganisaatiohierarkiaan, joka on liitetty **vähittäismyyntivalikoimaan**, **vähittäismyynnin täydennykseen** tai **vähittäismyynnin raportointiin**.

### <a name="after-you-set-up-a-retail-store"></a>Kun olet määrittänyt myymälän

Kun olet lisännyt vähittäismyymälälle tietoja, päätä tehtävät lähettämällä uudet vähittäismyymälän tiedot Retail POS -sovellukseen.

1.  Määritä myymälän myyntipisteiden kassakoneet.
2.  Määritä tuotevalikoimia myymälään.
3.  Käsittele valikoimat luodaksesi luettelo tuotteista, jotka sisältyvät valikoimaan ja tehdäksesi tuotteet saataviksi vähittäismyymälässä.
4.  Lähetä Retail POS -sovelluksen kassakoneille tietoja, kuten numerosarjat, laitteistojen laiteprofiilit ja myyntipisteen näytön asettelut.
5.  Julkaise vähittäismyymälä lähettääksesi myymälän tietoja Retail POS -sovellukseen.
6.  Suorita työt lähettääksesi myymälän Retail POS -sovellukseen.

## <a name="organization-hierarchies"></a>Organisaatiohierarkiat
Retail määrittää vähittäismyyntikanavien rakenteen organisaatiohierarkioiden avulla. Organisaatiohierarkiat edustavat liiketoimintasi muodostavien organisaatioiden välisiä suhteita. Kun perustat kauppoja, voit lisätä ne organisaatiohierarkiaan. Myymälät jakavat sitten valikoimissa, täydennyksissä ja raportoinnissa käytettävät tiedot.




