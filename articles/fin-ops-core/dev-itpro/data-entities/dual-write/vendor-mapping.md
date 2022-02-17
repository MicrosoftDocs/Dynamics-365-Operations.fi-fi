---
title: Integroidut toimittajien päätiedot
description: Tässä aiheessa käsitellään toimittajan tietojen integrointia taloushallinnon ja toimintojen sovellusten ja Dataversen välillä.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 7794f33aed7364b76a7d5ffd08a068342887e468
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063159"
---
# <a name="integrated-vendor-master"></a>Integroidut toimittajan päätiedot

[!include [banner](../../includes/banner.md)]



Termi *toimittaja* viittaa toimittajaorganisaatioon tai elinkeinonharjoittajaan, joka toimittaa tavaroita tai palveluja yrityksille. Vaikka *toimittaja* on vakiintunut käsite Microsoft Dynamics 365 Supply Chain Management issa, toimittajan konseptia ei ole muissa asiakasvuorovaikutussovelluksissa. Voit kuitenkin ylikuormittaa **Tili/yhteyshenkilö**-taulukon toimittajatietojen tallentamista varten. Integroitu päätoimittaja esittelee eksplisiittisen toimittajan käsitteen asiakasvuorovaikutussovelluksiin. Voit käyttää uuden toimittajan rakennetta tai tallentaa toimittajatietoja **Asiakkuus/yhteyshenkilö**-taulukkoon. Kaksoiskirjoitus tukee molempia lähestymistapoja.

Molemmissa tapauksessa toimittajatiedot on integroitu Dynamics 365 Supply Chain Managementiin, Dynamics 365 Salesiin, Dynamics 365 Field Serviceen ja Power Apps -portaaliin. Toimitusketjun hallinnassa tiedot ovat käytettävissä työnkuluissa, kuten ostoehdotuksissa ja ostotilauksissa.

## <a name="vendor-data-flow"></a>Toimittajatietojen virta

Jos et halua tallentaa toimittajatietoja **Asiakkuus/yhteyshenkilö**-taulukkoon Dataversessa, voit käyttää uuden toimittajan rakennetta.

![Toimittajatietojen virta.](media/dual-write-vendor-data-flow.png)

Jos haluat edelleen tallentaa toimittajatietoja **Asiakkuus/yhteyshenkilö**-taulukkoon, voit käyttää laajennettua toimittajan rakennetta. Jos haluat käyttää laajennettua toimittajan rakennetta, sinun on konfiguroitava toimittajan työnkulut kaksoiskirjoituksen ratkaisupaketissa. Lisätietoja on kohdassa [Toimittajan mallien välillä siirtyminen](vendor-switch.md).

![Laajennettu toimittajatietojen virta.](media/dual-write-vendor-detail.jpg)

> [!TIP]
> Jos käytät itsepalvelutoimittajien Power Apps -portaaleja, toimittajatiedot voivat virrata suoraan taloushallinnon ja toimintojen sovelluksiin.

## <a name="templates"></a>Mallit

Toimittajan tiedot sisältävät kaikki toimittajan tiedot, kuten toimittajaryhmän, osoitteet, yhteystiedot, maksuprofiilin ja laskutusprofiilin. Taulukarttojen kokoelma toimii yhdessä toimittajatietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.

Taloushallinnon ja toimintojen sovellukset | Asiakkaiden aktivointisovellukset     | kuvaus
----------------------------|-----------------------------|------------
[CDS-yhteyshenkilöt V2](mapping-reference.md#115) | yhteyshenkilöt | Tämä malli synkronoi kaikki sekä asiakkaiden että toimittajien ensisijaiset, toissijaiset ja kolmannentason yhteystiedot
[Nimen jälkiliitteet](mapping-reference.md#155) | msdyn_nameaffixes | Tämä malli synkronoi sekä asiakkaiden että toimittajien nimen jälkiliitteiden viitetiedot.
[CDS V2 -maksupäivärivit](mapping-reference.md#157) | msdyn_paymentdaylines | Tämä malli synkronoi sekä asiakkaiden että toimittajien maksusuunnitelmarivien viitetiedot.
[CDS-maksupäivät](mapping-reference.md#158) | msdyn_paymentdays | Tämä malli synkronoi sekä asiakkaiden että toimittajien maksupäivien viitetiedot.
[Maksusuunnitelmarivit](mapping-reference.md#159) | msdyn_paymentschedulelines | Synkronoi sekä asiakkaiden että toimittajien maksusuunnitelmarivien viitetiedot.
[Maksusuunnitelma](mapping-reference.md#160) | msdyn_paymentschedules | Tämä malli synkronoi sekä asiakkaiden että toimittajien maksusuunnitelman viitetiedot.
[Maksuehdot](mapping-reference.md#161) | msdyn_paymentterms | Tämä malli synkronoi sekä asiakkaiden että toimittajien maksuehtojen (maksuehdot) viitetiedot.
[Toimittajat V2](mapping-reference.md#202) | msdyn_vendors | Yritykset, jotka käyttävät mukautettua toimittajaratkaisua, voivat hyödyntää käyttövalmista toimittajakäsitettä, joka otetaan käyttöön Dataversessa taloushallinnon ja toimintojen sovellusten integroinnin ansiosta.
[Toimittajaryhmät](mapping-reference.md#200) | msdyn_vendorgroups | Tämä malli synkronoi toimittajaryhmän tiedot.
[Toimittajan maksutapa](mapping-reference.md#201) | msdyn_vendorpaymentmethods | Tämä malli synkronoi toimittajan maksutavan tiedot.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
