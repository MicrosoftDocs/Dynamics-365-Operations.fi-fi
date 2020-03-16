---
title: Viivakoodien määrittäminen
description: Tässä artikkelissa käsitellään viivakoodien käyttöä Dynamics 365 Commerceissa.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 52801e0d09b1d7da50719966700ca45275d702f7
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057275"
---
# <a name="set-up-bar-codes"></a>Viivakoodien määrittäminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään viivakoodien käyttöä Dynamics 365 Commerceissa.

Voit käyttää viivakoodeja tuotteiden ostamisessa ja myynnissä, tuotevarianttien seurannassa sekä asiakkaiden ja työntekijöiden määrittämisessä. Voit lisäksi käyttää viivakoodeja kuponkien, lahjakorttien ja hyvityslaskujen antamiseen ja käyttöön. Tuotteet voi määrittää niin, että niillä on joko vakioviivakoodit tai itse kehitetyt viivakoodit. Tuotteilla voi olla useampi viivakoodi. Tuotteella voi esimerkiksi olla useita viivakoodeja, jos se on peräisin usealta valmistajalta tai jos sillä on kokoon, tyyliin tai väriin perustuvia variantteja. Viivakoodit voivat sisältää tuotteen painon tai hinnan. Viivakoodin muodot ovat malleja, joita käytetään viivakoodien luomiseen.

> [!NOTE]
> Jos määrität kullekin varianttiyhdistelmälle yksilöllisen viivakoodin, voit lukea nimikkeen viivakoodin kassalla ja antaa ohjelman etsiä myytävän tuotevariantin. Voit myös kerätä ja tarkastella varianttiperusteisia myyntitilastoja. Kullekin koko-, väri- ja tyyliryhmälle voidaan määrittää yksilöllinen luku, joka yksilöi ryhmän viivakoodissa. Commerce muodostaa viivakoodit automaattisesti kullekin muuttujayhdistelmälle viivakoodin muodon perusteella. Tämä toiminto voi olla hyödyllinen, jos kokoja, värejä ja tyylejä on paljon, koska jokainen lisätty varianttikoodi suurentaa yhdistelmää merkittävästi. Jos toimintoa ei käytetä, viivakoodit täytyy määrittää manuaalisesti kuhunkin tuotevarianttia tarkoittavaan yhdistelmään.

Viivakoodeja voi luoda manuaalisesti tai automaattisesti. Viivakoodien luonti tapahtuu noudattamalla seuraavia tehtäviä järjestyksessä.

1. [Viivakoodin muodon merkkien määrittäminen](set-up-bar-code-masks.md).
2. [Viivakoodin muotojen määrittäminen](set-up-bar-code-masks.md).
3. Määritä viivakoodiasetukset.
4. Luo viivakoodit tuotteille.

## <a name="additional-resources"></a>Lisäresurssit

[Viivakoodin muotojen määrittäminen](set-up-bar-code-masks.md)
