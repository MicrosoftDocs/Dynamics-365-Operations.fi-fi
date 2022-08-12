---
title: Pankkitilin täsmäytyksen lisätoimintojen yhteenveto
description: Tässä artikkelissa kuvataan pankkitilin täsmäytysprosessin lisätoimintojen työnkulku. Pankkitilin täsmäytyksen lisätoimintojen avulla voit tuoda tiliotteet, jotka voidaan täsmäyttää automaattisesti pankkitapahtumista.
author: angelad116
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: kfend
ms.custom:
- "22104"
- intro-internal
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 96542aa2ee1fed85864b7695199df464ca7866be
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151650"
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
