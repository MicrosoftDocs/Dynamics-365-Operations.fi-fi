---
title: Laskelmien luonti, laskenta ja kirjaaminen vähittäismyymälälle
description: Tässä aiheessa kerrotaan myymälän laskelman luomisen, laskemisen ja kirjaamisen manuaaliset vaiheet.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21f1b0a34205e192957405bc9d298c45c8bb4d25
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412025"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a>Laskelmien luonti, laskenta ja kirjaaminen vähittäismyymälälle

[!include [banner](../includes/banner.md)]

Tässä aiheessa kerrotaan myymälän laskelman luomisen, laskemisen ja kirjaamisen manuaaliset vaiheet. Samalle tehtävälle voidaan määrittää myös erätöitä. Erätöiden määrittämisen ja suorittamisen vaiheet löytyvät myös muista aiheista. Tämän menettelyn suorittaminen edellyttää myyntipisteellä tehtyjä ja Dynamics 365 Commerceiin siirrettyjä tapahtumia. Tämä tallenne käyttää esittelytietojen USRT-yritystä.

1. Valitse kotisivulla **Myymälän myyntitiedot**.
2. Valitse **Uusi laskelma**.
3. Valitse **Myymälän numero** -kentästä vaihtoehto avattavasta luettelosta.
4. Valitse **OK**.
5. **Asetus**-ryhmässä on asetuksia, jotka ohjaavat laskelmaan sisällytettävien tapahtumien valintaa sekä tapahtumien laskentariveiksi ryhmittelyä. Voit avata **Asetus**-ryhmän ja muuttaa asetuksia tai käyttää oletusarvoja.  
    - **Laskelmatapa**-kentässä määritetään, miten laskelmarivit ryhmitellään.  
    - Valitse henkilökunnan jäsen tai kassakone **Henkilöstö/kassakone**-kentässä, jos haluat tehdä laskelman vain tietylle henkilökunnan jäsenelle tai kassakoneelle.  
6. Valitse vaihtoehto **Sulkemistapa**-kentässä.
7. Valitse toimintoruudusta **Laske laskelma**.
8. Valitse **Kyllä**.
    - Kun laskelma on tehty, jokaiselle käytetylle maksu- ja laskelmatavalle on luotu rivejä, jotka sisältävät kokonaissummat.  
    - Voit syöttää kullekin riville lasketun summan, jos summia on syötettävä tai päivitettävä. Laskettuun kenttää siirretään myyntipisteellä kassan maksuvälineittäin tehtyjen laskemistapahtumien summat.  
9. Valitse toimintoruudusta **Kirjaa laskelma**.
10. Valitse **Sulje**.
11. Sulje ruutu.
12. Valitse kotisivulla **Myymälän myyntitiedot**.
13. Valitse **Kirjatut laskelmat** -välilehti.

