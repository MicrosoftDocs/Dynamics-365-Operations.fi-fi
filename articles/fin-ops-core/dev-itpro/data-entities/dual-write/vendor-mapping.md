---
title: Integroidut toimittajan päätiedot
description: Tässä aiheessa kuvataan alihankkijatietojen integraatiota Finance and Operations -sovelluksen ja Dataversen välillä.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: f57a20ed56a761894b2cedf8835310dac098b098
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750615"
---
# <a name="integrated-vendor-master"></a>Integroidut toimittajan päätiedot

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Termi *toimittaja* viittaa toimittajaorganisaatioon tai elinkeinonharjoittajaan, joka toimittaa tavaroita tai palveluja yrityksille. Vaikka *toimittaja* on vakiintunut käsite Microsoft Dynamics 365 Supply Chain Management -sovelluksessa, toimittajan konseptia ei ole muissa mallipohjaisissa sovelluksissa Dynamics 365:ssa. Voit kuitenkin ylikuormittaa **Tili/yhteyshenkilö**-taulukon toimittajatietojen tallentamista varten. Integroitu toimittajan perustyyli sisältää eksplisiittisen toimittajan konseptin Dynamics 365 -malleissa, joissa käytetään mallipohjaisia sovelluksia. Voit käyttää uuden toimittajan rakennetta tai tallentaa toimittajatietoja **Asiakkuus/yhteyshenkilö**-taulukkoon. Kaksoiskirjoitus tukee molempia lähestymistapoja.

Molemmissa tapauksessa toimittajatiedot on integroitu Dynamics 365 Supply Chain Managementiin, Dynamics 365 Salesiin, Dynamics 365 Field Serviceen ja Power Apps -portaaliin. Toimitusketjun hallinnassa tiedot ovat käytettävissä työnkuluissa, kuten ostoehdotuksissa ja ostotilauksissa.

## <a name="vendor-data-flow"></a>Toimittajatietojen virta

Jos et halua tallentaa toimittajatietoja **Asiakkuus/yhteyshenkilö**-taulukkoon Dataversessa, voit käyttää uuden toimittajan rakennetta.

![Toimittajatietojen virta](media/dual-write-vendor-data-flow.png)

Jos haluat edelleen tallentaa toimittajatietoja **Asiakkuus/yhteyshenkilö**-taulukkoon, voit käyttää laajennettua toimittajan rakennetta. Jos haluat käyttää laajennettua toimittajan rakennetta, sinun on konfiguroitava toimittajan työnkulut kaksoiskirjoituksen ratkaisupaketissa. Lisätietoja on kohdassa [Toimittajan mallien välillä siirtyminen](vendor-switch.md).

![Laajennettu toimittajatietojen virta](media/dual-write-vendor-detail.jpg)

> [!TIP]
> Jos käytät itsepalvelutoimittajien Power Apps -portaaleja, toimittajatiedot voivat virrata suoraan Finance and Operations -sovelluksiin.

## <a name="templates"></a>Mallipohjat

Toimittajan tiedot sisältävät kaikki toimittajan tiedot, kuten toimittajaryhmän, osoitteet, yhteystiedot, maksuprofiilin ja laskutusprofiilin. Taulukarttojen kokoelma toimii yhdessä toimittajatietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.

Finance and Operations -sovellukset | Muut Dynamics 365 -sovellukset     | kuvaus
----------------------------|-----------------------------|------------
Toimittaja V2                   | Tili                     | Yritykset, jotka käyttävät Tili-taulukkoa toimittajatietojen tallentamiseen, voivat jatkaa sen käyttämistä samalla tavalla. Ne voivat myös hyödyntää eksplisiittistä toimittajan toiminnallisuutta, joka on tulossa Finance and Operations -sovellusten integroinnin ansiosta.
Toimittaja V2                   | Msdyn\_vendors              | Yritykset, jotka käyttävät mukautettua toimittajaratkaisua, voivat hyödyntää käyttövalmista toimittajakäsitettä, joka otetaan käyttöön Dataversessä Finance and Operations -sovellusten integroinnin ansiosta. 
Toimittajaryhmät               | msdyn\_vendorgroups         | Tämä malli synkronoi toimittajaryhmän tiedot.
Toimittajan maksutapa       | msdyn\_vendorpaymentmethods | Tämä malli synkronoi toimittajan maksutavan tiedot.
CDS-yhteyshenkilöt V2             | yhteyshenkilöt                    | [Yhteyshenkilöt](customer-mapping.md#cds-contacts-v2-to-contacts)-malli synkronoi kaikki sekä asiakkaiden että toimittajien ensisijaiset, toissijaiset ja kolmannentason yhteystiedot
Maksusuunnitelmarivit      | msdyn\_paymentschedulelines | [Maksusuunnitelmarivit](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines)-malli synkronoi sekä asiakkaiden että toimittajien viitetiedot.
Maksuaikataulu            | msdyn\_paymentschedules     | [Maksusuunnitelmat](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules)-malli synkronoi sekä asiakkaiden että toimittajien maksusuunnitelman viitetiedot.
CDS V2 -maksupäivärivit    | msdyn\_paymentdaylines      | [Maksupäivärivit](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines)-malli synkronoi asiakkaiden ja toimittajien maksupäivärivien viitetiedot.
CDS-maksupäivät            | msdyn\_paymentdays          | [Maksupäivät](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays)-malli synkronoi sekä asiakkaiden että toimittajien maksupäivien viitetiedot.
Maksuehdot            | msdyn\_paymentterms         | [Maksuehdot](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms)-malli synkronoi sekä asiakkaiden että toimittajien maksuehtojen viitetiedot.
Nimen jälkiliitteet                | msdyn\_nameaffixes          | [Nimen jälkiliitteet](customer-mapping.md#name-affixes-to-msdyn_nameaffixes)-malli synkronoi sekä asiakkaiden että toimittajien nimen jälkiliitteiden viitetiedot.

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]