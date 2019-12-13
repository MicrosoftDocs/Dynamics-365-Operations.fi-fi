---
title: Integroidut toimittajien päätiedot
description: Tässä aiheessa käsitellään toimittajan tietojen integrointia Finance and Operations -sovellusten ja Common Data Servicen välillä.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: da451c63c23444da564307505d38699faf9df19a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770979"
---
# <a name="integrated-vendor-master"></a>Integroidut toimittajien päätiedot

[!include [banner](../includes/banner.md)]

Termi *toimittaja* viittaa toimittajaorganisaatioon tai yksikköön, joka on osa toimitusketjun prosessia ja joka toimittaa tavaroita liiketoimintaa varten. Vaikka *toimittaja* on vakiintunut käsite Finance and Operations -sovelluksissa, toimittajan käsitettä ei ole muissa Dynamics 365 -sovelluksissa. Sen sijaan jotkin yritykset ylikuormittavat Asiakas-entiteettiä tallentamaan sekä asiakastietoja että toimittajatietoja. Muut yritykset käyttävät mukautettua toimittajakonseptia. Common Data Service -integraatio tukee molempia malleja. Tämän vuoksi voit ottaa käyttöön jommankumman malleista liiketoimintaskenaarion mukaan.

Toimittajatietojen integrointi Finance and Operations -sovellusten ja muiden Dynamics 365 -sovellusten välillä mahdollistaa päätietojen hallinnan monessa paikassa. Riippumatta siitä, mistä toimittajan tiedot ovat peräisin, ne on integroitu taustalla sovellusten rajojen ja infrastruktuurin erojen välillä. 

### <a name="vendor-data-flow"></a>Toimittajatietojen virta

Jos haluat käyttää muita Dynamics 365 -sovelluksia toimittajatietojen päähallintaan ja haluat eristää toimittajan tiedot asiakastiedoista, voit käyttää uutta toimittajarakennetta.

![Toimittajatietojen virta](media/dual-write-vendor-data-flow.png)

Jos haluat käyttää Dynamics 365 -sovelluksia toimittajatietojen päähallintaan ja jatkaa toimittajan tietojen tallentamista asiakastietoihin, voit käyttää uutta laajennettua toimittajarakennetta. Tässä suunnittelussa laajennetut toimittajatiedot, kuten toimittajaryhmä ja toimittajan kirjausprofiili, tallennetaan toimittajan tietoihin.

![Laajennettu toimittajatietojen virta](media/dual-write-vendor-detail.jpg)

Toimittajan yhteystiedot muistuttavat asiakkaan yhteystietoja. Taustalla yhteyshenkilön tiedot tallennetaan ja haetaan samoista entiteeteistä.

## <a name="templates"></a>Mallit

Toimittajan tiedot sisältävät kaikki toimittajan tiedot, kuten toimittajaryhmän, osoitteet, yhteystiedot, maksuprofiilin ja laskutusprofiilin. Entiteettikarttojen kokoelma toimii yhdessä toimittajatietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.

Finance and Operations -sovellukset | Muut Dynamics 365 -sovellukset         | Kuvaus
----------------------------|---------------------------------|------------
Toimittaja V2               | Tili | Yritykset, jotka käyttävät Asiakas-entiteettiä toimittajatietojen tallentamiseen, voivat jatkaa sen käyttämistä samalla tavalla. Ne voivat myös hyödyntää eksplisiittistä toimittajan toiminnallisuutta, joka on tulossa Finance and Operations -sovellusten integroinnin ansiosta.
Toimittaja V2               | Msdyn\_vendors | Yritykset, jotka käyttävät mukautettua toimittajaratkaisua, voivat hyödyntää käyttövalmista toimittajakäsitettä, joka otetaan käyttöön Common Data Servicessa Finance and Operations -sovellusten integroinnin ansiosta. 
Toimittajaryhmät | msdyn_vendorgroups | Tämä malli synkronoi toimittajaryhmän tiedot.
Toimittajan maksutapa | msdyn_vendorpaymentmethods | Tämä malli synkronoi toimittajan maksutavan tiedot.
CDS-yhteyshenkilöt V2             | yhteyshenkilöt                        | [Yhteyshenkilöt](dual-write-customer.md#cds-contacts-v2-to-contacts)-malli synkronoi kaikki sekä asiakkaiden että toimittajien ensisijaiset, toissijaiset ja kolmannentason yhteystiedot
Maksusuunnitelmarivit      | msdyn_paymentschedulelines      | [Maksusuunnitelmarivit](dual-write-customer.md#payment-schedule-lines-to-msdyn_paymentschedulelines)-malli synkronoi sekä asiakkaiden että toimittajien viitetiedot.
Maksusuunnitelma            | msdyn_paymentschedules          | [Maksusuunnitelmat](dual-write-customer.md#payment-schedule-to-msdyn_paymentschedules)-malli synkronoi sekä asiakkaiden että toimittajien maksusuunnitelman viitetiedot.
CDS V2 -maksupäivärivit    | msdyn_paymentdaylines           | [Maksupäivärivit](dual-write-customer.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines)-malli synkronoi asiakkaiden ja toimittajien maksupäivärivien viitetiedot.
CDS-maksupäivät            | msdyn_paymentdays               | [Maksupäivät](dual-write-customer.md#payment-days-cds-to-msdyn_paymentdays)-malli synkronoi sekä asiakkaiden että toimittajien maksupäivien viitetiedot.
Maksuehdot            | msdyn_paymentterms              | [Maksuehdot](dual-write-customer.md#terms-of-payment-to-msdyn_paymentterms)-malli synkronoi sekä asiakkaiden että toimittajien maksuehtojen viitetiedot.
Nimen jälkiliitteet                | msdyn_nameaffixes               | [Nimen jälkiliitteet](dual-write-customer.md#name-affixes-to-msdyn_nameaffixes)-malli synkronoi sekä asiakkaiden että toimittajien nimen jälkiliitteiden viitetiedot.

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [Vendors](dual-write/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](dual-write/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](dual-write/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]
