---
title: Toimittajan laskun tallentaminen laskukirjauskansioon
description: Tässä ohjauksessa näytetään, miten ostotilauksiin liittämättömät toimittajan laskut tallennetaan.
author: abruer
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35862195f3c2c13711157be919956f40fea0989b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820638"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Toimittajan laskun tallentaminen laskukirjauskansioon

[!include [banner](../../includes/banner.md)]

Tässä ohjauksessa näytetään, miten ostotilauksiin liittämättömät toimittajan laskut tallennetaan. Tällaisia laskuja ovat esimerkiksi tarvikkeiden tai palveluiden kulut.  Tässä tallenteessa käytetään esittely-yritystä USMF.

1. Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Työtilat > Toimittajan laskun syöttö**.
2. Napsauta **Toimintoruudussa** **Uusi laskukirjauskansio**.
3. Valitse **Uusi**.
4. Avaa haku syöttämällä **Nimi**-kenttään kirjauskansion nimi tai valitsemalla avattavan valikon painike.
5. Kirjoita **Kuvaus**-kenttään arvo.
6. Valitse **toimintoruudussa** **Rivit**. Syötä **Päivämäärä**-kenttään kirjauspäivämäärä, joka päivittää kirjanpidon.  
7. Määritä **Tili**-kenttään **Toimittajan tili**.
8. Syötä **Lasku**-kenttään laskunumero.
9. Kirjoita **Kuvaus**-kenttään arvo.
10. Syötä **Kredit**-kenttään numero.
11. Avaa haku syöttämällä **Vastatili**-kenttään tilinumero nimi tai valitsemalla avattavan valikon painike
    * **Arvonlisäveroryhmän** oletusarvo saadaan toimittajan tililtä.  
    * **Nimikkeen arvonlisäveroryhmän** oletusarvo saadaan **Vastatili**-kentässä määritetyltä päätililtä.  
    * **Eräpäivä** lasketaan maksuehtojen perusteella.  
    * **Käteisalennuksen** oletusarvo saadaan toimittajan tililtä.
12. Jos toimittajan laskukirjauskansion työnkulku on otettu käyttöön, valitse **Työnkulku > Lähetä**.
    * Kun lähetys on hyväksytty, päivämäärä lisätään seuraavan avoimen kauden ensimmäiseen päivään, jos tapahtuman kirjauspäivämäärä on sellaisen kauden sisällä, joka on pidossa tai suljettu kirjanpidon kirjausta varten.
12. Valitse **Kirjaa**.
13. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]