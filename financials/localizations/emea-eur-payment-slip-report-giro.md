---
title: Slip maksuraportti Euroopassa
description: "Tässä aiheessa on tietoja maksun slip raportit Euroopassa."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264604
ms.assetid: 551e047b-4581-4a77-b470-c4f8d395c375
ms.search.region: Belgium, Denmark, Finland, Norway, Switzerland
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: c795466753ca1515790b7961b989aac6e7d63c2c
ms.lasthandoff: 03/31/2017


---

# <a name="payment-slip-report-for-europe"></a>Slip maksuraportti Euroopassa

Tässä aiheessa on tietoja maksun slip raportit Euroopassa.

Maksun slip raporttien toimintoja on käytettävissä oikeushenkilöt, joilla on Tanskan, Belgian, Norjan, Sveitsin tai Suomen niiden ensisijainen osoite. Yritykset liittää usein laskujen kirjausta, tilitystä maksuviite antamaan kirjallinen maksukuitit. Maksutositetta voidaan käyttää myynti- ja vapaatekstilaskujen lisäksi projekti- tai palvelulaskuissa, maksukehotteissa, korkolaskussa ja tiliotteissa.

## <a name="set-up-a-creditor-id-number-denmark-only"></a>Määritä velkojan tunnus (vain Tanska)
Anna yrityksesi luotonantajan tunnus (ID)-numeron seuraavasti. Tämä numero tarjoaa välityksellä. Sitä käytetään apuna, kun asiakkaan maksut vastaanotetaan rahoituslaitosten kautta.

1.  Valitse **organisaation hallinta**&gt;**asennus**&gt;**organisaation**&gt;**oikeushenkilöt**.
2.  - **Pankkitilitiedot** pikavälilehti, joka **FI-luotonantajan tunnus** 8-numeroinen yksilöllinen velkojan ID-tunnus-kenttään.
3.  Tallenna muutokset sulkemalla lomake.

## <a name="set-up-a-payment-slip-attachment-format-for-invoices-interest-notes-collection-letters-and-account-statements"></a>Määrittää maksun slip liitetiedoston muoto laskut, korkolaskuja, maksukehotuksia ja tiliotteet
Maksun slip liitteet mukana seuraaviin myyntilaskujen, vapaatekstilaskujen, korkolaskuja, maksukehotuksia ja tiliotteet muoto määritetään seuraavasti.

1.  Valitse **myynti**&gt;**asennus**&gt;**lomakkeita**&gt;**asetukset**.
2.  - **Laskun** -lehden **liittyvän maksun liite myyntilaskussa** maksun slip liitetiedoston muoto-kenttään.
3.  - **Vapaatekstilaskun**, **korkolaskun**, **maksukehotuksen**, ja **tilin tiliotteen** välilehtiä, valitse maksu slip liitetiedoston muoto kutakin tiedostotyyppiä.
4.  Tallenna muutokset sulkemalla lomake.

Määritä muoto, mukana projektilaskujen maksun slip liitteiden seuraavasti.

1.  Valitse **projekti, projektinhallinta- ja**&gt;**asennus**&gt;**lomakkeita**&gt;**asetukset**.
2.  - **Liittyvän maksun liite** maksun slip liitetiedoston muoto-kenttään.

## <a name="assign-a-payment-slip-attachment-format-to-a-customer-account"></a>Määrittää asiakastilin maksu slip liitteen muodossa
Kun määrität pakkausluettelon liite maksumuoto myyntilaskujen, vapaatekstilaskuja, korkolaskuja, maksukehotuksia, tiliotteet ja laskut, voit liittää valitun asiakkaan muotoilut.

1.  Valitse **myynti**&gt;**yhteisen**&gt;**asiakkaiden**&gt;**kaikille asiakkaille**.
2.  Luo uusi asiakas tai valitse olemassa oleva asiakas.
3.  - **Laskutus- ja** pikavälilehdessä- **asiakkaan laskun**, **Vapaatekstilasku-**, **korkolaskussa**, **maksukehotukseen**, **projektin laskuun**, ja **tiliotteesta** kentät, valitse muoto maksu slip liitteet, jotka liitetään kunkin valitulle asiakkaalle lähetettäviin asiakirjoihin.
4.  Tallenna muutokset sulkemalla lomake.



