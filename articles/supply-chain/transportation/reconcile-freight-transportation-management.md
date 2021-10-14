---
title: Rahdin täsmäytys kuljetustenhallinnassa
description: Tässä aiheessa käsitellään rahdin täsmäytysprosessia.
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a63bfd34860c6a7c34cbc526c6a621cbc9666efc
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574902"
---
# <a name="reconcile-freight-in-transportation-management"></a>Rahdin täsmäytys kuljetustenhallinnassa

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään rahdin täsmäytysprosessia.

Rahti voidaan täsmäyttää manuaalisesti tai se voidaan määrittää tapahtumaan automaattisesti. Jos haluat käyttää rahdin automaattista täsmäytystä, sinun on määritettävä päätarkistus, jossa voit määrittää ehdot määrittämään automaattisesti täsmäytettävät rahtilaskut.

## <a name="the-freight-reconciliation-process"></a>Rahdin täsmäytysprosessi

Kuljetusmaksut lasketaan hinnan laskennassa, joka on liitetty soveltuvaan rahdinkuljettajaan. Kun kuorma on vahvistettu, rahtilasku luodaan ja rahtitaksat siirretään siihen. Rahtitaksat jaetaan sekalaisina kuluina soveltuvaan lähdeasiakirjaan (ostotilaus, myyntitilaus ja/tai siirtotilaus) sen mukaan, mitä asetuksia tavallisen laskutusprosessin asetuksissa on käytetty. Rahdin täsmäytysprosessi voi alkaa heti, kun rahdinkuljettajan rahtilasku saadaan. Kyse voi olla sähköisestä laskusta tai paperilaskusta. Jos kyse on paperilaskusta, voit luoda sähköisen laskun käyttämällä rahtilaskua mallina.

[![Rahdin täsmäytysprosessi.](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>Manuaalinen täsmäytys

Jos olet täsmäyttämässä rahtia manuaalisesti, sinun on täsmäytettävä kukin laskun rivi rahtilaskun rivin tai laskutettavan kuorman rivien kanssa. Tämä täsmäytys tehdään **Rahtilaskun ja laskun täsmäytys** -sivulla. Jos laskurivin summa ei täsmää rahtilaskun summan kanssa, valitse erolle täsmäytyssyy. Jos täsmäytyksellä on useita syitä, voit jakaa täsmäyttämättömät summan niiden kesken. Täsmäytyksen syy määrittää, miten eriävät summat kirjataan kirjanpitoon. Kun koko laskutussumma on täsmäytetty, se lähetetään hyväksytyksi, jonka jälkeen kirjauskansio kirjataan. Seuraavassa kuvassa on esitetty, kuinka voit luoda rahtilaskun ja suorittaa rahdin täsmäytyksen.

[![Rahdin täsmäytystehtävät.](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)

## <a name="automatic-reconciliation"></a>Automaattinen täsmäytys

Jos haluat käyttää automaattista täsmäytystä, sinun on määritettävä täsmäytysaikataulu ja käytettävät laskut ja rahdinkuljettajat. Laskurivit ja rahtilaskut täsmäytetään päätarkistuksen ja rahtilaskun tyypin asetusten mukaan. Kun olet suorittanut automaattisen täsmäytyksen, sinun on käsiteltävä kaikki laskut, joita järjestelmä ei voi täsmäyttää. Nämä laskut on sitten käsiteltävä manuaalisesti ennen kaikkien laskujen kirjaamista maksettaviksi.

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a>Rahtikirjojen ja rahtilaskujen täsmäyttäminen automaattisella tai manuaalisella täsmäytyksellä

*Täsmäytys* on prosessi, jolla etsitään kutakin rahtilaskua vastaavat rahtikirjat. Se voidaan tehdä täsmäyttämällä laskurivit yksi kerrallaan (manuaalinen täsmäytys) tai täsmäyttämällä kaikki käytettävissä olevat laskut kerralla (automaattinen täsmäytys).

### <a name="auto-matching"></a>Automaattinen täsmäytys

Kun useita rahtilaskuja täsmäytetään samaan rahtikirjaan, automaattinen täsmäytysprosessi toimii seuraavasti:

1. Kaikki täsmäyttämättömät rahtilaskut lajitellaan summan perusteella suurin summa ensimmäisenä.
1. Rahtilaskut täsmäytetään yksi kerrallaan, kun rahtikirjassa ei ole jäljellä positiivista summaa.
1. Päätarkastuksen asetusten ja rahtilaskujen jäljellä olevan summan perusteella määritetään jäljellä oleva summa.

### <a name="manual-matching"></a>Manuaalinen täsmäytys

Kaikki rahtikirjat, joissa on positiivinen summa, voidaan täsmäyttää. Automaattisen täsmäytyksen tavoin käyttäjä voi täsmäyttää vain rahtilaskut, joissa on negatiivisia summia, rahtikirjoihin, joita ei ole kokonaisuudessaan täsmäytetty.

### <a name="example"></a>Esimerkki

Oletetaan, että rahtikirjan summa on 1 500 ja kyseiselle rahtikirjalle on luotu kolme rahtilaskua, jossa kullekin laskulle on yksi laskurivi ja seuraavat asetukset:

- Alkuperäinen rahtikirja (FB): Summa 1 500
- Lasku 1 (Inv1): Summa 1 000
- Lasku 2 (Inv2): Summa 600
- Lasku 3 (Inv3): Summa -100

#### <a name="automatic-matching-result"></a>Automaattisen täsmäytyksen tulos

Automaattinen täsmäytys suoritetaan seuraavassa järjestyksessä:

1. Kaikki rahtilaskut lajitellaan summan mukaiseen laskevaan järjestykseen: Lasku 1 -> Lasku 2 -> Lasku 3.
1. Lasku 1 ja rahtikirja täsmäytetään. Laskussa 1 on täsmäytetty 1 000 ja rahtikirjassa on vielä 500 täsmäyttämättä, joten tilaksi määritetään *Osittainen vastaavuus*.
1. Lasku 2 ja rahtikirja täsmäytetään. Laskussa 2 on täsmäytetty 500 ja rahtikirjassa on vielä 0 täsmäyttämättä, joten tilaksi määritetään *Täysi vastaavuus*.
1. Koska rahtikirja on kokonaan täsmäytetty, laskua 3 ei käsitellä.

#### <a name="manual-matching-result"></a>Manuaalisen täsmäytyksen tulos

Manuaalisen täsmäytyksen tulokset vaihtelevat täsmäytysjärjestyksen mukaan, kuten seuraavissa esimerkkitapauksissa.

##### <a name="manual-matching-case-1"></a>Manuaalinen täsmäytystapaus 1

Manuaalinen täsmäytys voidaan tehdä esimerkiksi seuraavasti:

1. Rahtikirja ja lasku 1 täsmäytetään. Rahtikirjassa on jäljellä summa 500, joten tilaksi määritetään *Osittainen vastaavuus*.
1. Lasku 2 ja rahtikirja täsmäytetään. Laskussa 2 on täsmäytetty 500 ja rahtikirjassa on vielä 0 täsmäyttämättä, joten tilaksi määritetään *Täysi vastaavuus*.
1. Kun lasku 3 täsmäytetään manuaalisesti, yhtään täsmäyttämätöntä rahtikirjaa ei löydy.

Tämä tapaus on käytännössä sama kuin automaattinen täsmäytys

##### <a name="manual-matching-case-2"></a>Manuaalinen täsmäytystapaus 2

Manuaalinen täsmäytys voidaan tehdä myös seuraavalla tavalla:

1. Lasku 3 ja rahtikirja täsmäytetään. Rahtikirjan jäljellä oleva summa on nyt 1 600, joka vastaa negatiivisen 100:n vähentämistä 1 500:sta. Sekä rahtikirjan että laskun 3 täsmäytetty määrä on -100.
1. Lasku 1 ja lasku 2 täsmäytetään rahtikirjaan peräkkäin. Rahtikirjan on kokonaan täsmäytetty.

Tämä esimerkki osoittaa, että negatiivisia summia sisältävien rahtilaskujen täsmäyttäminen on tehtävä vain manuaalisesti. Näin varmistetaan, että negatiivisia summia sisältävät rahtilaskut voidaan aina täsmäyttää rahtikirjaan, jota ei ole kokonaan täsmäytetty, koska tällä tavoin täsmäytysjärjestystä voidaan hallita.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]