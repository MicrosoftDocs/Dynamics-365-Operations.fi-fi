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
ms.openlocfilehash: a66beb6338ea593247c79a11feb7f301d56f32a9
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572515"
---
# <a name="integrated-customer-master"></a>Integroidut asiakkaiden päätiedot

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

On tyypillistä, että asiakastietueet voidaan masteroida useammassa kuin yhdessä sovelluksessa. Esimerkiksi myyntiaktiviteetti voi tuoda kaupallisia asiakastietueita Sales-sovelluksen kautta ja sähköinen kaupankäynti tai vähittäismyynti voi tuoda asiakastietueita Finance and Operations -sovelluksen kautta. Riippumatta siitä, mistä asiakastietueet ovat peräisin, ne on integroitu taustalla sovellusten rajojen ja infrastruktuurin erojen välillä. Integroidut asiakkaiden päätiedot auttavat käsittelemään monimasterointiskenaarioita ja tarjoaa kattavan näkymän asiakkaasta Dynamics 365 -sovelluspakettiin.

## <a name="customer-data-flow"></a>Asiakastietojen virta

*Asiakas* on hyvin määritelty käsite sovelluksissa. Siksi asiakastietojen integrointi edellyttää vain asiakkaan käsitteen yhtenäistämistä kahden sovelluksen välillä. Seuraavassa on kuvattu asiakastietojen virta.

![Asiakastietojen virta](media/dual-write-customer-data-flow.png)

Asiakkaat voidaan luokitella laajasti kahteen eri luokkaan: kaupalliset/organisaation asiakkaat ja kuluttajat/loppukäyttäjät. Nämä kaksiasiakas tyyppiä tallennetaan ja käsitellään eri tavalla Finance and Operationsissa ja Common Data Servicessa.

Finance and Operationsissa sekä kaupalliset/organisaation asiakkaat että kuluttajat/loppukäyttäjät hallittaan yhdessä taulukossa, jonka nimi on **CustTable** (CustomerCustomerV3Entity), ja ne luokitellaan **Tyyppi**-määritteen avulla. (Jos **tyypiksi** on määritetty **Organisaatio**, asiakas on kaupallinen/organisaation asiakas ja jos **tyypiksi** on määritetty **Henkilö**, asiakas on kuluttaja/loppukäyttäjä.) Ensisijaisen yhteyshenkilön tietoja käsitellään SMMContactPersonEntity-entiteetissä.

Common Data Servicessa kaupalliset/organisatoriset asiakkaat ovat masteroitu Asiakas-entiteetissä ja tunnistetaan asiakkaiksi , kun **RelationshipType** -määritteeksi onmääritetty **Asiakas**. Yhteyshenkilö-entiteetti edustaa sekä kuluttajia/loppukäyttäjiä että yhteyshenkilöitä. Jotta kuluttajan/loppukäyttäjän ja yhteyshenkilön välillä olisi selvä ero **Yhteysenkilö**-entiteetissä on Boolean-merkintä nimeltään **Myytävissä**. Kun **Myytävissä**-arvo on **Tosi**, kontakti on kuluttaja/loppukäyttäjä ja tarjouksia ja tilauksia voidaan luoda kyseiselle kontaktille. Kun **Myytävissä**-arvo **Epätosi**, kontakti on vain asiakkaan ensisijainen yhteyshenkilö.

Kun ei-Myytävissä oleva kontakti osallistuu tarjous- tai tilausprosessiin, **Myytävissä**-arvoksi annetaan **Tosi**, jotta merkitään kontakti myytävissä olevaksi kontaktiksi. Kontakti, josta on tullut Myytävissä oleva kontakti, on edelleen Myytävissä oleva kontakti.

## <a name="templates"></a>Mallit

Asiakkaan tiedot sisältävät kaikki asiakkaan tiedot, kuten asiakasryhmän, osoitteet, yhteystiedot, maksuprofiilin, laskutusprofiilin ja kanta-asiakkuuden tilan. Entiteettikarttojen kokoelma toimii yhdessä asiakastietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.

Finance and Operations -sovellukset    | Muut Dynamics 365 -sovellukset
--------------------------|---------------------------------
Asiakas V3               | Tili
Asiakas V3               | Ota yhteyttä
CDS-yhteyshenkilöt V2           | Ota yhteyttä
Asiakasryhmät           | Msdyn\_customergroups
Asiakkaan maksutapa   | Msdyn\_customerpaymentmethods
Kanta-asiakaskortti              | Msdyn\_loyaltycards
Maksusuunnitelma          | Msdyn\_paymentschedules
Maksusuunnitelma          | Msdyn\_paymentschedulelines
CDS-maksupäivä           | Msdyn\_paymentdays
CDS-maksupäivärivit     | Msdyn\_paymentdaylines
Maksuehdot          | Msdyn\_paymentterms
Nimen jälkiliitteet              | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="customer-v3-to-account"></a>Asiakas V3 – Asiakas

Tämä malli synkronoi asiakkaiden päätiedot kaupallisten ja organisaation asiakkaiden tiedot Finance and Operations -sovellusten ja Common Data Servicen välillä.

<!-- ![](media/dual-write-account-1.png) -->

<!-- ![](media/dual-write-account-2.png) -->

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
CUSTOMERACCOUNT | = | accountnumber
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
CREDITLIMIT | = | creditlimit
DELIVERYADDRESSCITY | = | address1\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
DELIVERYADDRESSCOUNTY | = | address1\_county
DELIVERYADDRESSLATITUDE | \> | address1\_latitude
DELIVERYADDRESSLONGITUDE | \> | address1\_longitude
DELIVERYADDRESSZIPCODE | = | address1\_postalcode
ORGANIZATIONNAME | = | name
ORGANIZATIONNUMBEROFEMPLOYEES | = | numberofemployees
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTFAX | = | fax
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTTWITTER | = | primarytwitterid
PRIMARYCONTACTURL | = | websiteurl
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | kuvaus
CREDITLIMITISMANDATORY | \>\< | msdyn\_creditlimitismandatory
CREDITRATING | = | msdyn\_creditrating
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
INVOICEACCOUNT | = | msdyn\_billingaccount.accountnumber
INVOICEADDRESS | \>\< | msdyn\_invoiceaddress
ISONETIMECUSTOMER | \>\< | msdyn\_onetimecustomer
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PAYMENTDAY | = | msdyn\_paymentday.msdyn\_name
PAYMENTMETHOD | = | msdyn\_customerpaymentmethod.msdyn\_name
PAYMENTSCHEDULE | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTTERMS | = | msdyn\_paymentterm.msdyn\_name
PAYMENTTERMSBASEDAYS | = | msdyn\_paymenttermsbasedays
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
PRIMARYCONTACTLINKEDIN | = | msdyn\_primarylinkedinid
TAXEXEMPTNUMBER | = | msdyn\_taxexemptnumber
VENDORACCOUNT | = | msdyn\_vendor.msdyn\_vendoraccountnumber
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
LANGUAGEID | \<\< | none
DELIVERYADDRESSSTREET | = | address1\_line1
DELIVERYADDRESSSTATE | = | address1\_stateorprovince
none | \>\> | address1\_addresstypecode
none | \>\> | customertypecode
PARTYTYPE | \<\< | none
PARTYNUMBER | = | msdyn\_partynumber

## <a name="customer-v3-to-contact"></a>Asiakas V3 – yhteyshenkilö

Tämä malli synkronoi asiakkaiden päätiedot kuluttajille ja loppukäyttäjille tiedot Finance and Operationsin ja muiden Dynamics 365 -sovellusten välillä.

<!-- ![](media/dual-write-contact-1.png) -->
<!-- ![](media/dual-write-contact-2.png) -->

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
none | \>\> | msdyn\_sellable
PARTYTYPE | \<\< | none
PARTYNUMBER | = | msdyn\_partynumber
CUSTOMERACCOUNT | = | msdyn\_contactpersonid
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
PERSONFIRSTNAME | = | firstname
PERSONLASTNAME | = | lastname
PERSONMIDDLENAME | = | middlename
PERSONPROFESSIONALTITLE | = | jobtitle
PERSONGENDER | \>\< | gendercode
PERSONMARITALSTATUS | \>\< | familystatuscode
LANGUAGEID | \<\< | none
ADDRESSCITY | = | address1\_city
ADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
ADDRESSCOUNTY | = | address1\_county
ADDRESSLATITUDE | \> | address1\_latitude
ADDRESSLONGITUDE | \> | address1\_longitude
ADDRESSLOCATIONROLES | \<\< | none
ADDRESSSTATE | = | address1\_stateorprovince
ADDRESSSTREET | = | address1\_line1
ADDRESSZIPCODE | = | address1\_postalcode
ADDRESSPOSTBOX | = | address1\_postofficebox
none | \>\> | address1\_addresstypecode
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
none | \>\> | address2\_addresstypecode
DELIVERYADDRESSCITY | = | address3\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address3\_country
DELIVERYADDRESSCOUNTY | = | address3\_county
DELIVERYADDRESSLATITUDE | \> | address3\_latitude
DELIVERYADDRESSLONGITUDE | \>\> | address3\_longitude
DELIVERYADDRESSSTATE | = | address3\_stateorprovince
DELIVERYADDRESSSTREET | = | address3\_line1
DELIVERYADDRESSZIPCODE | = | address3\_postalcode
none | \>\> | address3\_addresstypecode
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFAX | = | fax
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTLINKEDIN | = | msdyn\_primaryinkedinid
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTER | = | msdyn\_primarytwitterid
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURL | = | websiteurl
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | kuvaus

## <a name="contacts"></a>Yhteyshenkilöt

Tämä malli synkronoi kaikki sekä asiakkaiden että toimittajien ensisijaiset, toissijaiset ja kolmannen tason yhteystiedot Finance and Operationsin ja muiden Dynamics 365 -sovellusten välillä.

<!-- ![](media/dual-write-contacts.png) -->

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn\_partynumber
ASSOCIATEDCONTACTTYPE | \<\< | none
FIRSTNAME | = | firstname
MIDDLENAME | = | middlename
LASTNAME | = | lastname
ASSOCIATEDCONTACTNUMBER | = | msdyn\_vendorcontactid.msdyn\_vendoraccountnumber
PRIMARYADDRESSCITY | = | address1\_city
PRIMARYADDRESSCOUNTRYREGIONID | = | address1\_country
PRIMARYADDRESSCOUNTYID | = | address1\_county
PRIMARYFAXNUMBER | = | fax
PRIMARYADDRESSSTATEID | = | address1\_stateorprovince
PRIMARYADDRESSSTREET | = | address1\_line1
PRIMARYADDRESSZIPCODE | = | address1\_postalcode
PRIMARYPHONENUMBER | = | telephone1
PRIMARYEMAILADDRESS | = | emailaddress1
EMPLOYMENTDEPARTMENT | = | department
NOTES | = | kuvaus
GENDER | \>\< | gendercode
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid
PRIMARYURL | = | websiteurl
MARITALSTATUS | \>\< | familystatuscode
ISRECEIVINGDIRECTMAIL | \>\< | donotemail
EMPLOYMENTPROFESSION | = | jobtitle
SPOUSENAME | = | spousesname
none | \>\> | msdyn\_contactforvendor
none | \>\> | msdyn\_contactpersonid

## <a name="customer-groups"></a>Asiakasryhmät

Tämä malli synkronoi asiakasryhmän tiedot Finance and Operationsin ja muiden Dynamics 365 -sovellusten välillä.

<!-- ![](media/dual-write-customer-groups.png) -->

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
CUSTOMERGROUPID | = | msdyn\_groupid
KUVAUS | = | msdyn\_description
ISSALESTAXINCLUDEDINPRICE | \>\< | msdyn\_issalestaxincludedinprice
PAYMENTTERMID | = | msdyn\_paymenttermid.msdyn\_name
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymenttermname.msdyn\_name

## <a name="customer-payment-methods"></a>Asiakkaan maksutavat

Tämä malli synkronoi asiakkaan maksutapatiedot Finance and Operationsin ja muiden Dynamics 365 -sovellusten välillä.

<!-- ![](media/dual-write-customer-payment-methods.png) -->

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
NIMI | = | msdyn\_name
ACCOUNTTYPE | \>\< | msdyn\_accounttype
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingpostingenabled
ISSEPA | \>\< | msdyn\_issepa
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
KUVAUS | = | msdyn\_description
PAYMENTTYPE | \>\< | msdyn\_paymenttype
CREATEANDDRAWBILLOFEXCHANGEDURINGINVOICEPOSTING | \>\< | msdyn\_invoiceupdate
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_enablepostdatescheckclearingposting
BILLOFEXCHANGEDRAFTTYPE | \>\< | msdyn\_billofexchangedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit

## <a name="loyalty-cards"></a>Kanta-asiakaskortit

Tämä malli synkronoi asiakkaan kanta-asiakaskortin tiedot Finance and Operationsin ja muiden Dynamics 365 -sovellusten välillä.

<!-- ![](media/dual-write-loyalty-cards.png) -->

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
CARDNUMBER | = | msdyn\_cardnumber
CARDTENDERTYPE | \>\< | msdyn\_cardtendertype
PARTYNUMBER | = | msdyn\_partynumber
REPLACEMENTCARDNUMBER | \> | msdyn\_replacementcardnumber
OMOPERATINGUNITNUMBER | = | msdyn\_operatingunitnumber
LOYALTYENROLLMENTDATE | = | msdyn\_enrollmentdate

## <a name="payment-schedules"></a>Maksusuunnitelmat

Tämä malli synkronoi sekä asiakkaiden että toimittajien maksusuunnitelmien viitetiedot Finance and Operationsin ja muiden Dynamics 365 -sovellusten välillä.

<!-- ![](media/dual-write-payment-schedules.png) -->

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
NIMI | = | msdyn\_name
KUVAUS | = | msdyn\_description
ALLOCATIONMETHOD | \>\< | msdyn\_allocationmethod
PAYMENTFREQUENCYUNITS | \>\< | msdyn\_paymentfrequencyunit
PAYMENTFREQUENCY | = | msdyn\_paymentfrequency
NUMBEROFPAYMENTS | = | msdyn\_numberofpayments
FIXEDPAYMENTAMOUNT | = | msdyn\_fixedpaymentamount
MINIMUMPAYMENTAMOUNT | = | msdyn\_minimumpaymentamount
SALESTAXALLOCATIONMETHOD | \>\< | msdyn\_salestaxallocationmethod
NOTES | = | msdyn\_note

## <a name="payment-schedule-lines"></a>Maksusuunnitelmarivit

Synkronoi sekä asiakkaiden että toimittajien maksusuunnitelmarivien viitetiedot Finance and Operationsin ja muiden Dynamics 365 -sovellusten välillä.

<!-- ![](media/dual-write-payment-schedule-lines.png) -->

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTSCHEDULENAME | \> | msdyn\_name
LINENUMBER | = | msdyn\_linenumber
PERIODSAFTERDUEDATE | = | msdyn\_periodsafterduedate
PERCENTORAMOUNT | \>\< | msdyn\_percentoramount
PERCENTORAMOUNTVALUE | = | msdyn\_percentoramountvalue

## <a name="payment-days"></a>Maksupäivät

Tämä malli synkronoi sekä asiakkaiden että toimittajien maksupäivien viitetiedot Finance and Operationsin ja muiden Dynamics 365 -sovellusten välillä.

<!-- ![](media/dual-write-payment-days.png) -->

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
NIMI | = | msdyn\_name
KUVAUS | = | msdyn\_description

## <a name="payment-day-lines"></a>Maksupäivärivit

Tämä malli synkronoi sekä asiakkaiden että toimittajien maksupäivärivien viitetiedot Finance and Operationsin ja muiden Dynamics 365 -sovellusten välillä.

<!-- ![](media/dual-write-payment-day-lines.png) -->

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
CDSINTEGRATIONKEY | = | msdyn\_paymentdaylineid
FREQUENCY | \>\< | msdyn\_frequency
DAYOFWEEK | \>\< | msdyn\_dayofweek
DAYOFMONTH | = | msdyn\_dayofmonth
NIMI | = | msdyn\_paymentday.msdyn\_name

## <a name="payment-terms"></a>Maksuehdot

Tämä malli synkronoi sekä asiakkaiden että toimittajien maksuehtojen viitetiedot Finance and Operationsin ja muiden Dynamics 365 -sovellusten välillä.

<!-- ![](media/dual-write-payment-terms.png) -->

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
KUVAUS | = | msdyn\_description
NIMI | = | msdyn\_name
NUMBEROFMONTHS | = | msdyn\_numberofmonth
CUTOFFDAYOFMONTH | = | msdyn\_cutoffdayofmonth
ISCASHPAYMENT | \>\< | msdyn\_iscashpayment
NUMBEROFDAYS | = | msdyn\_days
ISCERTIFIEDCOMPANYCHECK | \>\< | msdyn\_iscertifiedcompanycheck
ISDEFAULTPAYMENTTERM | \>\< | msdyn\_isdefaultpaymentterm
CREDITCARDPAYMENTTYPE | \>\< | msdyn\_creditcardpaymenttype
CREDITCARDCREDITCHECKTYPE | \>\< | msdyn\_creditcardcreditchecktype
PAYMENTDAYNAME | = | msdyn\_paymentdayname.msdyn\_name
PAYMENTMETHODTYPE | \>\< | msdyn\_paymentmethodtype
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedulename.msdyn\_name

## <a name="name-affixes"></a>Nimen jälkiliitteet

Tämä malli synkronoi sekä asiakkaiden että toimittajien nimien jälkiliitteiden viitetiedot Finance and Operationsin ja muiden Dynamics 365 -sovellusten välillä.

<!-- ![](media/dual-write-name-affixes.png) -->

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
AFFIX | = | msdyn\_affix
TYYPPI | \>\< | msdyn\_affixtype
KUVAUS | = | msdyn\_description
