---
title: Asiakkaan maksut osasummalla
description: "Joskus asiakkaiden maksama summa on pienempi kuin laskun summa. Tässä artikkelissa on kuvaus erilaisista toimintavaihtoehdoista tällaisessa tilanteessa. Käytettävissä olevat vaihtoehdot määräytyvät liiketoiminnan vaatimusten ja konfiguraation mukaan."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13011
ms.assetid: 20423a2d-6997-4e1c-a596-a77016600071
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 795d13a07065a125a750970beaff85b59307f623
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="customer-payments-for-a-partial-amount"></a>Asiakkaan maksut osasummalla

[!include[banner](../includes/banner.md)]


Joskus asiakkaiden maksama summa on pienempi kuin laskun summa. Tässä artikkelissa on kuvaus erilaisista toimintavaihtoehdoista tällaisessa tilanteessa. Käytettävissä olevat vaihtoehdot määräytyvät liiketoiminnan vaatimusten ja konfiguraation mukaan.

<a name="partial-payment-with-no-discount"></a>Osamaksu ilman alennusta
--------------------------------

Asiakkaat voivat suorittaa osamaksun, koska heillä ei ole tarpeeksi käteisvaroja maksaakseen laskun kokonaisuudessaan, tai koska jostakin laskunimikkeestä on erimielisyyttä. Tässä tilanteessa laskun voi osatäsmäyttää maksuun. Lasku jää avoimeksi ja sillä näkyy saldo.

## <a name="discount-amounts"></a>Alennussummat
Voit tarjota asiakkaillesi käteisalennuksen, jos he maksavat laskun ennen eräpäivää. Voit syöttää esimerkiksi laskun summaksi 100,00, jolle määritetään 2 prosentin käteisalennus, jos lasku maksetaan 10 päivän kuluessa. Maksuehto on 30 päivää. Jos saat maksun summalla 98,00 10 päivän kuluessa, kirjaat maksuksi 98,00. Kun lasku sitten merkitään täsmäytettäväksi, käteisalennus otetaan huomioon automaattisesti.

## <a name="partial-payments-with-cash-discounts"></a>Osamaksut käteisalennuksella
Kun asiakas suorittaa osamaksun, suunnitelmana voi olla suorittaa toinen osamaksu laskun loppuun maksamiseksi. Jos haluat vastaanottaa käteisalennuksen osittaiselta maksulta, sinun on määritettävä **Laske käteisalennukset osamaksuille** -asetukseksi **Kyllä** **Myyntireskontran parametrit** -sivulla. 

Voit esimerkiksi tarjota 2 prosentin käteisalennuksen, jos lasku maksetaan 10 päivän kuluessa. Laskun arvoksi on kirjattu 100,00. Jos saat maksun summalla 49,00 10 päivän kuluessa, kirjaat maksuksi 49,00 maksujen kirjauskansioon. Kun täsmäytät osamaksun **Selvitä tapahtumat** -sivulla, **1,00** näkyy **Käytettävä käteisalennussumma** -kentässä. Alennussumma kirjataan käteisalennustilille. 

> [!NOTE] 
> Jos kirjaat osamaksun ja jätät koko laskusumman **Täsmäytettävä summa** -kenttään, **Käytettävä käteisalennussumma** -kenttä lasketaan uudelleen automaattisesti, kun kirjaat tapahtumat.

## <a name="credit-notes-with-discounts"></a>Hyvityslaskut ja alennukset
Jos asiakkaat palauttavat laskulla olevia nimikkeitä, voit antaa heille hyvityslaskun. Jos alkuperäiselle laskulle oli annettu käteisalennus, asiakkaan hyvityslaskun summa tulisi olla asiakkaan saaman käteisalennuksen nettosumma. Jos **Laske käteisalennukset hyvityslaskuille** -asetukseksi on määritetty **Kyllä** **Myyntireskontran parametrit** -sivulla, alennus lasketaan automaattisesti hyvityslaskulle. 

Olet esimerkiksi voinut tarjota maksuehdon, jossa tarjotaan 2 prosentin käteisalennus, jos lasku maksetaan 10 päivän kuluessa. Olet kirjannut laskun summalla 100,00, ja asiakas on käyttänyt käteisalennuksensa. Jos asiakas palauttaa tuotteen, ja annat hänelle hyvityslaskun, voit kirjata hyvityslaskun summalla -100,00. Kun tarkastelet hyvityslaskua **Tilitä avoimet tapahtumat** -sivulla,**98,00** näkyy **Tilitettävä summa** -kentässä ja **-2,00** näkyy **Käteisalennuksen summa** -kentässä. Alennussumma kirjataan käteisalennustilille.

## <a name="overpaymentunderpayment-amounts"></a>Liika-/alisuorituksen summat
Kun asiakas suorittaa maksun, jäljelle voi jäädä hyvin pieniä, tilitettäviä summia. Voit esimerkiksi laskuttaa asiakkaalta 1 000,00, ja asiakas maksaa 999,90. Jos jäljelle jäävä summa on pienempi kuin liika-/alisuorituksen summa, joka on määritetty **Myyntireskontran parametrit** -sivulla, erotus kirjataan automaattisesti liika-/alisuorituksien kirjanpitotilille.

## <a name="full-settlement"></a>Täysi tilitys
Asiakkaat voivat suorittaa osittaisen maksun, jossa jäljellä oleva summaa ei makseta, mutta se on suurempi kuin liian vähän maksettu summa, joka on määritetty **Ostoreskontran parametrit** -sivulla. Jos haluat merkitä laskun täysin selvitetyksi, voit käyttää **Täysi tilitys** -asetusta **Selvitä tapahtumat** -sivulla. (Voit ottaa täyden tilityksen toiminnon käyttöön konfigurointiavaimen avulla.) Esimerkiksi, lasku kirjataan summalle 1 000,00, ja asiakas suorittaa 990,00 arvoisen maksun. Olette sopineet, että asiakkaan ei tarvitse maksaa jäljellä olevaa summaa 10,00. Kun merkitset laskun selvitykseen, voit myös merkitä **Täysi tilitys**. Lasku merkitään siten täysin maksetuksi. 10,00:n alijäämä kirjataan käteisalennuksen tilille muuna käteisalennussummana.




