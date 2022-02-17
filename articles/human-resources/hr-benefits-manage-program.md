---
title: Etuohjelman määrittäminen ja hallinta
description: Henkilöstöhallinto sisältää joukon työkaluja, joiden avulla organisaation tarjoamia tai työntekijöitä varten käsittelemiä etuja, vähennyksiä ja työntekijöiden kompensaatiosuunnitelmia voi määrittää ja ylläpitää. Tässä artikkelissa on tietoja etujen määrittämisestä ja hallinnasta.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 1f2bfa901aa299a091194978ee95ff0e69f2cdbf
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065348"
---
# <a name="define-and-manage-a-benefits-program"></a>Etuohjelman määrittäminen ja hallinta


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Henkilöstöhallinto sisältää joukon työkaluja, joiden avulla organisaation tarjoamia tai työntekijöitä varten käsittelemiä etuja, vähennyksiä ja työntekijöiden kompensaatiosuunnitelmia voi määrittää ja ylläpitää. Tässä artikkelissa on tietoja etujen määrittämisestä ja hallinnasta.

## <a name="benefit-setup"></a>Etujen asetukset

Työntekijät voidaan rekisteröidä etuihin sen jälkeen, kun kunkin edun elementit on luotu. Nämä elementit yhdistävät samanlaiset etusuunnitelmat ja määrittävät oletusasetukset, kuten vähennysten määrät ja kirjanpitotiedot. Useita asetuksia voidaan muokata myöhemmin, kun työntekijät rekisteröidään etuun. Organisaation etusuunnitelmassa voi olla useita rekisteröitymisasetuksia tai työntekijä voi peruuttaa suunnitelmaan rekisteröitymisen. 

[![Etuprosessin työnkulku.](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Edun elementit

Ennen etuuden luomista ja työntekijöiden rekisteröimistä niihin on määritettävä elementit, jotka muodostavat edut. Näitä elementtejä ovat tyyppi, suunnitelma ja vaihtoehdot.

-   **Tyyppi** – kokoelma tietynlaisia etuussuunnitelmia, kuten työterveys tai pysäköinti.
-   **Suunnitelma** – tietty etuus, jonka tarjoamisesta on tehty sopimus palveluntarjoajan kanssa.
-   **Asetus** – kattavuustaso, kuten vain työntekijöille tarkoitettu tai työntekijä ja puoliso/kumppani.

Organisaatio voi tarjota työntekijöille jokaista etutyyppiä, kuten näöntarkistusta tai hammashuoltoa, varten yhden tai useita suunnitelmia. Organisaatio voi tarjota kutakin suunnitelmaa varten useita asetuksia. Työntekijät voivat ostaa esimerkiksi henkivakuutuksen lisävakuutusturvan, joka on vuosipalkan suuruinen tai kaksi tai kolme kertaan sen suuruinen. Jokaisesta suunnitelman ja asetusten yhdistelmästä muodostuu etu, johon työntekijät voivat rekisteröityä. 

[![edun kuva.](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>Kelpoisuus
Useat tekijät määrittävät työntekijän kelpoisuuden työnantajan tarjoamiin erilaisiin etutyyppeihin. Kun etu luodaan Dynamics 365 Human Resourcesissa, etuun liittyvän kelpoisuuden tyyppi voidaan määrittää. 

Voit tehdä edun käytettäväksi kaikille työntekijöille. Jotkin yritykset tarjoavat esimerkiksi pysäköintilippuja luontaisetuna kaikille työntekijöille. Kun tämä etu luodaan, määritä kelpoisuuden arvoksi **Kaikki työntekijät ovat oikeutettuja**. 

Muissa eduissa, kuten, palkanpidätyksissä ja veroissa, kelpoisuus ei ole voimassa. Kun luot tämän tyyppisiä etuja, kelpoisuuden arvoksi määritetään **Kaikki työntekijät ovat oikeutettuja**. 

Etukelpoisuus voi perustua sääntöön. Esimerkissä yritys tarjoaa työntekijöille kahta erityyppistä henkivakuutusetua. Johtotason työntekijät ovat oikeutettuja eri henkivakuutussuunnitelmaan kuin kokoaikaiset työntekijät. Human Resourcesissa voidaan luoda etukelpoisuuden sääntö, jonka avulla etsitään johtotason työntekijät, ja toinen sääntö, jonka avulla etsitään kokoaikaiset työntekijät. Tämän jälkeen säännöt kohdistetaan soveltuvaan etuun.

## <a name="enrollment"></a>Rekisteröityminen
Kun organisaation tarjoamat edut on luotu ja kelpoisuus määritetty, voit rekisteröidä työntekijät etuihin. Yhden prosessin aikana etuihin voi rekisteröidä yhden työntekijän tai useita työntekijäitä yhteen tai useaan etuun. 

Joskus organisaatio lopettaa tietyn edun tarjoamisen. Tällöin etu ja siihen rekisteröidyt työntekijät on päivitettävä. Etujen joukkopäättämisen avulla voit muuttaa samalla sekä edun että työntekijän rekisteröimisten päättymispäivää. Voit myös valita useita työntekijöitä, joka on rekisteröity johonkin etuun, ja muuttaa niiden kattamiseen päättymispäivämäärän. 

Etujen joukkopäättämisen avulla voi samaan tapaan laajentaa sekä edun että työntekijöiden rekisteröitymisten päättymispäivää, jos haluat edun olevan käytettävissä alkuperäistä aikaa pidempään.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
