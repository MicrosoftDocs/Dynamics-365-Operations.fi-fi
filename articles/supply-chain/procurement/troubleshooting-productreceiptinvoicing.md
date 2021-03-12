---
title: Tuotteiden vastaanottojen ja laskutuksen vianmääritys
description: Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita tuotteiden vastaanottamisessa ja laskutuksessa voi esiintyä.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 22b1abec0c6dd5f571e604c5c07379b397b8bdaa
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999050"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a>Tuotteiden vastaanottojen ja laskutuksen vianmääritys

Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita tuotteiden vastaanottamisessa ja laskutuksessa voi esiintyä.

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>Voin kirjata vain yhden laskun ostotilausriville, jolla on luokkaperusteisia nimikkeitä.

Määrä on pakollinen, jos haluat kirjata laskuja. Siten, jos rivin kokonaismäärä on laskutettu vain osittaisen summan osalta, et voi laskuttaa jäljellä olevaa summaa toisella laskulla.

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>Saan "Kohdeviitettä ei määritetty" -virheen ostotilauksen vahvistuksen aikana tai "Kutsun kohde on aiheuttanut poikkeuksen" -poikkeus esiintyy toimittajan laskun julkaisemisen yhteydessä.

Tämä ongelma voi esiintyä, kun ostotilausten jaoissa on epäjohdonmukaisuuksia.

Voit poistaa tämän ongelman eston ja palauttaa ostotilauksen *Luonnos* siirtymällä kohtaan **Ostot ja hankinnat \> Säännölliset tehtävät \> Tyhjennys \> Ostotilauksen jaon palautus**. Lisä tietoja on seuraavassa blogikirjoituksessa: [Ostotilausten jakovirheiden korjaaminen Dynamics 365 Supply Chain Managementissa](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>En saa yhdistettyä useita tuotteiden vastaanottoja yhdeksi ostotilaukseksi.

Useita tuotteiden vastaanottoja ei voi yhdistää yhdeksi ostotilaukseksi, jos eri tuotteiden vastaanottojen riveillä on eri kirjanpitopäivämäärät.

Aiemmissa Microsoft Dynamics 365 Supply Chain Managementin versioissa yhdistäminen sallittiin tässä tilanteessa. Käytäntö on kuitenkin altis virheille. Luotujen ostotilausrivien kirjanpitopäivämäärän ei pitäisi poiketa niiden tuotteen vastaanoton rivien kirjanpitopäivämäärästä, joiden perusteella ostotilausrivit luotiin. (Osto tilausrivien kirjanpitopäivämäärä vastaa ostotilauksen otsikon kirjanpitopäivämäärää.) Tämän vuoksi useiden tuotteiden vastaanottojen yhdistäminen yhdeksi ostotilaukseksi ei ole enää sallittua.

Kirjanpitopäivämäärää käytetään esimerkiksi budjettivarausten ja varausten osalta. Siksi se on säilytettävä siirryttäessä tuotteen vastaanotosta ostotilaukseen.

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a>Kun tuotteen vastaanotot peruutetaan, tapahtumat voidaan kirjata keskeytetylle kirjanpitotilille.

### <a name="issue-description"></a>Ongelman kuvaus

Jos tuotteen vastaanotto peruutetaan, järjestelmä sallii tapahtumien kirjaamisen keskeytetyille kirjanpitotileille, vaikka päätilit olisivat keskeytettynä.

### <a name="reproduce-the-issue"></a>Ongelman toistaminen

Seuraavassa esitetään yksi tapa ongelman toistamiseen.

1. Varmista **Ostoreskontran parametrit** -sivun **Yleiset**-välilehdessä, että **Kirjaa vastaanotto kirjanpitoon** -asetuksen arvona on *Kyllä*.
1. Luo ostotilaus ja lisää tilausrivi, jossa tietyn tuotteen määrä on *1 000*.
1. Vahvista ostotilaus.
1. Kirjaa tuotteen vastaanotto ja tarkista tositteet.
1. Keskeytä tarvittavat päätilit eli *200140* ja *140200*.
1. Peruuta kirjattu tuotteen vastaanotto.
1. Huomaa, että tapahtumat voidaan kirjata keskeytetyille kirjanpitotileille.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tapahtumat voidaan kirjata keskeytetyille kirjanpitotileille, kun tuotteiden vastaanotot peruutetaan, koska tämä toimintatapa mahdollistaa oikeelliset kirjaukset.

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a>Tuotteen vastaanoton tositenumero käytettään, vaikka tuotteen vastaanoton aikana ei luotaisi rahoitustositetta.

Jos **Jaksota ostovelka tuotteen vastaanotossa** -asetuksen arvoksi on määritetty *Ei* nimikemalliryhmän osalta, kirjanpitoon ei tehdä kirjauksia. Fyysinen tapahtuma kirjataan kuitenkin kirjanpitotarkoituksia varten alikirjanpitoon, ja tapahtuma vaatii tositenumeron. Tämä tositenumero on se tositenumero, johon viitataan varastotapahtumissa.

On suositeltavaa määrittää **Jaksota ostovelka tuotteen vastaanotossa** -asetuksen arvoksi *Kyllä*, kuten seuraavassa blogikirjoituksessa kuvataan: [Muiden kulujen kirjaaminen tuotteen vastaanoton hetkellä](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>Kirjaa kirjanpidon veloitustilille -asetus ei ole käytössä.

### <a name="issue-description"></a>Ongelman kuvaus

Tämä ongelma ilmenee, kun ostotilaus laskutetaan ja **Kirjaa kirjanpidon veloitustilille** -asetuksen arvona on *Kyllä* **Ostoreskontran parametrit** -sivun **Lasku**-välilehdessä.

### <a name="reproduce-the-issue"></a>Ongelman toistaminen

Seuraavassa esitetään yksi tapa ongelman toistamiseen.

1. Valitse **Ostoreskontra \> Asetukset \> Ostoreskontran parametrit**.
1. Määritä **Lasku**-välilehden **Kirjaa kirjanpidon veloitustilille** -asetukseksi *Kyllä*.
1. Siirry kohtaan **Varastonhallinta \> Määritys \> Kirjaus \> Kirjaus**.
1. Varmista **Ostotilaus**-välilehdellä, että olet poistanut kaikki tuotteen ostomenojen rivit.
1. Valitse **Ostoreskontra \> Ostotilaukset \> Kaikki ostotilaukset**.
1. Luo ostotilaus. Valitse **Toimittajatili**-kentässä *1001 Acme-toimistotarviketta*.
1. Lisää ostotilausrivi, jossa on seuraavat asetukset:

    - **Nimikenumero:** *D0011 Laserprojektori*
    - **Toimipaikka:** *1*
    - **Varasto**: *11*
    - **Määrä** *4*

1. Valitse toimintoruudun **osta**-välilehden **Toimi**-ryhmässä **Vahvista**.
1. Valitse toimintoruudun **Vastaanota**-välilehden **Luo**-ryhmässä **Tuotteen vastaanotto**.
1. Syötä **Tuotteen vastaanottokirjaus** -valintaikkunan **Tuotteen vastaanotto** -kenttään satunnainen numero ja valitse **OK**.
1. Valitse Toimintoruudun **Laskutus**-välilehden **Luo**-ryhmässä **Lasku**.
1. Syötä **Numero**-kenttään satunnainen numero laskunumeroksi.
1. Päivitä täsmäytyksen tila ja kirjaa.
1. Huomaa, näkyviin tulee nyt seuraava virhe, kun luot laskun ostotilauksesta: "Tuotteen ostomenot -tapahtumatyypin tilinumeroa ei ole olemassa".

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tämä määräytyy laskujen ja laskuryhmien parametriasetusten perusteella. Lisä tietoja on seuraavassa blogikirjoituksessa: [Ostomenojen kirjaaminen ja varastotilanteen vaihtelut](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).
