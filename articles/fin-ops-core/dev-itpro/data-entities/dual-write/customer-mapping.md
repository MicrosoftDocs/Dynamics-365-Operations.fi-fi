---
title: Integroidut asiakkaiden päätiedot
description: Tässä aiheessa kuvataan asiakastietojen integraatiota Finance and Operationsin ja Dataversen välillä.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 801538e320ca78b0cc55bb4e4b8a80d38b9b48d6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685636"
---
# <a name="integrated-customer-master"></a>Integroidut asiakkaan päätiedot

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


Asiakastietoja voidaan hallita useammassa kuin yhdessä Dynamics 365 -sovelluksessa. Esimerkiksi asiakasrivi voi olla peräisin myyntitehtävästä Dynamics 365 Salesissa (mallivetoinen sovellus Dynamics 365:ssa) tai rivi voi olla peräisin Dynamics 365 Commercen (Finance and Operations -sovelluksen) vähittäismyynnistä. Riippumatta siitä, mistä asiakastiedot ovat peräisin, ne integroidaan näkymän taakse. Integroidut asiakkaan päätiedot antavat sinulle joustavuutta hallita asiakastietoja missä tahansa Dynamics 365-sovelluksessa ja tarjoaa kattavan näkymän asiakkaasta kautta koko Dynamics 365 -sovelluspaketin.

## <a name="customer-data-flow"></a>Asiakastietojen virta

*Asiakas* on hyvin määritelty käsite sovelluksissa. Siksi asiakastietojen integrointi edellyttää vain asiakkaan käsitteen yhtenäistämistä kahden sovelluksen välillä. Seuraavassa on kuvattu asiakastietojen virta.

![Asiakastietojen virta](media/dual-write-customer-data-flow.png)

Asiakkaat voidaan luokitella laajasti kahteen eri luokkaan: kaupalliset/organisaation asiakkaat ja kuluttajat/loppukäyttäjät. Nämä kaksiasiakas tyyppiä tallennetaan ja käsitellään eri tavalla Finance and Operationsissa ja Dataversessä.

Finance and Operationsissa sekä kaupalliset/organisaation asiakkaat että kuluttajat/loppukäyttäjät hallittaan yhdessä taulukossa, jonka nimi on **CustTable** (CustCustomerV3Entity), ja ne luokitellaan **Tyyppi**-määritteen avulla. (Jos **tyypiksi** on määritetty **Organisaatio**, asiakas on kaupallinen/organisaation asiakas ja jos **tyypiksi** on määritetty **Henkilö**, asiakas on kuluttaja/loppukäyttäjä.) Ensisijaisen yhteyshenkilön tietoja käsitellään SMMContactPersonEntity-entiteetissä.

Dataversessa kaupalliset/organisatoriset asiakkaat ovat masteroitu Asiakas-entiteetissä ja tunnistetaan asiakkaiksi , kun **RelationshipType** -määritteeksi onmääritetty **Asiakas**. Yhteyshenkilö-entiteetti edustaa sekä kuluttajia/loppukäyttäjiä että yhteyshenkilöitä. Jotta kuluttajan/loppukäyttäjän ja yhteyshenkilön välillä olisi selvä ero **Yhteysenkilö**-entiteetissä on Boolean-merkintä nimeltään **Myytävissä**. Kun **Myytävissä**-arvo on **Tosi**, kontakti on kuluttaja/loppukäyttäjä ja tarjouksia ja tilauksia voidaan luoda kyseiselle kontaktille. Kun **Myytävissä**-arvo **Epätosi**, kontakti on vain asiakkaan ensisijainen yhteyshenkilö.

Kun ei-Myytävissä oleva kontakti osallistuu tarjous- tai tilausprosessiin, **Myytävissä**-arvoksi annetaan **Tosi**, jotta merkitään kontakti myytävissä olevaksi kontaktiksi. Kontakti, josta on tullut Myytävissä oleva kontakti, on edelleen Myytävissä oleva kontakti.

## <a name="templates"></a>Mallit

Asiakkaan tiedot sisältävät kaikki asiakkaan tiedot, kuten asiakasryhmän, osoitteet, yhteystiedot, maksuprofiilin, laskutusprofiilin ja kanta-asiakkuuden tilan. Taulukarttojen kokoelma toimii yhdessä asiakastietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.

Finance and Operations -sovellukset | Muut Dynamics 365 -sovellukset         | Kuvaus
----------------------------|---------------------------------|------------
CDS-yhteyshenkilöt V2             | yhteyshenkilöt                        | Tämä malli synkronoi kaikki sekä asiakkaiden että toimittajien ensisijaiset, toissijaiset ja kolmannentason yhteystiedot
Asiakasryhmät             | msdyn_customergroups            | Tämä malli synkronoi asiakasryhmän tiedot.
Asiakkaan maksutapa     | msdyn_customerpaymentmethods    | Tämä malli synkronoi asiakkaan maksutavan tiedot.
Asiakkaat V3                | tilit                        | Tämä malli synkronoi asiakkaiden päätiedot kaupallisten asiakkaiden ja organisaatioasiakkaiden tiedot.
Asiakkaat V3                | yhteyshenkilöt                        | Tämä malli synkronoi asiakkaiden päätiedot kuluttajille ja loppukäyttäjille.
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

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]