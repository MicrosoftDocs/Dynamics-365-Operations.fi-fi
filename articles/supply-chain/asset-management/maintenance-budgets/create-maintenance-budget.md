---
title: Luo ylläpitobudjetit
description: Tässä ohjeaiheessa kerrotaan, kuinka ylläpitobudjetti luodaan resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetBudgetLineAdjust, EntAssetBudget, EntAssetBudgetRecalc, EntAssetBudgetCopy, EntAssetBudgetLine, EntAssetBudgetCreate, EntAssetBudgetApprove, EntAssetBudgetCalculateActualCost
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 602a00060c1e56285d9954981d019bececaf90fd
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020986"
---
# <a name="create-maintenance-budgets"></a>Luo ylläpitobudjetit

[!include [banner](../../includes/banner.md)]

 



Kunnossapitobudjettien avulla luodaan yleiskatsaus ennakoivaan kunnossapitoon liittyvistä odotetuista kustannuksista. Budjettirivit lasketaan niiden kunnossapitoaikataulurivien perusteella, joiden odotettu alkamispäivämäärä on budjettikauden aikana.

Kunnossapitobudjetit perustuvat käyttöomaisuuden hallinnassa käytettyihin kustannustyyppeihin: **Ennaltaehkäisevä**, **Korjaava** ja **Investointi**. Investointi-ylläpidon budjetoidut kustannukset sisältyvät aktiivisiin käyttökohteisiin, joilla on korvauspäivä budjettikauden aikana sekä siihen liittyvä korvaava arvo. Korjaavan huollon budjetoidut kustannukset sisällytetään, jos edellinen oikaisupäivämäärä sisällytetään budjetin laskemiseen. Tällöin aiemman kauden korjaavat kustannukset lasketaan samalle tulevalle kaudelle, jolle ylläpitobudjettia lasketaan.

## <a name="create-a-maintenance-budget"></a>Luo ylläpitobudjetti

1. Valitse **Resurssien hallinta**\>**Kyselyt**\> **Ylläpitobudjetti** \> **Budjetti**.
2. Valitse **Luo budjetti**.
3. Kirjoita budjetin tunnus **Ylläpitobudjetti**-kenttään.
4. Syötä **Kuvaus**-kenttään kuvaus.
4. Määritä **Kausi**-pikavälilehden **Alkupäivämäärä** -ja **Päättymispäivämäärä**-kenttiin budjettikauden alkamis- ja päättymispäivämäärät.
5. Jos haluat sisällyttää korjattavat budjetti kustannukset, jotka lasketaan edellisen kauden todellisten kustannusten perusteella, määritä **Korjaus päivämäärästä** -kenttään sen kauden alkamispäivämäärä, josta nämä kustannukset sisällytetään.
6. Määritä viidessä **Ryhmittely**-pikavälilehdessä asetukset sen mukaan, miten yksityiskohtaisia tietoja budjetti edellyttää.
7. Valitse **OK**.
8. Valitsemalla **Budjettirivit** voit avata **Ylläpitobudjettirivit**-sivun, jossa voit tarkastella kaikkia kaudelle luotuja budjettirivejä.
9. Voit hyväksyä budjetin valitsemalla sen **Ylläpitobudjetit** -sivulta ja valitsemalla sitten **Hyväksy**. Valitse sitten **Hyväksy budjetti** -valintaikkunassa **OK**. Nimesi lisätään **Ylläpitobudjetit**-sivun **Hyväksynyt-** kenttään.

    > [!NOTE]
    > Kun olet hyväksynyt ylläpitobudjetin, et voi laskea uudelleen tai muuttaa **Ylläpitobudjetin rivit** -sivun liittyviä rivejä, ellet ensin poista hyväksyntää. Voit poistaa ylläpitobudjetin hyväksynnän valitsemalla sen **Ylläpitobudjetit** -sivulta ja valitsemalla sitten **Hyväksy**. Valitse sitten **Hyväksy budjetti** -valintaikkunassa **OK**.

![Ylläpitobudjetit](media/01-maintenance-budgets.png)

Voit myös luoda uuden ylläpitobudjetin kopioimalla aiemmin luodun budjetin. Valitse **Ylläpitobudjetit** -sivulla kopioitava budjetti ja valitse sitten **Kopioi**. Tästä lähestymistavasta on hyötyä, jos olet esimerkiksi luonut yhden kuukauden budjetin ja haluat kopioida sen muihin kuukausiin.

> [!NOTE]
> Kunnossapitobudjetissa lasketaan vain kunnossapitoaikatauluriveihin perustuvia budjettikustannuksia. Voit laskea saman kauden todelliset kustannukset käyttämällä **Resurssien kustannusten hallinta** -sivulla olevaa laskentaa. 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]