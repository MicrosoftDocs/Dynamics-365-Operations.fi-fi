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
ms.openlocfilehash: d33625b94e7611a256c389a6de4692ae8f4ff2a7
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572469"
---
# <a name="integrated-vendor-master"></a>Integroidut toimittajien päätiedot

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

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

Finance and Operations -sovellukset  | Muut Dynamics 365 -sovellukset
------------------------|---------------------------------
Toimittaja V2               | Tili
Toimittaja V2               | Msdyn\_vendors
CDS-yhteyshenkilöt V2         | Ota yhteyttä
Toimittajaryhmät           | Msdyn\_vendorgroups
Toimittajan maksutapa   | Msdyn\_vendorpaymentmethods
Maksusuunnitelma        | Msdyn\_paymentschedules
Maksusuunnitelma        | Msdyn\_paymentschedulelines
CDS-maksupäivä         | Msdyn\_paymentdays
CDS-maksupäivärivit   | Msdyn\_paymentdaylines
Maksuehdot        | Msdyn\_paymentterms
Nimen jälkiliitteet            | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="vendor-v2-and-account"></a>Toimittaja V2 ja Asiakas 

Yritykset, jotka käyttävät Asiakas-entiteettiä toimittajatietojen tallentamiseen, voivat jatkaa sen käyttämistä samalla tavalla. Ne voivat myös hyödyntää eksplisiittistä toimittajan toiminnallisuutta, joka on tulossa Finance and Operations -sovellusten integroinnin ansiosta.

## <a name="vendor-v2-and-msdyn_vendors"></a>Toimittaja V2 ja Msdyn\_vendors

Yritykset, jotka käyttävät mukautettua toimittajaratkaisua, voivat hyödyntää käyttövalmista toimittajakäsitettä, joka otetaan käyttöön Common Data Servicessa Finance and Operations -sovellusten integroinnin ansiosta. 

<!-- ![vendor mappings](media/dual-write-vendors-1.png) -->

<!-- ![vendor mappings](media/dual-write-vendors-2.png) -->

<!-- ![vendor mappings](media/dual-write-vendors-3.png) -->

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
VENDORACCOUNTNUMBER | = | msdyn\_vendoraccountnumber
VENDORGROUPID | = | msdyn\_vendorgroupid.msdyn\_vendorgroup
VENDORORGANIZATIONNAME | = | msdyn\_name
VENDORPARTYTYPE | \>\< | msdyn\_isperson
PERSONFIRSTNAME | = | msdyn\_firstname
PERSONLASTNAME | = | msdyn\_lastname
CREDITLIMIT | = | msdyn\_vendorcreditlimit
ISFOREIGNENTITY | \>\< | msdyn\_isforeignentity
ISONETIMEVENDOR | \>\< | msdyn\_isonetimevendor
ADDRESSBUILDINGCOMPLIMENT | = | msdyn\_addressbuildingcompliment
PERSONCHILDRENNAMES | = | msdyn\_childrennames
ADDRESSCITY | = | msdyn\_addresscity
ADDRESSCOUNTRYREGIONID | = | msdyn\_addresscountryregionid
ADDRESSCOUNTRYREGIONISOCODE | = | msdyn\_addresscountryregionisocode
ADDRESSCOUNTYID | = | msdyn\_addresscountyid
CREDITRATING | = | msdyn\_creditrating
ADDRESSDESCRIPTION | = | msdyn\_addressdescription
ADDRESSDISTRICTNAME | = | msdyn\_addressdistrictname
DUNSNUMBER | = | msdyn\_dunsnumber
ETHNICORIGINID | = | msdyn\_ethnicorigin
FORMATTEDPRIMARYADDRESS | = | msdyn\_formattedprimaryaddress
PERSONHOBBIES | = | msdyn\_hobbies
PERSONINITIALS | = | msdyn\_initials
LANGUAGEID | = | msdyn\_languageid
PERSONLASTNAMEPREFIX | = | msdyn\_lastnameprefix
PERSONMIDDLENAME | = | msdyn\_middlename
ORGANIZATIONNUMBER | = | msdyn\_organizationnumber
OURACCOUNTNUMBER | = | msdyn\_ourvendoraccountnumber
PAYMENTID | = | msdyn\_paymentid
PERSONPHONETICFIRSTNAME | = | msdyn\_phoneticfirstname
PERSONPHONETICMIDDLENAME | = | msdyn\_phoneticmiddlename
PERSONPHONETICLASTNAME | = | msdyn\_phoneticlastname
ORGANIZATIONPHONETICNAME | = | msdyn\_organizationphoneticname
ADDRESSPOSTBOX | = | msdyn\_addresspostbox
PRIMARYURL | = | msdyn\_primarycontacturl
PRIMARYEMAILADDRESS | = | msdyn\_primaryemailaddress
PRIMARYEMAILADDRESSDESCRIPTION | = | msdyn\_primaryemailaddressdescription
PRIMARYFACEBOOK | = | msdyn\_primaryfacebook
PRIMARYFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYFAXNUMBER | = | msdyn\_primaryfaxnumber
PRIMARYFAXNUMBERDESCRIPTION | = | msdyn\_primaryfaxnumberdescription
PRIMARYFAXNUMBEREXTENSION | = | msdyn\_primaryfaxnumberextension
PRIMARYLINKEDIN | = | msdyn\_primarylinkedin
PRIMARYLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescription
PRIMARYPHONENUMBER | = | msdyn\_pimaryphonenumber
PRIMARYPHONENUMBERDESCRIPTION | = | msdyn\_primaryphonenumberdescription
PRIMARYPHONENUMBEREXTENSION | = | msdyn\_primaryphonenumberextension
PRIMARYTELEX | = | msdyn\_primarytelex
PRIMARYTELEXDESCRIPTION | = | msdyn\_primarytelexdescription
PRIMARYTWITTER | = | msdyn\_primarytwitter
PRIMARYTWITTERDESCRIPTION | = | msdyn\_primarytwitterdescription
PRIMARYURLDESCRIPTION | = | msdyn\_primaryurldescription
PERSONPROFESSIONALSUFFIX | = | msdyn\_professionalsuffix
PERSONPROFESSIONALTITLE | = | msdyn\_professionatitle
ADDRESSSTATEID | = | msdyn\_addressstateid
ADDRESSSTREET | = | msdyn\_addressstreet
ADDRESSSTREETNUMBER | = | msdyn\_addressstreetnumber
VENDORKNOWNASNAME | = | msdyn\_vendorknownasname
ADDRESSZIPCODE | = | msdyn\_addresszipcode
DEFAULTPAYMENTDAYNAME | = | msdyn\_defaultpaymentdayname.msdyn\_name
DEFAULTPAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
DEFAULTPAYMENTTERMSNAME | = | msdyn\_paymentterms.msdyn\_name
HASONLYTAKENBIDS | \>\< | msdyn\_hasonlytakenbids
ISMINORITYOWNED | \>\< | msdyn\_isminorityowned
ISVENDORLOCALLYOWNED | \>\< | msdyn\_isvendorlocallyowned
ISSERVICEVETERANOWNED | \>\< | msdyn\_isserviceveteranowned
ISOWNERDISABLED | \>\< | msdyn\_ownerisdisabled
ISWOMANOWNER | \>\< | msdyn\_womanowner
PERSONANNIVERSARYDAY | = | msdyn\_personanniversaryday
PERSONANNIVERSARYYEAR | = | msdyn\_anniversaryyear
PERSONBIRTHDAY | = | msdyn\_birthday
PERSONBIRTHYEAR | = | msdyn\_birthyear
ORGANIZATIONEMPLOYEEAMOUNT | = | msdyn\_numberofemployees
VENDORHOLDRELEASEDATE | = | msdyn\_vendoronholdreleasedate
VENDORPARTYNUMBER | = | msdyn\_vendorpartynumber
ADDRESSLOCATIONID | = | msdyn\_addresslocationid
PERSONANNIVERSARYMONTH | = | msdyn\_vendorpersonanniversarymonth
PERSONBIRTHMONTH | = | msdyn\_vendorpersonbirthmonth
PERSONMARITALSTATUS | \>\< | msdyn\_maritalstatus
ADDRESSLATITUDE | \>\> | msdyn\_addresslatitude
ADDRESSLONGITUDE | \>\> | msdyn\_addresslongitude
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
CURRENCYCODE | = | msdyn\_currencycode.isocurrencycode
ISVENDORLOCATEDINHUBZONE | \>\< | msdyn\_isvendorlocatedinhubzone
DEFAULTVENDORPAYMENTMETHODNAME | = | msdyn\_vendorpaymentmethod.msdyn\_name
INVOICEVENDORACCOUNTNUMBER | = | msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber
PERSONGENDER | \>\< | msdyn\_gender
AREPRICESINCLUDINGSALESTAX | \>\< | msdyn\_priceincludessalestax
SALESTAXGROUPCODE | = | msdyn\_taxgroup.msdyn\_name
VENDORPRICETOLERANCEGROUPID | = | msdyn\_pricetolerancegroup.msdyn\_groupid

## <a name="contacts"></a>Yhteyshenkilöt

Tämä malli synkronoi kaikki sekä asiakkaiden että toimittajien ensisijaiset, toissijaiset ja kolmannen tason yhteystiedot Finance and Operations -sovellusten ja muiden Dynamics 365 -sovellusten välillä. Lisätietoja entiteettien yhdistämismääritysten yksityiskohdista on kohdassa [Integroidut asiakkaiden päätiedot](dual-write-customer.md#contacts).

## <a name="vendor-groups"></a>Toimittajaryhmät

Tämä malli synkronoi toimittajaryhmän tiedot Finance and Operations -sovellusten ja muiden Dynamics 365 -sovellusten välillä.

<!-- ![vendor groups mappings](media/dual-write-vendor-groups.png) -->

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
DEFAULTPAYMENTTERMNAME | = | msdyn\_paymentterms.msdyn\_name
KUVAUS | = | msdyn\_description
VENDORGROUPID | = | msdyn\_vendorgroup
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymentpermname.msdyn\_name

### <a name="vendor-payment-method"></a>Toimittajan maksutapa

Tämä malli synkronoi toimittajan maksutapatiedot Finance and Operationsin ja muiden Dynamics 365 -sovellusten välillä.

<!-- ![vendor payment method mappings](media/dual-write-vendor-payment-method.png) -->

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
NIMI | = | msdyn\_name
KUVAUS | = | msdyn\_description
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
ALLOWPAYMENTCOPIES | \>\< | msdyn\_allowpaymentcopies
PAYMENTTYPE | \>\< | msdyn\_paymenttype
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
ACCOUNTTYPE | \>\< | msdyn\_accounttype
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingposting
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_postdatedcheckclearingposting
PROMISSORYNOTEDRAFTTYPE | \>\< | msdyn\_promissorynotedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit

