---
title: Toimittajan maksut osasummalla
description: "Joskus toimittajalle saatetaan luoda maksu, jonka summa on laskun summaa pienempi. Tässä artikkelissa on kuvaus erilaisista toimintavaihtoehdoista tällaisessa tilanteessa. Käytettävissä olevat vaihtoehdot määräytyvät liiketoiminnan vaatimusten ja konfiguraation mukaan."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 4d243e6a9a68b69a6b32748344fc606ff3f2d965
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-payments-for-a-partial-amount"></a>Toimittajan maksut osasummalla

Joskus toimittajalle saatetaan luoda maksu, jonka summa on laskun summaa pienempi. Tässä artikkelissa on kuvaus erilaisista toimintavaihtoehdoista tällaisessa tilanteessa. Käytettävissä olevat vaihtoehdot määräytyvät liiketoiminnan vaatimusten ja konfiguraation mukaan. 

<a name="cash-discount-amounts"></a>Käteisalennussummat
---------------------

Toimittaja voi tarjota yrityksellesi käteisalennuksen, jos maksat laskun ennen eräpäivää. Voit syöttää esimerkiksi laskun summaksi 100,00, jolle määritetään 2 prosentin käteisalennus, jos lasku maksetaan 10 päivän kuluessa. Maksuehto on 30 päivää. Jos maksuehdotusta käytetään Käteisalennus laskun valintaehdot ehtona, ja jos Ehdotus käteisalennuksen päivämääränä tai sitä ennen, maksua varten valitut lasku ja maksu luodaan 98.00. Käteisalennus voidaan ottaa myös kertaluonteista maksua, joka on luotu manuaalisesti.

## <a name="partial-payments-with-cash-discounts"></a>Osamaksut käteisalennuksella
Kun suoritat osamaksun, suunnitelmana voi olla suorittaa toinen osamaksu laskun loppuun maksamiseksi. Ottaa osamaksu käteisalennus on määritettävä ** Laske käteisalennukset osittainen maksujen ** asetuksella **Kyllä** - **huomioon Ostoreskontran parametrit** sivulla. 

Saat esimerkin mukaisesti 2 prosentin käteisalennuksen, jos lasku maksetaan 10 päivän kuluessa sen luonnista. Laskun arvoksi on kirjattu 100,00. Jos teet 49.00 10 päivän kuluessa maksun, kirjoita 49.00 on maksupäiväkirjaan. Kun selvität sen osittaisen maksun **Selvitä avoimet tapahtumat** sivun **1,00** tulee **käteisalennuksen summa ottamaan** kenttä. 

> [!NOTE] 
> Jos syötät osamaksu ja jättää koko laskutussumma **Täsmäytettävä summa** -kenttään **käteisalennuksen summa ottamaan** kenttä lasketaan automaattisesti, kun tapahtumat kirjataan.

## <a name="credit-notes-with-cash-discounts"></a>Hyvityslaskut ja käteisalennukset
Saatat palauttaa laskulla olevia nimikkeitä ja saada niistä hyvityslaskun. Jos käteisalennusta oli käytetty alkuperäisellä laskulla, voit vähentää alennuksen arvon ja saada palautuksen oikealle summalle. Jos ** Laske käteisalennukset hyvityslaskuille ** asetus **Kyllä** - **Ostoreskontran parametrit** sivulla, alennus lasketaan automaattisesti hyvityslaskun. 

Saat esimerkin mukaisesti 2 prosentin käteisalennuksen, jos lasku maksetaan 10 päivän kuluessa sen luonnista. Laskun kirjataan arvolla 100,00. Jos Palauta tavaroita ja vastaanottaa hyvityslaskun, voit syöttää hyvityslaskun alkuperäisen laskun 100,00 2 prosentin käteisalennus, joka on myös määritetty hyvityslaskun ja koko summan.  Kun tarkastelet hyvityslaskun **tapahtumat selvitetään** sivun **98.00** tulee **Täsmäytettävä summa** -kenttään ja **-2.00** tulee **käteisalennuksen summa** kenttä. Alennussumma kirjataan käteisalennustilille.

## <a name="overpaymentunderpayment-amounts"></a>Liika-/alisuorituksen summat
Voit suorittaa osamaksun, jonka jälkeen tilitettäväksi voi jäädä hyvin pieni summa. Toimittajan laskun summa on esimerkiksi 1 000,00 ja suoritat maksun summalle 999,90. Jos jäljelle jäävä summa on pienempi kuin liika-/alisuorituksen summa, joka on määritetty **Ostoreskontran parametrit** -sivulla, erotus kirjataan automaattisesti liika-/alisuorituksien kirjanpitotilille.


