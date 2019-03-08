---
title: Viivakoodien määrittäminen
description: Tässä artikkelissa käsitellään viivakoodien käyttöä Microsoft Dynamics 365 for Retailissa.
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
ms.openlocfilehash: 15d12abe32d3f5a47348016c67a4fb02d0a5d8e3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "347350"
---
# <a name="set-up-bar-codes"></a>Viivakoodien määrittäminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään viivakoodien käyttöä Microsoft Dynamics 365 for Retailissa.

Voit käyttää viivakoodeja tuotteiden ostamisessa ja myynnissä, tuotevarianttien seurannassa sekä asiakkaiden ja työntekijöiden määrittämisessä. Voit lisäksi käyttää viivakoodeja kuponkien, lahjakorttien ja hyvityslaskujen antamiseen ja käyttöön. Vähittäismyynnin tuotteet voi määrittää niin, että niillä on joko vakioviivakoodit tai itse kehitetyt viivakoodit. Tuotteilla voi olla useampi viivakoodi. Tuotteella voi esimerkiksi olla useita viivakoodeja, jos se on peräisin usealta valmistajalta tai jos sillä on kokoon, tyyliin tai väriin perustuvia variantteja. Viivakoodit voivat sisältää tuotteen painon tai hinnan. Viivakoodin muodot ovat malleja, joita käytetään viivakoodien luomiseen.

> [!NOTE]
> Jos määrität kullekin varianttiyhdistelmälle yksilöllisen viivakoodin, voit lukea nimikkeen viivakoodin kassalla ja antaa ohjelman etsiä myytävän tuotevariantin. Voit myös kerätä ja tarkastella varianttiperusteisia myyntitilastoja. Kullekin koko-, väri- ja tyyliryhmälle voidaan määrittää yksilöllinen luku, joka yksilöi ryhmän viivakoodissa. Dynamics 365 for Retail muodostaa viivakoodit automaattisesti kullekin muuttujayhdistelmälle viivakoodin muodon perusteella. Tämä toiminto voi olla hyödyllinen, jos kokoja, värejä ja tyylejä on paljon, koska jokainen lisätty varianttikoodi suurentaa yhdistelmää merkittävästi. Jos toimintoa ei käytetä, viivakoodit täytyy määrittää manuaalisesti kuhunkin tuotevarianttia tarkoittavaan yhdistelmään.

Viivakoodeja voi luoda manuaalisesti tai automaattisesti. Viivakoodien luonti tapahtuu noudattamalla seuraavia tehtäviä järjestyksessä.

1. [Viivakoodin muodon merkkien määrittäminen](set-up-bar-code-masks.md).
2. [Viivakoodin muotojen määrittäminen](set-up-bar-code-masks.md).
3. Määritä viivakoodiasetukset.
4. Luo viivakoodit tuotteille.

## <a name="additional-resources"></a>Lisäresurssit

[Viivakoodin muotojen määrittäminen](set-up-bar-code-masks.md)
