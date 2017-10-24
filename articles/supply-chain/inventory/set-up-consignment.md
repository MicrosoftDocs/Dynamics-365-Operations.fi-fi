---
title: "Tavaralähetyksen määrittäminen"
description: "Tässä aiheessa kerrotaan, miten määritetään saapuvan tavaralähetyksen varastotoimintoja."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 41c1b8de0aae24efb30a670d3109b6d65e6abd9c
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-consignment"></a>Tavaralähetyksen määrittäminen

[!include[banner](../includes/banner.md)]


Tässä aiheessa kerrotaan, miten määritetään saapuvan tavaralähetyksen varastotoimintoja.

Tavaralähetysvarasto on varasto, joka on toimittajan omistaa mutta joka on varastoituna yrityksesi toimipaikalle. Kun haluat käyttää osan varastosta tai koko varaston, varaston omistajuus siirtyy yrityksellesi. Tässä aiheessa kuvataan tarvittavat asetukset tavaralähetysprosessien käyttöönottoon. Lisätietoja tavaralähetysprosesseista on kohdassa [Tavaralähetys](consignment.md).

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
Jos toimittajat käyttävät toimittajayhteistyöliittymää, he voivat valvoa sen avulla toimipaikan varaston kulutusta. Saat lisätietoja toimittajien määrittämisestä käyttämään toimittajayhteistyötä [Käyttöoikeuksien määrittäminen toimittajayhteistyöliittymän käyttäjille](../procurement/configure-security-vendor-portal-users.md).

