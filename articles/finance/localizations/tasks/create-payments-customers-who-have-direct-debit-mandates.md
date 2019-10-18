---
title: Maksujen luominen asiakkaalle, jolla on suoraveloitusvaltakirjoja
description: Näiden ohjeiden avulla voit luoda ISO20022-suoraveloituksen maksutiedoston asiakkaalle, jolle on määritetty suoraveloitus ja jolla on maksettava lasku.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, LedgerJournalTable, LedgerJournalTransCustPaym, SysQueryForm, CustPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 129c5291a29994f91ef325aa9b9a3b54a0e958d6
ms.sourcegitcommit: 807dec193cd163c9f5d949e744cfde40f2eb24b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2468952"
---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a>Maksujen luominen asiakkaalle, jolla on suoraveloitusvaltakirjoja

[!include [task guide banner](../../includes/task-guide-banner.md)]

Näiden ohjeiden avulla voit luoda ISO20022-suoraveloituksen maksutiedoston asiakkaalle, jolle on määritetty suoraveloitus ja jolla on maksettava lasku. Laskun luominen ja kirjaaminen on vapaaehtoista. Sen sijaan, että lasku maksettaisiin, voit valita valtakirjan kirjauskansiossa ennen maksutiedoston luomista, jos haluat tukea asiakkaan ennakkomaksuja.



Tämän menettelyn luomisessa käytetty esittely-yritys on DEMF.



Tämä on viimeinen viidestä tehtävästä, joilla esitellään asiakasmaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä. Edelliset tehtävät on suoritettava ennen tätä tehtävää. Sinun on ensiksi tuotava asiakkaan maksun sähköiset raportointimääritykset, määritettävä maksutavat sekä määritettävä yrityksen ja asiakkaan tiedot. 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a>Kirjaa vapaatekstilasku suoraveloitustietoineen
1. Siirry kohtaan Myyntireskontra > Laskut > Kaikki vapaatekstilaskut.
2. Valitse Uusi.
3. Syötä tai valitse arvo Asiakastili-kentässä.
    * Valitse esimerkiksi arvo DE-010.  
4. Anna tai valitse arvo Maksutapa-kentässä.
    * Esimerkki: valitse Sähköinen.  
5. Anna tai valitse Suoraveloitusvaltakirjan tunnus -kentässä arvo.
6. Valitse Lisää rivi.
7. Kirjoita Kuvaus-kenttään arvo.
8. Määritä Päätili-kenttään haluamasi arvot.
9. Syötä Yksikköhinta-kenttään numero.
10. Valitse Kirjaa.
11. Valitse OK.

## <a name="create-a-payment"></a>Luo maksu
1. Siirry kohtaan Myyntireskontra > Maksut > Maksukirjauskansio.
2. Valitse Uusi.
3. Syötä tai valitse arvo Nimi-kenttään.
4. Valitse Rivit.
5. Valitse Maksuehdotus.
6. Valitse Luo maksuehdotus.
7. Laajenna Tietueet-kohta ja sisällytä osaan.
8. Valitse Suodatin.
9. Valitse luettelosta Asiakastapahtumat-taulukon ja Maksutapa-kentän rivi.
    * Voit käyttää mitä tahansa ehtoja maksettavien asiakastapahtumien valinnassa. Tässä esimerkissä käytetään tapahtumien suodattamiseen maksutapaa Sähköinen.  
10. Syötä tai valitse arvo Ehdot-kenttään.
11. Valitse OK.
12. Valitse OK.
13. Valitse Luo maksut.
