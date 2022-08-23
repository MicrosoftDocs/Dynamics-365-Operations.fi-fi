---
title: Viivakoodien määrittäminen
description: Tässä artikkelissa käsitellään viivakoodien käyttöä Dynamics 365 Commercessa.
author: josaw1
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.industry: Retail
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
ms.openlocfilehash: 5771ada4a9bba92fb32155ae425f08d6429b46e6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271793"
---
# <a name="set-up-bar-codes"></a>Viivakoodien määrittäminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään viivakoodien käyttöä Dynamics 365 Commercessa.

Voit käyttää viivakoodeja tuotteiden ostamisessa ja myynnissä, tuotevarianttien seurannassa sekä asiakkaiden ja työntekijöiden määrittämisessä. Voit lisäksi käyttää viivakoodeja kuponkien, lahjakorttien ja hyvityslaskujen antamiseen ja käyttöön. Tuotteet voi määrittää niin, että niillä on joko vakioviivakoodit tai itse kehitetyt viivakoodit. Tuotteilla voi olla useampi viivakoodi. Tuotteella voi esimerkiksi olla useita viivakoodeja, jos se on peräisin usealta valmistajalta tai jos sillä on kokoon, tyyliin tai väriin perustuvia variantteja. Viivakoodit voivat sisältää tuotteen painon tai hinnan. Viivakoodin muodot ovat malleja, joita käytetään viivakoodien luomiseen.

> [!NOTE]
> Jos määrität kullekin varianttiyhdistelmälle yksilöllisen viivakoodin, voit lukea nimikkeen viivakoodin kassalla ja antaa ohjelman etsiä myytävän tuotevariantin. Voit myös kerätä ja tarkastella varianttiperusteisia myyntitilastoja. Kullekin koko-, väri- ja tyyliryhmälle voidaan määrittää yksilöllinen luku, joka yksilöi ryhmän viivakoodissa. Commerce muodostaa viivakoodit automaattisesti kullekin muuttujayhdistelmälle viivakoodin muodon perusteella. Tämä toiminto voi olla hyödyllinen, jos kokoja, värejä ja tyylejä on paljon, koska jokainen lisätty varianttikoodi suurentaa yhdistelmää merkittävästi. Jos toimintoa ei käytetä, viivakoodit täytyy määrittää manuaalisesti kuhunkin tuotevarianttia tarkoittavaan yhdistelmään.

Viivakoodeja voi luoda manuaalisesti tai automaattisesti. Viivakoodien luonti tapahtuu noudattamalla seuraavia tehtäviä järjestyksessä.

1. [Viivakoodin muodon merkkien määrittäminen](set-up-bar-code-masks.md).
2. [Viivakoodin muotojen määrittäminen](set-up-bar-code-masks.md).
3. Määritä viivakoodiasetukset.
4. [Luo viivakoodit tuotteille](../supply-chain/pim/tasks/create-bar-code-product.md).

## <a name="additional-resources"></a>Lisäresurssit

[Viivakoodin muotojen määrittäminen](set-up-bar-code-masks.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
