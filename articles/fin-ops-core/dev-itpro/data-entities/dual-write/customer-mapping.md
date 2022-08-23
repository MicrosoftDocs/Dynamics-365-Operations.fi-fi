---
title: Integroidut asiakkaan päätiedot
description: Tässä artikkelissa kuvataan asiakastietojen integraatiota talous- ja toimintosovellusten sekä Dataversen välillä.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ea142aff7c8f4b442d7224325e44359129efe8a8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289677"
---
# <a name="integrated-customer-master"></a>Integroidut asiakkaan päätiedot

[!include [banner](../../includes/banner.md)]



Asiakastietoja voidaan hallita useammassa kuin yhdessä Dynamics 365 -sovelluksessa. Esimerkiksi asiakasrivi voi olla peräisin myyntitehtävästä Dynamics 365 Salesissa (asiakasvuorovaikutussovellus) tai rivi voi olla peräisin Dynamics 365 Commercen vähittäismyynnistä (taloushallinnon toimintojen sovellus). Riippumatta siitä, mistä asiakastiedot ovat peräisin, ne integroidaan näkymän taakse. Integroidut asiakkaan päätiedot antavat sinulle joustavuutta hallita asiakastietoja missä tahansa Dynamics 365-sovelluksessa ja tarjoaa kattavan näkymän asiakkaasta kautta koko Dynamics 365 -sovelluspaketin.

## <a name="customer-data-flow"></a>Asiakastietojen virta

*Asiakas* on hyvin määritelty käsite sovelluksissa. Siksi asiakastietojen integrointi edellyttää vain asiakkaan käsitteen yhtenäistämistä kahden sovelluksen välillä. Seuraavassa on kuvattu asiakastietojen virta.

![Asiakastietojen virta.](media/dual-write-customer-data-flow.png)

Asiakkaat voidaan luokitella laajasti kahteen eri luokkaan: kaupalliset/organisaation asiakkaat ja kuluttajat/loppukäyttäjät. Nämä kaksiasiakas tyyppiä tallennetaan ja käsitellään eri tavalla talous- ja toimintosovelluksissa ja Dataversessa.

Talous- ja toimintosovelluksissa sekä kaupalliset/organisaation asiakkaat että kuluttajat/loppukäyttäjät hallittaan yhdessä taulukossa, jonka nimi on **CustTable** (CustCustomerV3Entity), ja ne luokitellaan **Tyyppi**-määritteen avulla. (Jos **tyypiksi** on määritetty **Organisaatio**, asiakas on kaupallinen/organisaation asiakas ja jos **tyypiksi** on määritetty **Henkilö**, asiakas on kuluttaja/loppukäyttäjä.) Ensisijaisen yhteyshenkilön tietoja käsitellään SMMContactPersonEntity-taulukossa.

Dataversessa kaupallisia/organisaation asiakkaita hallitaan Asiakas-taulukossa ja heidät tunnistetaan asiakkaiksi, kun **RelationshipType** -määritteeksi on määritetty **Asiakas**. Yhteyshenkilö-taulukko edustaa sekä kuluttajia/loppukäyttäjiä että yhteyshenkilöitä. Jotta kuluttajan/loppukäyttäjän ja yhteyshenkilön välillä olisi selvä ero **Yhteyshenkilö** taulukossa on **Myytävissä**-niminen totuusarvomerkintä. Kun **Myytävissä**-arvo on **Tosi**, kontakti on kuluttaja/loppukäyttäjä ja tarjouksia ja tilauksia voidaan luoda kyseiselle kontaktille. Kun **Myytävissä**-arvo **Epätosi**, kontakti on vain asiakkaan ensisijainen yhteyshenkilö.

Kun ei-Myytävissä oleva kontakti osallistuu tarjous- tai tilausprosessiin, **Myytävissä**-arvoksi annetaan **Tosi**, jotta merkitään kontakti myytävissä olevaksi kontaktiksi. Kontakti, josta on tullut Myytävissä oleva kontakti, on edelleen Myytävissä oleva kontakti.

## <a name="templates"></a>Mallit

Asiakkaan tiedot sisältävät kaikki asiakkaan tiedot, kuten asiakasryhmän, osoitteet, yhteystiedot, maksuprofiilin, laskutusprofiilin ja kanta-asiakkuuden tilan. Taulukarttojen kokoelma toimii yhdessä asiakastietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.

Taloushallinnon ja toimintojen sovellukset | Asiakkaiden aktivointisovellukset         | kuvaus
----------------------------|---------------------------------|------------
[CDS-yhteyshenkilöt V2](mapping-reference.md#115) | yhteyshenkilöt | Tämä malli synkronoi kaikki sekä asiakkaiden että toimittajien ensisijaiset, toissijaiset ja kolmannentason yhteystiedot
[Asiakasryhmät](mapping-reference.md#126) | msdyn_customergroups | Tämä malli synkronoi asiakasryhmän tiedot.
[Asiakkaan maksutapa](mapping-reference.md#127) | msdyn_customerpaymentmethods | Tämä malli synkronoi asiakkaan maksutavan tiedot.
[Asiakkaat V3](mapping-reference.md#101) | tilit | Tämä malli synkronoi asiakkaiden päätiedot kaupallisten asiakkaiden ja organisaatioasiakkaiden tiedot.
[Asiakkaat V3](mapping-reference.md#116) | yhteyshenkilöt | Tämä malli synkronoi asiakkaiden päätiedot kuluttajille ja loppukäyttäjille.
[Nimen jälkiliitteet](mapping-reference.md#155) | msdyn_nameaffixes | Tämä malli synkronoi sekä asiakkaiden että toimittajien nimen jälkiliitteiden viitetiedot.
[CDS V2 -maksupäivärivit](mapping-reference.md#157) | msdyn_paymentdaylines | Tämä malli synkronoi sekä asiakkaiden että toimittajien maksusuunnitelmarivien viitetiedot.
[CDS-maksupäivät](mapping-reference.md#158) | msdyn_paymentdays | Tämä malli synkronoi sekä asiakkaiden että toimittajien maksupäivien viitetiedot.
[Maksusuunnitelmarivit](mapping-reference.md#159) | msdyn_paymentschedulelines | Synkronoi sekä asiakkaiden että toimittajien maksusuunnitelmarivien viitetiedot.
[Maksusuunnitelma](mapping-reference.md#160) | msdyn_paymentschedules | Tämä malli synkronoi sekä asiakkaiden että toimittajien maksusuunnitelman viitetiedot.
[Maksuehdot](mapping-reference.md#161) | msdyn_paymentterms | Tämä malli synkronoi sekä asiakkaiden että toimittajien maksuehtojen (maksuehdot) viitetiedot.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

