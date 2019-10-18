---
title: Maksuluetteloraportti Euroopassa
description: Tässä aiheessa on tietoja maksuluetteloraporteista Euroopassa.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMLegalEntities, ProjFormletterParameters, CustFormletterParameters
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 264604
ms.search.region: Belgium, Denmark, Finland, Norway, Switzerland
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cbbfa25252074cd371b271be2f0f03ad2a687944
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175745"
---
# <a name="payment-slip-report-for-europe"></a>Maksuluetteloraportti Euroopassa

[!include [banner](../includes/banner.md)]

Tässä aiheessa on tietoja maksuluetteloraporteista Euroopassa.

Maksuluetteloraporttien toiminnot on käytettävissä yrityksille, joilla on ensisijainen osoite Tanskassa, Belgiassa, Norjassa, Sveitsissä tai Suomessa. Yritykset usein liittävät usein asiakkaiden laskuihin tulostetun maksutositteen, jossa on maksuviite kirjaamista ja tilitystä varten. Maksutositetta voidaan käyttää myynti- ja vapaatekstilaskujen lisäksi projekti- tai palvelulaskuissa, maksukehotteissa, korkolaskussa ja tiliotteissa.

## <a name="set-up-a-creditor-id-number-denmark-only"></a>Määritä laskuttajan tunnusnumero (vain Tanska)
Anna yrityksesi luotonantajan tunnus (ID) -numero seuraavasti. Saat tämän numeron rahoituslaitokseltasi. Sitä käytetään viitteenä, kun asiakkaan maksut vastaanotetaan rahoituslaitosten kautta.

1.  Siirry kohtaan **Organisaation hallinto** &gt; **Asetukset** &gt; **Organisaatio** &gt; **Yritykset**.
2.  Anna **Pankkitilitiedot**-pikavälilehden **FI-luotonantajan tunnus** -kentässä 8-numeroinen yksilöllinen velkojan ID-tunnus.
3.  Tallenna muutokset sulkemalla lomake.

## <a name="set-up-a-payment-slip-attachment-format-for-invoices-interest-notes-collection-letters-and-account-statements"></a>Määritä maksutositteen muoto laskuille, korkolaskuille, maksukehotuksille ja tiliotteille
Määritä myyntilaskujen, vapaatekstilaskujen, korkolaskujen, maksukehotusten ja tiliotteiden liitteenä lähetettävän maksutositteen muoto seuraavasti.

1.  Valitse **Myyntireskontra** &gt; **Asetukset** &gt; **Lomakkeet** &gt; **Lomakeasetukset**.
2.  Valitse **Lasku**-välilehden **Asiakkaan laskun liittyvä maksun liite** -kentässä maksutositteen liitetiedoston muoto.
3.  Valitse **Vapaatekstilasku**-, **Korkolasku**-, **Maksukehotus**- ja **Tiliote**-välilehdissä, maksutositteen liitetiedoston muoto kullekin asiakirjatyypille.
4.  Tallenna muutokset sulkemalla lomake.

Määritä maksutositeliitteiden muoto, joka liitetään projektilaskuihin, seuraavasti.

1.  Valitse **Projektinhallinta ja kirjanpito** &gt; **Asetukset** &gt; **Lomakkeet** &gt; **Lomakeasetukset**.
2.  Valitse **Liittyvän maksun liite** -kentässä maksutositeliitteen muoto.

## <a name="assign-a-payment-slip-attachment-format-to-a-customer-account"></a>Maksukuittiliitteen muodon määrittäminen asiakastilille
Kun olet määrittänyt maksutositeliitteen muodon myyntilaskuille, vapaatekstilaskuille, korkolaskuille, maksukehotuksille, tiliotteille ja projektilaskuille, voit määrittää valitun asiakkaan muotoilut.

1.  Valitse **Myyntireskontra** &gt; **Yleinen** &gt; **Asiakkaat** &gt; **Kaikki asiakkaat**.
2.  Luo uusi asiakas tai valitse aiemmin määritetty asiakas.
3.  Valitse **Lasku ja toimitus** -pikavälilehden **Myyntilaskussa**-, **Vapaatekstilaskussa**-, **Korkolaskussa**-, **Maksukehotuksessa**-, **Projektilaskussa**- ja **Tiliotteessa**-kentissä muoto maksutositeliitteille, jotka liitetään valitulle asiakkaalle lähetettäviin eri tyyppisiin asiakirjoihin.
4.  Tallenna muutokset sulkemalla lomake.




