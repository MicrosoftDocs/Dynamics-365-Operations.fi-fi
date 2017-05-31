---
title: "Pankkitilin täsmäytyksen lisätoimintojen yhteenveto"
description: "Tässä artikkelissa kuvataan pankkitilin täsmäytysprosessin lisätoimintojen työnkulku. Pankkitilin täsmäytyksen lisätoimintojen avulla voit tuoda tiliotteet, jotka voidaan täsmäyttää automaattisesti pankkitapahtumista."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: deba55d5e1e376f3f4063f372bfe853fcaf20498
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Pankkitilin täsmäytyksen lisätoimintojen yhteenveto

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kuvataan pankkitilin täsmäytysprosessin lisätoimintojen työnkulku. Pankkitilin täsmäytyksen lisätoimintojen avulla voit tuoda tiliotteet, jotka voidaan täsmäyttää automaattisesti pankkitapahtumista.

Pankkitilin täsmäytyksen lisätoimintojen avulla tuodaan tiliotteita. Tuotu tiliote voidaan tämän jälkeen täsmäyttää automaattisesti pankkitapahtumista. Pankkitilin täsmäytyksen lisätoimintojen työnkulun vaiheet ovat seuraavat.

1.  Määritä tiliotteen tuonti.
    -   Tuo tiliotteet tietoyksikön ympäristön kautta.
    -   Muodostetaan kolme tavallista tiliotteen muotoa: ISO20022, BAI2 ja MT940.
    -   Toimintoja voidaan käyttää missä tahansa muodossa.

2.  Määritä numerosarja pankin täsmäytyksen lisätoimintoja varten. Määritä myös pankin täsmäytyssäännöt.
    -   Täsmäytyssääntö on ehtojoukko, jonka avulla tiliotteen ja Microsoft Dynamics 365 for Operationsin pankkitapahtuman rivejä suodatetaan täsmäytysprosessin aikana. Liiketoimintakäytäntöjesi mukaan voit määrittää useita vastaavia sääntöjä automatisoidaksesi ja optimoidaksesi täsmäytysprosessin.

3.  Täsmäytä tiliotteet Microsoft Dynamics 365 for Operationsin pankkitapahtumien kanssa.
    -   Suorita täsmäytyksen kirjauskansioille automaattinen täsmäytys ja luonti.
    -   Tarkastele rinnakkain tiliotteita ja Dynamics 365 for Operationsin pankkitapahtumia.
    -   Kirjaa Dynamics 365 for Operationsin pankkitapahtumat automaattisesti, jos ne näkyvät tiliotteella, mutta eivät Dynamics 365 for Operationsissa.
    -   Luo täsmäytystiliote.






