---
title: Hintojen, alennusten, sopimusten ja ostohyvitysten vianmääritys
description: Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita hintojen, alennusten, sopimusten ja ostohyvitysten käytössä voi esiintyä.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 14fdddabde7739cbf9ba0fcee0fa0b8b816e74dd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007363"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a>Hintojen, alennusten, sopimusten ja ostohyvitysten vianmääritys

Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita hintojen, alennusten, sopimusten ja ostohyvitysten käytössä voi esiintyä.

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a>En saa linkitettyä ostotilausta ostotilausriviin, kun ostotilaus on luotu.

Ostosopimus on yhdistettävä ostotilaukseen, kun ostotilaus luodaan. Muussa tapauksessa ostotilausrivejä ei voi liittää ostosopimusriveihin.

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>Mikä tarkistus tuottaa sanoman "Päivitä manuaalisesti syötetyt hinnat ja alennukset tai ulkoinen asiakirja"?

Kun muutat lähetyspäivämäärää, näyttöön voi tulla sanoma "Päivitä manuaalisesti syötetyt hinnat ja alennukset tai ulkoinen asiakirja" Saat tämän sanoman, koska jos lähetyspäivämäärää muutetaan, muu kauppa- tai myyntisopimus saattaa tulla voimaan ja aiheuttaa hinnanmuutoksen. Toimituspäivämäärän muuttaminen voi vaikuttaa myös fyysisen varastoinnin aikatauluihin ja liittyviin tietoihin.

Sanoma luodaan, kun jokin päivämääristä tai muista parametreista muuttuu. Sanoman tarkoitus on varmistaa, että olet tietoinen hinnanmuutoksista, joita voi aiheutua kyseisistä muutoksista.

Sanoma on kauppasopimuksen arviointi (TAE) -kehote. Täydellinen kuvaus [Kauppasopimuksen arviointikäytännöt](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>Ostotilauksen kuitti ei sisällä kaikkia maksuja.

### <a name="reproduce-the-issue"></a>Ongelman toistaminen

Seuraavassa esitetään yksi tapa ongelman toistamiseen.

1. Varmista **Osto- ja hankintaparametrit** -sivun **Toimitus**-välilehdessä, että **Luo maksuja tuotteen vastaanottamisen yhteyteen** -asetuksen arvona on *Kyllä*.
1. Luo ostotilaus, joka sisältää maksuja.
1. Vahvista ostotilaus.
1. Vastaanota ostotilaus.
1. Tarkista kuitin kokonaissumma ja vertaa sitä odotettuun summaan.
1. Huomaa, että kaikki maksut eivät sisälly ostotilauksen kuittiin.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Ratkaisu riippuu siitä, miten muut maksut on määritetty. Lisätietoja muiden maksujen määrittämisestä vastaamaan tarpeitasi on seuraavassa blogikirjoituksessa: [Kirjaa muut kulut tuotteen vastaanoton yhteydessä](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a>Kauppasopimuksen hintoja ja alennuksia ei käytetä myynti- tai ostotilausriveillä, jotka tuodaan tiedonhallinnan kautta.

### <a name="issue-description"></a>Ongelman kuvaus

Myynti- tai ostotilausriveissä käytettäviä kauppasopimuksia ei käytetä riveillä, jotka tuodaan tiedonhallinnan kautta. Samoja kauppasopimuksia käytetään kuitenkin manuaalisesti luoduissa myynti- tai ostotilausriveissä.

### <a name="reason-for-the-issue"></a>Ongelman syy

Jos tiedonhallinnan kautta tuotavat ostotilausrivit sisältävät jo hintatietoja, kauppasopimusta ei arvioida uudelleen kyseisten rivien osalta. Jos riville on määritetty **Rivialennusprosentti** tai jokin hinnan ja alennuksen arvoista, kauppasopimuksia ei etsitä kyseiselle riville.

### <a name="issue-workaround"></a>Ongelman kiertotapa

Tämä toiminta on odotettavissa, ja se on samanlainen sekä myynti- että ostotilauksissa.

Kiertotapana voit tuoda ostotilausrivit määrittämättä hintatietoja. Tällöin sovelletaan kauppasopimuksia ja ostotilausrivit päivitetään määritettyjen kauppasopimusten perusteella.

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>Toimittajan ostohyvitystä ei kerry laskujen perusteella.

### <a name="issue-description"></a>Ongelman kuvaus

Jos kirjatuilla laskuilla on eri eräpäivät, laskut eivät näy toimittajan ostohyvityksissä, jotka on luotu niiden perusteella.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Eräpäivää ei tarkoituksella oteta huomioon toimittajan ostohyvitystä laskettaessa. Harkitse järjestelmän mukauttamista siten, että eräpäivä ja suhde ovat ilmeisempiä todellisen toimittajan ostohyvityksen osalta.

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>Ostotilausten yksikköhintoja ei lasketa yksikkömuunnoksen perusteella.

### <a name="issue-description"></a>Ongelman kuvaus

Kun yksikköä muutetaan ostotilauksessa, kauppasopimuksen hintoja ei lasketa uudelleen yksikkömuunnoksen määritysten mukaisesti.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Hinnat perustuvat aina kauppasopimuksiin (tai muihin järjestelmän hinta-asetuksiin, kuten myyntisopimuksiin tai nimikkeiden hintoihin), ja ne on määritetään yksikkökohtaisesti.

Jos yksikköä muutetaan tilausrivillä, järjestelmä hakee hinnan uudelle nimikkeelle ja soveltaa sitä. Jos yksikölle ei löydy hintaa, järjestelmä ei käytä hintaa. Yksikkömuunnosta ei voi käyttää hinnan uudelleenlaskemiseen toiseen yksikköön. Teoriassa yhden laatikon hinta ei ehkä vastaa kymmentä kertaa yhden laatikon hintaa.

### <a name="issue-workaround"></a>Ongelman kiertotapa

Yksi tapa kiertää tämä ongelma on varmistaa, että nimikkeen tilausriveillä käytetään odottamiasi yksiköitä koskevia kauppasopimuksia.

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a>Kauppasopimuksissa esiintyy valuutanmuunto-ongelmia.

Kauppasopimusten hintoja ei lasketa uudelleen valuutan mukaan, kun valuutta on ostotilauksessa eri.

*Yleinen valuutta* -toiminnon avulla voit määrittää hinnat ja alennukset vain yhdessä valuutassa. Tällöin voit muuntaa muihin valuuttoihin tarpeen mukaan. Lisäksi kun muunnos on tehty, toiminto voi automaattisesti käyttää taktista pyöristystä.

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a>Kun avaan ostosopimussivun rivinäkymätilassa, en voi mukauttaa sivua lisäämällä hintayksikön kenttää rivin yhteenvetoon.

Osaa sopimuskehyksen yhteisiä kenttiä ei voi sisällyttää yksilöinteihin. Tämä rajoitus ilmenee käytettävän tietomallin vuoksi. Siksi et voi mukauttaa **Hintayksikkö**-kenttää.

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a>Ostosopimuksen yläraja ei ole päde ostoehdotukseen.

### <a name="issue-description"></a>Ongelman kuvaus

Kun ostoehdotus linkitetään ostosopimukseen, ostosopimuksen yläraja ei päde ostoehdotukseen. Oletushintatiedot on syötetty oikein, mutta ostoehdotuksella voit tilata ostosopimuksen ylärajan ylittävän määrän.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tämä toiminta on tarkoituksellista. Koska ehdotuksia ei aina hyväksytä, määrää tai summaa ei pitäisi varata ostosopimuksessa. Siksi ostosopimuksen ylärajaa ei saavuteta.

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a>Kauppasopimuksia voi luoda hylätyistä tarjouspyynnöistä. Siksi järjestelmä ei estä kauppasopimusten kirjauskansioiden luomista, jos tarjouspyyntöriviä ei ole hyväksytty.

Voit luoda kauppasopimuksia mille tahansa tarjouspyynnön vastaukselle riippumatta siitä, hyväksyttiinkö vai hylättiinkö vastaus. Lisätietoja: [Tarjouspyyntöjen yleiskatsaus](request-quotations.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]