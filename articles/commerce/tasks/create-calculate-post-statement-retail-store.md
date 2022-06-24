---
title: Vähittäismyymälän laskelmien luominen, laskeminen ja kirjaaminen
description: Tässä artikkelissa kerrotaan myymälän laskelman luomisen, laskemisen ja kirjaamisen manuaaliset vaiheet.
author: jashanno
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 740857e6a902e21588855eef5e36cac68e560898
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873275"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a>Vähittäismyymälän laskelmien luominen, laskeminen ja kirjaaminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan myymälän laskelman luomisen, laskemisen ja kirjaamisen manuaaliset vaiheet. Samalle tehtävälle voidaan määrittää myös erätöitä. Erätöiden määrittämisen ja suorittamisen vaiheet löytyvät myös muista artikkeleista. Tämän menettelyn suorittaminen edellyttää myyntipisteellä tehtyjä ja Dynamics 365 Commerceiin siirrettyjä tapahtumia. Tämä tallenne käyttää esittelytietojen USRT-yritystä.

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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]