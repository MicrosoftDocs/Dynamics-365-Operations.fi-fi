---
title: Integroidut asiakkaiden päätiedot
description: Tässä aiheessa kuvataan asiakastietojen integraatiota Finance and Operationsin ja Common Data Servicen välillä.
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
ms.openlocfilehash: 269346d38eeb3812c352d16f9d50fbcd09307c12
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019763"
---
# <a name="integrated-customer-master"></a>Integroidut asiakkaan päätiedot

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

On tyypillistä, että asiakastietueet voidaan masteroida useammassa kuin yhdessä sovelluksessa. Esimerkiksi myyntiaktiviteetti voi tuoda kaupallisia asiakastietueita myyntisovelluksen kautta, ja e-Commerce- tai vähittäismyynti voi tuoda asiakastietueita Finance and Operations -sovelluksen kautta. Riippumatta siitä, mistä asiakastietueet ovat peräisin, ne on integroitu taustalla sovellusten rajojen ja infrastruktuurin erojen välillä. Integroidut asiakkaiden päätiedot auttavat käsittelemään monimasterointiskenaarioita ja tarjoaa kattavan näkymän asiakkaasta Dynamics 365 -sovelluspakettiin.

## <a name="customer-data-flow"></a>Asiakastietojen virta

*Asiakas* on hyvin määritelty käsite sovelluksissa. Siksi asiakastietojen integrointi edellyttää vain asiakkaan käsitteen yhtenäistämistä kahden sovelluksen välillä. Seuraavassa on kuvattu asiakastietojen virta.

![Asiakastietojen virta](media/dual-write-customer-data-flow.png)

Asiakkaat voidaan luokitella laajasti kahteen eri luokkaan: kaupalliset/organisaation asiakkaat ja kuluttajat/loppukäyttäjät. Nämä kaksiasiakas tyyppiä tallennetaan ja käsitellään eri tavalla Finance and Operationsissa ja Common Data Servicessä.

Finance and Operationsissa sekä kaupalliset/organisaation asiakkaat että kuluttajat/loppukäyttäjät hallittaan yhdessä taulukossa, jonka nimi on **CustTable** (CustomerCustomerV3Entity), ja ne luokitellaan **Tyyppi**-määritteen avulla. (Jos **tyypiksi** on määritetty **Organisaatio**, asiakas on kaupallinen/organisaation asiakas ja jos **tyypiksi** on määritetty **Henkilö**, asiakas on kuluttaja/loppukäyttäjä.) Ensisijaisen yhteyshenkilön tietoja käsitellään SMMContactPersonEntity-entiteetissä.

Common Data Servicessa kaupalliset/organisatoriset asiakkaat ovat masteroitu Asiakas-entiteetissä ja tunnistetaan asiakkaiksi , kun **RelationshipType** -määritteeksi onmääritetty **Asiakas**. Yhteyshenkilö-entiteetti edustaa sekä kuluttajia/loppukäyttäjiä että yhteyshenkilöitä. Jotta kuluttajan/loppukäyttäjän ja yhteyshenkilön välillä olisi selvä ero **Yhteysenkilö**-entiteetissä on Boolean-merkintä nimeltään **Myytävissä**. Kun **Myytävissä**-arvo on **Tosi**, kontakti on kuluttaja/loppukäyttäjä ja tarjouksia ja tilauksia voidaan luoda kyseiselle kontaktille. Kun **Myytävissä**-arvo **Epätosi**, kontakti on vain asiakkaan ensisijainen yhteyshenkilö.

Kun ei-Myytävissä oleva kontakti osallistuu tarjous- tai tilausprosessiin, **Myytävissä**-arvoksi annetaan **Tosi**, jotta merkitään kontakti myytävissä olevaksi kontaktiksi. Kontakti, josta on tullut Myytävissä oleva kontakti, on edelleen Myytävissä oleva kontakti.

## <a name="templates"></a>Mallit

Asiakkaan tiedot sisältävät kaikki asiakkaan tiedot, kuten asiakasryhmän, osoitteet, yhteystiedot, maksuprofiilin, laskutusprofiilin ja kanta-asiakkuuden tilan. Entiteettikarttojen kokoelma toimii yhdessä asiakastietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.

Finance and Operations -sovellukset | Muut Dynamics 365 -sovellukset         | Kuvaus
----------------------------|---------------------------------|------------
CDS-yhteyshenkilöt V2             | yhteyshenkilöt                        | Tämä malli synkronoi kaikki sekä asiakkaiden että toimittajien ensisijaiset, toissijaiset ja kolmannentason yhteystiedot
Asiakasryhmät             | msdyn_customergroups            | Tämä malli synkronoi asiakasryhmän tiedot.
Asiakkaan maksutapa     | msdyn_customerpaymentmethods    | Tämä malli synkronoi asiakkaan maksutavan tiedot.
Asiakkaat V3                | tilit                        | Tämä malli synkronoi asiakkaiden päätiedot kaupallisten asiakkaiden ja organisaatioasiakkaiden tiedot.
Asiakkaat V3                | yhteyshenkilöt                        | Tämä malli synkronoi asiakkaiden päätiedot kuluttajille ja loppukäyttäjille.
Kanta-asiakaskortti                | msdyn_loyaltycards              | Tämä malli synkronoi asiakkaan kanta-asiakaskortin tiedot.
Nimen jälkiliitteet                | msdyn_nameaffixes               | Tämä malli synkronoi sekä asiakkaiden että toimittajien nimen jälkiliitteiden viitetiedot.
CDS V2 -maksupäivärivit    | msdyn_paymentdaylines           | Tämä malli synkronoi sekä asiakkaiden että toimittajien maksusuunnitelmarivien viitetiedot.
CDS-maksupäivät            | msdyn_paymentdays               | Tämä malli synkronoi sekä asiakkaiden että toimittajien maksupäivien viitetiedot.
Maksusuunnitelmarivit      | msdyn_paymentschedulelines      | Synkronoi sekä asiakkaiden että toimittajien maksusuunnitelmarivien viitetiedot.
Maksusuunnitelma            | msdyn_paymentschedules          | Tämä malli synkronoi sekä asiakkaiden että toimittajien maksusuunnitelman viitetiedot.
Maksuehdot            | msdyn_paymentterms              | Tämä malli synkronoi sekä asiakkaiden että toimittajien maksuehtojen (maksuehdot) viitetiedot.

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]
