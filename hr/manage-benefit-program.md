---
title: "Määritä ja hallitse ohjelman edut"
description: "Henkilöstöhallinto sisältää joukon työkaluja, joiden avulla organisaation tarjoamia tai työntekijöitä varten käsittelemiä etuja, vähennyksiä ja työntekijöiden kompensaatiosuunnitelmia voi määrittää ja ylläpitää. Tässä artikkelissa on tietoja etujen määrittämisestä ja hallinnasta."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 81b5c9056001b26c33b2b42a95711ff5b50243e6
ms.openlocfilehash: 9d00d8f6dfa075f53473af31c257deb57c9efa86
ms.lasthandoff: 03/31/2017


---

# <a name="define-and-manage-a-benefits-program"></a>Määritä ja hallitse ohjelman edut

Henkilöstöhallinto sisältää joukon työkaluja, joiden avulla organisaation tarjoamia tai työntekijöitä varten käsittelemiä etuja, vähennyksiä ja työntekijöiden kompensaatiosuunnitelmia voi määrittää ja ylläpitää. Tässä aiheessa on tietoja siitä, miten voit määrittää hallinta-etuudet.

<a name="benefit-setup"></a>Etujen asetukset
-------------

Työntekijät voidaan rekisteröidä etuihin sen jälkeen, kun kunkin edun elementit on luotu. Nämä elementit yhdistävät samanlaiset etusuunnitelmat ja määrittävät oletusasetukset, kuten vähennysten määrät ja kirjanpitotiedot. Useita asetuksia voidaan muokata myöhemmin, kun työntekijät rekisteröidään etuun. Organisaation etusuunnitelmassa voi olla useita rekisteröitymisasetuksia tai työntekijä voi peruuttaa suunnitelmaan rekisteröitymisen. 

[![Hyötyä prosessinkulku](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Edun elementit
Ennen etujen luomista ja työntekijöiden rekisteröimistä niihin määritetään edun muodostavat elementit, joita ovat tyyppi, suunnitelma ja asetukset.

-   **Tyyppi** – kokoelma tietynlaisia etuussuunnitelmia, kuten työterveys tai pysäköinti.
-   **Suunnitelma** – tietty etuus, jonka tarjoamisesta on tehty sopimus palveluntarjoajan kanssa.
-   **Asetus** – kattavuustaso, kuten vain työntekijöille tarkoitettu tai työntekijä ja puoliso/kumppani.

Organisaatio voi tarjota työntekijöille jokaista etutyyppiä, kuten näöntarkistusta tai hammashuoltoa, varten yhden tai useita suunnitelmia. Organisaatio voi tarjota kutakin suunnitelmaa varten useita asetuksia. Työntekijät voivat ostaa esimerkiksi henkivakuutuksen lisävakuutusturvan, joka on vuosipalkan suuruinen tai kaksi tai kolme kertaan sen suuruinen. Jokaisesta suunnitelman ja asetusten yhdistelmästä muodostuu etu, johon työntekijät voivat rekisteröityä. 

[![etu-pic](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>Oikeutus
Useat tekijät määrittävät työntekijän kelpoisuuden työnantajan tarjoamiin erilaisiin etutyyppeihin. Voit määrittää kelpoisuus, joka koskee kyseisen etuuden tyypin luodessasi hyötyä Microsoft Dynamics-365 operaatioille. 

Voit tehdä hyötyä käytettävissä kaikille työntekijöille. Esimerkiksi jotkin yritykset tarjoavat pysäköinti osumia kaikille työntekijöille kuin luontaisetu. Kun tämä etu luodaan, määritä kelpoisuuden arvoksi **Kaikki työntekijät ovat oikeutettuja**. 

Tukikelpoisuutta ei liity muita etuja, kuten garnishments ja ALV-maksut. Hera luoda tällaisia etuuksia, arvoksi määritetään tukikelpoisuuden **ohittaa tukikelpoisuuden prosessi**. 

Lopuksi etu tukikelpoisuutta voidaan säännön perusteella. Esimerkiksi yritys tarjoaa kahdenlaisia henkivakuutus hyötyä työntekijöille. Executive työntekijät ovat oikeutettuja yksi henkivakuutus suunnitelma kaikkien kokoaikaisten työntekijöiden ovat tukikelpoisia henkivakuutus suunnitelma. Dynamics 365 operaatioille voit luoda kaikki executive työntekijöiden edun kelpoisuus sääntö ja toinen sääntö kaikkien kokoaikaisten työntekijöiden ja näiden säännösten soveltaminen sitten asianmukaiset etu.

## <a name="enrollment"></a>Rekisteröityminen
Kun organisaation tarjoamat edut on luotu ja kelpoisuus määritetty, voit rekisteröidä työntekijät etuihin. Yhden prosessin aikana etuihin voi rekisteröidä yhden työntekijän tai useita työntekijäitä yhteen tai useaan etuun. 

Joskus organisaatio lopettaa tietyn edun tarjoamisen. Tällöin sinun täytyy päivittää etu ja jotka ovat rekisteröityneet työntekijät. Edun voimassaolon avulla voit muuttaa kyseisen etuuden samaan aikaan sekä etu-että työntekijän rekisteröintejä vanhentumispäivämäärä. Voit myös valita useita työntekijöitä, joka on rekisteröity johonkin etuun, ja muuttaa niiden kattamiseen päättymispäivämäärän. 

Etujen joukkopäättämisen avulla voi samaan tapaan laajentaa sekä edun että työntekijöiden rekisteröitymisten päättymispäivää, jos haluat edun olevan käytettävissä alkuperäistä aikaa pidempään.

<a name="see-also"></a>Lisätietoja
--------

[Benefit eligibility policies](benefit-eligibility-policies.md)


