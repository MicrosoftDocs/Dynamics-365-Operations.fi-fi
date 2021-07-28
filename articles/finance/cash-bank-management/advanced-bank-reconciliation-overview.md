---
title: Pankkitilin täsmäytyksen lisätoimintojen yhteenveto
description: Tässä artikkelissa kuvataan pankkitilin täsmäytysprosessin lisätoimintojen työnkulku. Pankkitilin täsmäytyksen lisätoimintojen avulla voit tuoda tiliotteet, jotka voidaan täsmäyttää automaattisesti pankkitapahtumista.
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "22104"
- intro-internal
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93ba7c8dc29a50de4b4cec342a5a83efe03e6419
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/03/2021
ms.locfileid: "6336138"
---
# <a name="advanced-bank-reconciliation-overview"></a>Pankkitilin täsmäytyksen lisätoimintojen yhteenveto

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan pankkitilin täsmäytysprosessin lisätoimintojen työnkulku. Pankkitilin täsmäytyksen lisätoimintojen avulla voit tuoda tiliotteet, jotka voidaan täsmäyttää automaattisesti pankkitapahtumista.

Pankkitilin täsmäytyksen lisätoimintojen avulla tuodaan tiliotteita. Tuotu tiliote voidaan tämän jälkeen täsmäyttää automaattisesti pankkitapahtumista. Pankkitilin täsmäytyksen lisätoimintojen työnkulun vaiheet ovat seuraavat.

1.  Määritä tiliotteen tuonti.
    -   Tuo tiliotteet tietoyksikön ympäristön kautta.
    -   Muodostetaan kolme tavallista tiliotteen muotoa: ISO20022, BAI2 ja MT940.
    -   Toimintoja voidaan käyttää missä tahansa muodossa.

2.  Määritä numerosarja pankin täsmäytyksen lisätoimintoja varten. Määritä myös pankin täsmäytyssäännöt.
    -   Täsmäytyssääntö on ehtojoukko, joilla suodatetaan tiliotteen rivejä ja Microsoft Dynamics 365 Financen pankkitapahtuman rivejä täsmäytysprosessin aikana. Liiketoimintakäytäntöjesi mukaan voit määrittää useita vastaavia sääntöjä automatisoidaksesi ja optimoidaksesi täsmäytysprosessin.

3.  Täsmäytä tiliotteet Financen pankkitapahtumien kanssa.
    -   Suorita täsmäytyksen kirjauskansioille automaattinen täsmäytys ja luonti.
    -   Tarkastele rinnakkain tiliotteita ja Financen pankkitapahtumia.
    -   Kirjaa Financen pankkitapahtumat automaattisesti, jos ne näkyvät tiliotteella, mutta eivät Finance-sovelluksessa.
    -   Luo täsmäytystiliote.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]