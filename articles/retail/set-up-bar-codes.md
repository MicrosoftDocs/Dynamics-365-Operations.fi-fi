---
title: "Määritä viivakoodit"
description: "Tässä artikkelissa kuvataan viivakoodien käyttö Microsoft Dynamics 365 for Retailissa."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bfb47e653cc3ef36135fd7c4f60771a354699af7
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-bar-codes"></a>Viivakoodien määrittäminen

[!include[banner](includes/banner.md)]


Tässä artikkelissa kuvataan viivakoodien käyttö Microsoft Dynamics 365 for Retailissa.

Voit käyttää viivakoodeja tuotteiden ostamisessa ja myynnissä, tuotevarianttien seurannassa sekä asiakkaiden ja työntekijöiden määrittämisessä. Voit lisäksi käyttää viivakoodeja kuponkien, lahjakorttien ja hyvityslaskujen antamiseen ja käyttöön. Vähittäismyynnin tuotteet voi määrittää niin, että niillä on joko vakioviivakoodit tai itse kehitetyt viivakoodit. Tuotteilla voi olla useampi viivakoodi. Tuotteella voi esimerkiksi olla useita viivakoodeja, jos se on peräisin usealta valmistajalta tai jos sillä on kokoon, tyyliin tai väriin perustuvia variantteja. Viivakoodit voivat sisältää tuotteen painon tai hinnan. Viivakoodin muodot ovat malleja, joita käytetään viivakoodien luomiseen. **Huomautus:** Jos määrität kullekin varianttiyhdistelmälle yksilöllisen viivakoodin, voit lukea nimikkeen viivakoodin kassalla ja antaa ohjelman etsiä myytävän tuotevariantin. Voit myös kerätä ja tarkastella varianttiperusteisia myyntitilastoja. Kullekin koko-, väri- ja tyyliryhmälle voidaan määrittää yksilöllinen luku, joka yksilöi ryhmän viivakoodissa. Dynamics 365 for Retail muodostaa viivakoodit automaattisesti kullekin muuttujayhdistelmälle viivakoodin muodon perusteella. Tämä toiminto voi olla hyödyllinen, jos kokoja, värejä ja tyylejä on paljon, koska jokainen lisätty varianttikoodi suurentaa yhdistelmää merkittävästi. Jos toimintoa ei käytetä, viivakoodit täytyy määrittää manuaalisesti kuhunkin tuotevarianttia tarkoittavaan yhdistelmään. Viivakoodeja voi luoda manuaalisesti tai automaattisesti. Viivakoodien luonti tapahtuu noudattamalla seuraavia tehtäviä järjestyksessä.

1.  [Viivakoodin muodon merkkien määrittäminen](set-up-bar-code-masks.md).
2.  [Viivakoodin muotojen määrittäminen](set-up-bar-code-masks.md).
3.  Määritä viivakoodiasetukset.
4.  Luo viivakoodit tuotteille.


<a name="see-also"></a>Lisätietoja
--------

[Viivakoodin muotojen määrittäminen](set-up-bar-code-masks.md)




