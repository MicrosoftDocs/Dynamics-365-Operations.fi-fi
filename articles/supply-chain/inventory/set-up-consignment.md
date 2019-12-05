---
title: Tavaralähetyksen määrittäminen
description: Tässä aiheessa kerrotaan, miten määritetään saapuvan tavaralähetyksen varastotoimintoja.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 04b3fb3038a1373e203ec240a0163cf67de655cc
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813838"
---
# <a name="set-up-consignment"></a>Tavaralähetyksen määrittäminen

[!include [banner](../includes/banner.md)]

Tässä aiheessa kerrotaan, miten määritetään saapuvan tavaralähetyksen varastotoimintoja.

Tavaralähetysvarasto on varasto, joka on toimittajan omistaa mutta joka on varastoituna yrityksesi toimipaikalle. Kun haluat käyttää osan varastosta tai koko varaston, varaston omistajuus siirtyy yrityksellesi. Tässä aiheessa kuvataan tarvittavat asetukset tavaralähetysprosessien käyttöönottoon. Lisätietoja tavaralähetysprosesseista on kohdassa [Tavaralähetyksen määrittäminen](consignment.md).

## <a name="inventory-owners"></a>Varaston omistajat
Saapuvien lähetyksen fyysisen varaston kirjaamiseksi täytyy määrittää toimittajan omistaja. Tämä tehdään **varaston omistaja** -sivulla. Kun valitset **toimittajatili** tämä luo oletusarvot **nimi** ja **omistaja** -kenttiin. Arvo **omistaja**-kentässä näytetään toimittajalle, joten voit halutessasi muuttaa sitä, jos ulkoisten käyttäjien ei ole helppoa tunnistaa toimittajan tilin nimiä. Voit muokata **omistaja** -kenttää ainoastaan siihen asti, kun olet tallentanut **varaston omistaja** -tietueen. **Nimi**-kenttä täytetään sen osapuolen tiedoilla, joihin toimittajatili liittyy, eikä sitä voi muuttaa.

[![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>Seurantadimensioryhmä
Nimikkeet, jotka on tarkoitus käyttää lähetysprosesseissa, on yhdistettävä **seurantadimensioryhmään** jossa **omistaja** dimension arvo määritetään **aktiivinen**. Omistaja-dimensiossa **Varastotilanne** ja **kirjanpitovarasto** -asetukset ovat aina valittuina. **Kattavuussuunnitelma dimension mukaan** ei ole koskaan valittuna.

[![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)

## <a name="inventory-ownership-change-journal"></a>Varaston omistajuuden muutoksen kirjauskansio
**Varaston omistajuuden muutos** -kirjauskansiota käytetään muuttamaan tavaralähetysvaraston omistajuus toimittajalta yritykselle, joka käyttää varastoa. Jokaiselle varastokirjauskansiolle on määritettävä nimi. Nämä nimet luodaan **Varastokirjauskansion nimet** -sivulla ja **kirjauskansiotyypiksi** on määritettävä **Omistajuuden muutos**.

[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Toimittajayhteistyö tavaralähetysprosessissa
Jos toimittajat käyttävät toimittajayhteistyöliittymää, he voivat valvoa sen avulla toimipaikan varaston kulutusta. Lisätietoja toimittajien määrittämisestä käyttämään toimittajayhteistyötä on kohdassa [Toimittajaportaalin käyttäjän suojaus](../procurement/configure-security-vendor-portal-users.md).
