---
title: "Toimittajayhteistyö asiakkaiden kanssa"
description: "Tässä aiheessa kuvataan, miten voit käyttää ostotilauksia toimittajayhteistyön avulla Finance and Operations -ympäristössä ja valvoa tavaralähetysvarastoa."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 6119f1c85b68e6ed5dce01a266c4e681dfc4cd30
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="vendor-collaboration-with-customers"></a>Toimittajayhteistyö asiakkaiden kanssa

[!include[banner](../includes/banner.md)]


Tässä aiheessa kuvataan, miten voit käyttää ostotilauksia toimittajayhteistyön avulla Finance and Operations -ympäristössä ja valvoa tavaralähetysvarastoa.

Tässä aiheessa kuvataan, miten voit tehdä yhteistyötä ulkoisten toimittajien kanssa Microsoft Finance and Operations -ympäristössä. Aihe sisältää tietoja ostotilausten seuraamisesta ja niihin vastaamisesta sekä tavaralähetysvaraston valvonnasta. Toimittajayhteistyötä on myös mahdollista käyttää laskujen käsittelyyn. Saat lisätietoja kohdasta [Toimittajayhteistyön laskutustyötila](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md).

## <a name="working-with-purchase-orders"></a>Ostotilausten käsittely
**Ostotilauksen vahvistus** -työtilan avulla voit vastata ostotilauksiin, jotka on lähetetty sinulle tarkistusta varten. Voit myös tarkastella ostotilauksen tietoja, jotka odottavat toimenpidettä asiakkaalta, ja ostotilauksia jotka on vahvistettu mutta edelleen avoimia. **Ostotilauksen vahvistus** -työtilassa on kolme luetteloa:

-   **Tarkistettavat ostotilaukset**: luettelossa näkyvät kaikki sinulle lähetetyt ostotilaukset, jotka odottavat vastaustasi. Kun olet vastannut, ostotilaus poistuu luettelosta. Jos asiakas lähettää uuden version ostotilauksesta ennen kuin olet vastannut edelliseen, ainoastaan uusin versio näkyy luettelossa.
-   **Odottaa asiakkaan toimintoa**: luettelossa voit selata ostotilauksia, joihin olet vastannut mutta joita asiakas ei ole vielä vahvistanut. Jos olet hyväksynyt ostotilauksen, voit valvoa sitä luettelossa, kunnes tilaksi muuttuu **vahvistettu**. Jos hylkäsit ostotilauksen tai hyväksyit sen muutosten kera, voit valvoa ostotilausta luettelossa, kunnes asiakas lähettää uuden version.
-   **Avoimet vahvistetut ostotilaukset**: luettelo sisältää kaikki tililläsi olevat ostotilaukset, joiden tila on **vahvistettu**. Kun kaikki ostotilausta vastaavat tuotteet tai palvelut on vastaanotettu, ostotilaus poistuu luettelosta.

Seuraavassa luettelossa on neljä sivua, joiden avulla voit käsitellä ostotilauksia. Kahden sivun tiedot ovat samat kuin työtilan luetteloissa:

-   **Tarkistettavat ostotilaukset** (katso edellä)
-   **Ostotilausten toimittajan vahvistushistoria**: sivu sisältää kaikki ostotilaukset ja niiden versiot, jotka on lähetetty toimittajalle, ja kaikki vastaukset, jotka on palautettu toimittajalta.
-   **Avoimet vahvistetut ostotilaukset** (katso edellä)
-   **Kaikki vahvistetut ostotilaukset** sivu sisältää kaikki vahvistetut ostotilaukset, mukaan lukien ne joiden tuotteet tai palvelut on vastaanotettu. Tämän luettelon avulla voit valvoa, mitkä ostotilaukset voidaan laskuttaa.

### <a name="responding-to-purchase-orders"></a>Ostotilauksiin vastaaminen

Asiakkaan tarkastettaviksi lähettämät ostotilaukset näkyvät **Ostotilauksen vahvistus** -työtilassa ja **Tarkistettavat ostotilaukset** -sivulla. Kun olet avannut ostotilauksen, voit hyväksyä, hylätä tai hyväksyä ostotilauksen muutosten kera. Ostotilauksen otsikossa tai yksittäisillä riveillä voi olla liitteitä. Voit liittää tietoja vastaukseesi ostotilauksen otsikkoon tai yksittäisille riveille. Voit esimerkiksi ehdottaa korvaavaa nimikettä yhdelle riville. Voit esikatsella ja tulostaa ostotilauksen PDF-muodossa **Esikatselu/tulostus** -asetuksella. Voit piilottaa tai näyttää seuraavat dimensiosarakkeet **Näytä dimensiot** -toiminnolla: toimipaikka, varasto, väri, koko, malli, konfiguraatio. Käytettäessä **Hyväksy muutosten kera** -vaihtoehtoa, voit hyväksyä tai hylätä yksittäisiä rivejä. Voit tehdä seuraavia muutoksia riveille:

-   Päivämäärien tai määrien muuttaminen. Jos haluat päivittää vahvistetun toimituspäivän kaikilla riveillä, valitse **Päivitä toimituspäivä** vaihtoehto ostotilauksen otsikossa.
-   Rivien jakaminen eri toimituspäivämäärille tai määrille
-   Korvaa nimike. Tämä tehdään kirjoittamalla nimikkeen kuvaus ja nimiketunnus **Ulkoinen** -kenttään **Rivin tiedot** -osaan.

Et voi muuttaa hinnoittelutietoja etkä maksuja, mutta voi tehdä muutosehdotuksia niihin huomautuksissa. Jos asiakas lähettää sinulle uuden ostotilauksen version, sen loppuliite osoittaa, että kyseessä on aiemmin lähetetyn ostotilauksen muokattu versio. **Ostotilausten toimittajan vahvistushistoria** -sivulla voit seurata jokaisen tilauksen historiatietoja.

## <a name="monitoring-consignment-inventory"></a>Tavaralähetysvaraston valvonta
Jos käytät tavaralähetysvarastoa, voit käyttää toimittajayhteistyöliittymää tietojen tarkasteluun seuraavilla sivuilla:

-   **Tavaralähetysvarastoa pienentävät ostotilaukset** - Tavaralähetysvaraston ostotilaukset luodaan, kun varaston omistajuus vaihtuu asiakkaalle. Nämä tavaralähetyksen ostotilaukset näytetään vain **Tavaralähetysvarastoa vähentävät ostotilaukset** -sivulla. Ne eivät sisälly **Kaikki vahvistetut ostotilaukset** -sivulle.
-   **Tavaralähetysvarastosta vastaanotetut tuotteet**: sivulla luetteloidaan kaikki tapahtumat, joissa tuotteiden omistajuus siirretään varastoa käyttävälle yritykselle. Näiden tietojen avulla voit laskuttaa asiakasta.
-   **Käytettävissä oleva tavaralähetysvarasto**: Tällä sivulla näkyy yrityksesi omistama käytettävissä oleva tavaralähetysvarasto, joka on käytettävissä asiakkaan varastossa.


<a name="see-also"></a>Lisätietoja
--------

[Toimittajayhteistyön käyttäjien hallinta](manage-vendor-collaboration-users.md)




