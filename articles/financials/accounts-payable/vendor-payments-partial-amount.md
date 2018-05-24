---
title: Toimittajan maksut osasummalla
description: "Joskus toimittajalle saatetaan luoda maksu, jonka summa on laskun summaa pienempi. Tässä artikkelissa on kuvaus erilaisista toimintavaihtoehdoista tällaisessa tilanteessa."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d8c012d3e88f3f4fe2e60f1db59978e326c42681
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="vendor-payments-for-a-partial-amount"></a>Toimittajan maksut osasummalle

[!include [banner](../includes/banner.md)]

Joskus toimittajalle saatetaan luoda maksu, jonka summa on laskun summaa pienempi. Tässä artikkelissa on kuvaus erilaisista toimintavaihtoehdoista tällaisessa tilanteessa. Käytettävissä olevat vaihtoehdot määräytyvät liiketoiminnan vaatimusten ja konfiguraation mukaan. 

<a name="cash-discount-amounts"></a>Käteisalennussummat
---------------------

Toimittaja voi tarjota yrityksellesi käteisalennuksen, jos maksat laskun ennen eräpäivää. Voit syöttää esimerkiksi laskun summaksi 100,00, jolle määritetään 2 prosentin käteisalennus, jos lasku maksetaan 10 päivän kuluessa. Maksuehto on 30 päivää. Jos maksuehdotuksessa käytetään käteisalennusta ehtona laskun valinnalle, ja jos ehdotus ajetaan käteisalennuspäivämääränä tai sitä ennen, lasku valitaan maksettavaksi ja maksu luodaan arvolle 98,00. Käteisalennusta voi myös käyttää yksittäiselle, manuaalisesti luodulle maksulle.

## <a name="partial-payments-with-cash-discounts"></a>Osamaksut käteisalennuksella
Kun suoritat osamaksun, suunnitelmana voi olla suorittaa toinen osamaksu laskun loppuun maksamiseksi. Jos haluat käyttää käteisalennusta osittaismaksussa, sinun on määritettävä **Laske käteisalennukset osamaksuille** -asetukseksi **Kyllä** **Ostoreskontran parametrit** -sivulla. 

Saat esimerkin mukaisesti 2 prosentin käteisalennuksen, jos lasku maksetaan 10 päivän kuluessa sen luonnista. Laskun arvoksi on kirjattu 100,00. Jos suoritat maksun summalla 49,00 10 päivän kuluessa, kirjaat maksuksi 49,00 maksujen kirjauskansioon. Kun täsmäytät osamaksun **Selvitä avoimet tapahtumat** -sivulla, **1,00** näkyy **Käytettävä käteisalennussumma** -kentässä. 

> [!NOTE] 
> Jos kirjaat osamaksun ja jätät koko laskusumman **Täsmäytettävä summa** -kenttään, **Käytettävä käteisalennussumma** -kenttä lasketaan uudelleen automaattisesti, kun kirjaat tapahtumat.

## <a name="credit-notes-with-cash-discounts"></a>Hyvityslaskut ja käteisalennukset
Saatat palauttaa laskulla olevia nimikkeitä ja saada niistä hyvityslaskun. Jos käteisalennusta oli käytetty alkuperäisellä laskulla, voit vähentää alennuksen arvon ja saada palautuksen oikealle summalle. Jos **Laske käteisalennukset hyvityslaskuille** -asetukseksi on määritetty **Kyllä** **Ostoreskontran parametrit** -sivulla, alennus lasketaan automaattisesti hyvityslaskulle. 

Saat esimerkin mukaisesti 2 prosentin käteisalennuksen, jos lasku maksetaan 10 päivän kuluessa sen luonnista. Laskun kirjataan arvolla 100,00. Jos palautat tavarat ja vastaanotat hyvityslaskun, voit syöttää hyvityslaskun kokonaisuudessaan alkuperäisen laskun summalle, 100,00, mukaan lukien 2 prosentin käteisalennus, joka on myös määritetty hyvityslaskulla.  Kun tarkastelet hyvityslaskua **Tilitä tapahtumat** -sivulla, **98,00** näkyy **Tilitettävä summa** -kentässä ja **-2,00** näkyy **Käteisalennuksen summa** -kentässä. Alennussumma kirjataan käteisalennustilille.

## <a name="overpaymentunderpayment-amounts"></a>Liika-/alisuorituksen summat
Voit suorittaa osamaksun, jonka jälkeen tilitettäväksi voi jäädä hyvin pieni summa. Toimittajan laskun summa on esimerkiksi 1 000,00 ja suoritat maksun summalle 999,90. Jos jäljelle jäävä summa on pienempi kuin liika-/alisuorituksen summa, joka on määritetty **Ostoreskontran parametrit** -sivulla, erotus kirjataan automaattisesti liika-/alisuorituksien kirjanpitotilille.


Lisätietoja on ohjeaiheessa [Toimittajan maksujen yleiskatsaus](../cash-bank-management/tasks/vendor-payment-overview.md).

