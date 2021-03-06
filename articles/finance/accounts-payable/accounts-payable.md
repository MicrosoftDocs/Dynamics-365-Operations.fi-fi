---
title: Ostoreskontran aloitussivu
description: Tässä aiheessa on yleiskuvaus ostoreskontrasta.
author: ShylaThompson
ms.date: 02/15/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 21901
ms.assetid: 1e4c2ac4-077b-4678-8733-5cec8f6ff659
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 62e075fc26ee2e183cd859c5ec2c90faa3bfe3ab
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897007"
---
# <a name="accounts-payable-home-page"></a>Ostoreskontran aloitussivu

[!include [banner](../includes/banner.md)]

Tässä aiheessa on yleiskuvaus ostoreskontrasta. 

Voit syöttää toimittajan laskut manuaalisesti tai vastaanottaa ne sähköisesti tietoyksikön kautta. Sen jälkeen kun laskut on syötetty tai vastaanotettu, voit tarkistaa ja hyväksyä laskut laskujen hyväksymiskirjauskansion avulla tai **Toimittajan lasku** -sivulla. Voit automatisoida tarkistusprosessin laskun täsmäytyksen, toimittajan laskutuskäytäntöjen ja työnkulun avulla. Tämän jälkeen tietyt ehdot täyttävät laskut hyväksytään automaattisesti ja muut laskut merkitään valtuutetun käyttäjän tarkistettavaksi.

**Liiketoimintaprosessit**

[![Liiketoimintaprosessikaavio](./media/AP-process.PNG)](./media/AP-process.PNG)

## <a name="set-up-accounts-payable"></a>Ostoreskontran asetukset

Määritä toimittajaryhmät, toimittajat, kirjausprofiilit ja erilaiset maksuvaihtoehdot sekä toimittajia, kuluja, toimituksia ja kohteita sekä velkakirjoja ja muun tyyppisiä ostoreskontran tietoja koskevat parametrit. 

[Ostoreskontran määrittäminen – yleiskatsaus](accounts-payable-overview.md)

[Toimittajan laskujen kirjanpidolliset jaot ja alareskontran kirjauskansioviennit](accounting-distributions-subledger-journal-entries-vendor-invoices.md) 

[Ulkomaanvaluutan uudelleenarvostus osto- ja myyntireskontrassa](../cash-bank-management/foreign-currency-revaluation-accounts-payable-accounts-receivable.md)

## <a name="configure-vendor-invoices"></a>Toimittajan laskujen määrittäminen

Ostoreskontran avulla voit tarkastella laskuja ja toimittajille suoritettavia maksuja.

[Ostoreskontran laskujen täsmäytys – yleiskatsaus](accounts-payable-invoice-matching.md)

[Toimittajan kirjausprofiilit](vendor-posting-profiles.md)

[Ostoreskontran laskujen täsmäytyksen vahvistuksen asetukset](tasks/set-up-accounts-payable-invoice-matching-validation.md)

[Kolmisuuntaiset vastaavuuskäytännöt](three-way-matching-policies.md)

[Laskujen täsmäytys ja konsernin sisäiset ostotilaukset](invoice-matching-intercompany-purchase-orders.md)

[Ristiriitojen selvittäminen laskusummien täsmäytyksen aikana – yleiskatsaus](resolve-invoice-totals-invoice-matching-discrepancies.md)

[Toimittajan laskujen ja laskujen hyväksynnän kirjauskansioiden oletusvastatilit](default-offset-accounts-vendor-invoice-journals.md)

[Mobiililaskujen hyväksynnät](mobile-invoice-approvals.md)

[Toimittajayhteistyön laskutustyötila](vendor-portal-invoicing-workspace.md)

[Toimittajan laskuautomaatio](vendor-invoice-automation.md)

## <a name="configure-vendor-payments"></a>Toimittajan maksujen määrittäminen 

Määritä järjestelmässä määritetty maksutyyppi, kuten sekki, sähköinen maksu tai velkakirja, mille tahansa käyttäjän määrittämälle maksutavalle. Maksutyypit ovat valinnaisia, mutta niiden avulla on helppo tehdä sähköisten maksujen oikeellisuustarkistus ja määrittää nopeasti, mitä maksutyyppiä maksu käyttää. 

[Toimittajan maksujen työtila](vendor-payments-workspace.md)

[Toimittajan maksulisien määritys](tasks/define-vendor-payment-fees.md)

[Toimittajan maksuehtojen määritys](tasks/define-vendor-payment-terms.md)

[Positive pay -yleiskatsaus](positive-pay-overview.md)

[Positive pay -tiedostojen asetukset ja luonti](set-up-generate-positive-pay-files.md)

[Toimittajamaksujen luominen maksuehdotuksen avulla](create-vendor-payments-payment-proposal.md)

[Toimittajan maksut osasummalle](vendor-payments-partial-amount.md)

[Alennuksen käyttäminen, kun alennuksen summa on suurempi kuin toimittajan maksulle laskettu alennus](take-discount-more-calculated-discount-vendor-payment.md)

[Käteisalennuksen käyttäminen käteisalennuskauden ulkopuolella](take-cash-discount-outside-cash-discount-timeframe.md)

[Toimittajan näytesekkien sähköinen raportointi](electronic-reporting-sample-vendor-checks.md)

[Käänteinen toimittajamaksu](reverse-vendor-payment.md)

[Ennakkomaksulaskujen ja ennakkomaksujen vertailu](prepayments-invoices-vs-prepayments.md)

[Ostoreskontran keskitetyt maksut](centralized-payments-accounts-payable.md)

## <a name="settlements"></a>Tilitykset

Seuraavissa ohjeaiheissa on tietoa tilityksistä. Tilitys tarkoittaa maksujen tilittämistä laskuihin. 

[Tilityksen määrittäminen](../cash-bank-management/configure-settlement.md)

[Toimittajan osamaksun tilittäminen ennen alennuspäivämäärää, kun viimeinen maksu suoritetaan alennuspäivämäärän jälkeen](settle-partial-vendor-payment-before-discount-or-final-payment-after.md)

[Toimittajan hyvityslaskujen alennuksia sisältävän toimittajan osamaksun tilittäminen](settle-partial-vendor-payment-discounts-vendor-credit-notes.md)

[Useita alennuskausia sisältävän toimittajan osamaksun tilittäminen](settle-partial-vendor-payment-multiple-discount-periods.md)

[Toimittajan osamaksun ja viimeisen maksun tilittäminen kokonaan ennen alennuspäivämäärää](settle-partial-vendor-payment-or-final-payment-before-discount.md)

[Yksi tosite useille asiakas- tai toimittajatietueille](single-voucher-multiple-customer-vendor-records.md)



### <a name="additional-resources"></a>Lisäresurssit

#### <a name="whats-new-and-in-development"></a>Uudet ja kehitteillä olevat toiminnot

Siirry [Microsoft Dynamics 365:n julkaisusuunnitelmiin](/dynamics365/release-plans/), kun haluat nähdä uudet suunnitteilla olevat toiminnot. 

#### <a name="blogs"></a>Blogit

[Microsoft Dynamics 365 -blogissa](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) ja [taloushallinnon Microsoft Dynamics 365 Finance -blogissa](https://community.dynamics.com/365/financeandoperations/b/financials) esitetään ostoreskontraa ja muita ratkaisuja koskevia mielipiteitä, uutisia ja muita tietoja.

[Microsoft Dynamics Operations -kumppaniyhteisön blogista](https://community.dynamics.com/partner/b/operationspartnercommunityblog) Microsoft Dynamics -kumppanit saavat keskitetysti tietoja Dynamics 365 -sovelluksen uutuuksista ja suosituista aiheista.

#### <a name="community-blogs"></a>Yhteisöblogit

[Ostovelkojen hallinta Dynamics 365 Finance -sovelluksessa](https://financefunction.tech/2019/02/15/how-to-manage-payables-in-dynamics-365-for-finance-and-operations)

#### <a name="task-guides"></a>Tehtäväoppaat
Sovelluksen tehtäväoppaissa on lisäohjeita. Voit avata tehtäväoppaan napsauttamalla Ohje-painiketta millä tahansa sivulla.

#### <a name="videos"></a>Videot

Tutustu [Microsoft Dynamics 365 YouTube -kanavan](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ) ohjevideoihin.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]