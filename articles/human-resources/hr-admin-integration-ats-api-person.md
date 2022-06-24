---
title: Henkilö
description: Tässä artikkelissa kuvataan Dynamics 365 Human Resourcesin Henkilö-yksikköä.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 49d9b5e1a1297c9528bfa82d0e8307bad3b2d1cc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864109"
---
# <a name="person"></a>Henkilö


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa kuvataan Dynamics 365 Human Resourcesin Henkilö-yksikköä.

Fyysinen nimi: mshr_dirpersonentity

### <a name="description"></a>kuvaus

Tämä yksikkö antaa hakijan henkilökohtaiset tiedot.

## <a name="json-representation"></a>JSON-esitys

```json
{
    "mshr_partynumber": "String",
    "mshr_name": "String",
    "mshr_namealias": "String",
    "mshr_knownas": "String",
    "mshr_languageid": "String",
    "mshr_addressbooks": "String",
    "mshr_anniversaryday": Int,
    "mshr_anniversarymonth": Int,
    "mshr_anniversaryyear": Int,
    "mshr_birthday": Int,
    "mshr_birthmonth": Int,
    "mshr_birthyear": Int,
    "mshr_childrennames": "String",
    "mshr_gender": Int,
    "mshr_hobbies": "String",
    "mshr_initials": "String",
    "mshr_maritalstatus": Int,
    "mshr_phoneticfirstname": "String",
    "mshr_phoneticlastname": "String",
    "mshr_phoneticmiddlename": "String",
    "mshr_personalsuffix": "String",
    "mshr_personaltitle": "String",
    "mshr_professionalsuffix": "String",
    "mshr_professionaltitle": "String",
    "mshr_fullprimaryaddress": "String",
    "mshr_addresscity": "String",
    "mshr_addresscountryregionid": "String",
    "mshr_addresscountryregionisocode": "String",
    "mshr_addresscounty": "String",
    "mshr_addressdistrictname": "String",
    "mshr_addresslatitude": Decimal,
    "mshr_addresslocationid": "000003212",
    "mshr_addresslocationroles": "Home",
    "mshr_addresslongitude": Decimal,
    "mshr_addressstate": "String",
    "mshr_addressstreet": "String",
    "mshr_addressvalidfrom": "Date",
    "mshr_addressvalidto": "Date",
    "mshr_addresszipcode": "String",
    "mshr_addressisprivate": Int,
    "mshr_addressdescription": "String",
    "mshr_primarycontactemail": "String",
    "mshr_primarycontactemaildescription": "String",
    "mshr_primarycontactemailisim": Int,
    "mshr_primarycontactemailpurpose": "String",
    "mshr_primarycontactfax": "String",
    "mshr_primarycontactfaxdescription": "String",
    "mshr_primarycontactfaxextension": "String",
    "mshr_primarycontactfaxpurpose": "String",
    "mshr_primarycontactphone": "String",
    "mshr_primarycontactphonedescription": "String",
    "mshr_primarycontactphoneextension": "String",
    "mshr_primarycontactphoneismobile": Int,
    "mshr_primarycontactphonepurpose": "String",
    "mshr_primarycontacttelex": "String",
    "mshr_primarycontacttelexdescription": "String",
    "mshr_primarycontacttelexpurpose": "String",
    "mshr_primarycontacturl": "String",
    "mshr_primarycontacturldescription": "String",
    "mshr_primarycontacturlpurpose": "String",
    "mshr_primarycontactfacebook": "String",
    "mshr_primarycontactfacebookdescription": "String",
    "mshr_primarycontactfacebookisprivate": Int,
    "mshr_primarycontactfacebookpurpose": "String",
    "mshr_primarycontactlinkedin": "String",
    "mshr_primarycontactlinkedindescription": "String",
    "mshr_primarycontactlinkedinisprivate": Int,
    "mshr_primarycontactlinkedinpurpose": "String",
    "mshr_primarycontacttwitter": "String",
    "mshr_primarycontacttwitterdescription": "String",
    "mshr_primarycontacttwitterisprivate": Int,
    "mshr_primarycontacttwitterpurpose": "String",
    "mshr_partytype": "String",
    "mshr_namesequencedisplayas": "String",
    "mshr_firstname": "String",
    "mshr_lastnameprefix": "String",
    "mshr_lastname": "String",
    "mshr_middlename": "String",
    "mshr_electroniclocationid": "String",
    "mshr_dirpersonentityid": "Guid",
    "mshr_addresstimezone": Int
}
```

## <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Henkilön yksikkötunnus**<br>mshr_dirpersonentityid<br>*GUID* | Vain luku<br>Vaadittu<br>Järjestelmän luoma | Järjestelmän luoma yksikkötietueen yksilöivä tunnus. |
| **Osapuolinumero**<br>mshr_partynumber<br>*Merkkijono* | Vain luku<br>Vaadittu<br>Järjestelmän luoma | Käyttäjän luettava, järjestelmän luoma henkilön yksilöivä tunnus.  |
| **Nimi**<br>mshr_name<br>*Merkkijono* | Vain luku<br>Vaadittu | Kentän arvo on etunimen, toisen nimen, sukunimen etuliitteen ja sukunimen ketjutettu merkkitjono **Nimien järjestys – näytä muodossa** -kentässä määritetyssä järjestyksessä. |
| **Nimen alias**<br>mshr_namealias<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilölle annettu nimen alias. |
| **Tunnetaan nimellä**<br>mshr_knownas<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön nimi, jota voidaan käyttää, jos se yleensä tunnetaan toisena nimenä. |
| **Kielitunnus**<br>mshr_languageid<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaisen kielen kielitunnus ISO 639-1 -muodossa määritetyssä muodossa. |
| **Osoitekirjat**<br>mshr_addressbooks<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Osoitekirja, johon henkilö voidaan liittää. Organisaatiolle määritettävät osoitekirjat luetellaan mshr_diraddressbooksentity-yksikössä. |
| **Vuosipäivän päivä**<br>mshr_anniversaryday<br>*Int* | Luku/Kirjoitus<br>Valinnainen | Henkilön vuosipäivän päivämäärä. |
| **Vuosipäivän kuukausi**<br>mshr_anniversarymonth<br>*mshr_monthsofyear-asetusjoukko* | Luku/Kirjoitus<br>Valinnainen | Henkilön vuosipäivän kuukausi. |
| **Vuosipäivän vuosi**<br>mshr_anniversaryyear<br>*Int* | Luku/Kirjoitus<br>Valinnainen | Henkilön vuosipäivän vuosi. |
| **Syntymäpäivä**<br>mshr_birthday<br>*Int* | Luku/Kirjoitus<br>Valinnainen | Henkilön syntymäpäivän päivämäärä. |
| **Syntymäkuukausi**<br>mshr_birthmonth<br>*mshr_monthsofyear-asetusjoukko* | Luku/Kirjoitus<br>Valinnainen | Henkilön syntymäpäivän kuukausi. |
| **Syntymävuosi**<br>mshr_birthyear<br>*Int* | Luku/Kirjoitus<br>Valinnainen | Henkilön syntymäpäivän vuosi. |
| **Lasten nimet**<br>mshr_childrennames<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Merkkijono henkilön lasten nimiä varten. Vaadittua erotinta ei ole. |
| **Sukupuoli**<br>mshr_gender<br>*mshr_hcmpersongender-asetusjoukko* | Luku/Kirjoitus<br>Valinnainen | Henkilön sukupuoli. |
| **Harrastukset**<br>mshr_hobbies<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön harrastukset. |
| **Nimikirjaimet**<br>mshr_initials<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön nimen alkukirjaimet. |
| **Siviilisääty**<br>mshr_maritalstatus<br>*mshr_hcmpersonmaritalstatus-asetusjoukko* | Luku/Kirjoitus<br>Valinnainen | Henkilön siviilisääty. |
| **Foneettinen etunimi**<br>mshr_phoneticfirstname<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön etunimen foneettinen ääntämys. |
| **Foneettinen sukunimi**<br>mshr_phoneticlastname<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön sukunimen foneettinen ääntämys. |
| **Foneettinen toinen nimi**<br>mshr_phoneticmiddlename<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön sukunimen foneettinen ääntämys. |
| **Nimen jälkiliite**<br>mshr_personalsuffix<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön henkilökohtainen loppuliite. mshr_dirnameaffixentity-yksikön kelvolliset arvot, joissa mshr_type on Suffix (200000001). |
| **Henkilön nimike**<br>mshr_personaltitle<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön henkilökohtainen titteli. mshr_dirnameaffixentity-yksikön kelvolliset arvot, joissa mshr_type on Title (200000000).
| **Ammattiloppuliite**<br>mshr_professionalsuffix<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Ammattiloppuliite. |
| **Ammattinimike**<br>mshr_professionaltitle<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Ammattinimike. |
| **Täydellinen ensisijainen osoite**<br>mshr_fullprimaryaddress<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön täydellinen ensisijainen osoite, ensisijaisten osoitekenttien ketjutus. |
| **Osoitteen kaupunki**<br>mshr_addresscity<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaisen osoitteen kaupunki. Määritetään mshr_logisticsaddresscityentity-yksikössä. |
| **Osoitteen maa/alue**<br>mshr_addresscountryregionid<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaisen osoitteen maa/alue. Kelvolliset arvot mshr_logisticsaddresscountryregionentity-yksikössä. |
| **Osoitteen maan/alueen ISO-koodi**<br>mshr_addresscountryregionisocode<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaisen osoitteen maan/alueen ISO-koodi. |
| **Osoitteen maakunta**<br>mshr_addresscounty<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaisen osoitteen maakunta. Määritetään mshr_logisticsaddresscountyentity-yksikössä. |
| **Osoitteen alueen nimi**<br>mshr_addressdistrictname<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaisen osoitteen alue. Määritetään mshr_logisticsaddressdistrictentity-yksikössä. |
| **Osoitteen leveysaste**<br>mshr_addresslatitude<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaisen osoitteen leveysaste. |
| **Osoitteen sijainnin tunnus**<br>mshr_addresslocationid<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaisen osoitteen sijainnin yksilöivä tunnus. Kelvolliset arvot mshr_logisticspostaladdresslocationcdsentity-yksikössä. |
| **Osoitteen sijainnin roolit**<br>mshr_addresslocationroles<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaisen osoitteen sijainnin rooli. Määritetään mshr_logisticslocationrolecdsentity-yksikössä. |
| **Osoitteen pituusaste**<br>mshr_addresslongitude<br>*Merkkijono* |  Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaisen osoitteen pituusaste. |
| **Osoitteen osavaltio**<br>mshr_addressstate<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaisen osoitteen osavaltio. Määritetään mshr_logisticsaddressstateentity-yksikössä. |
| **Osoitteen katuosoite**<br>mshr_addressstreet<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaisen osoitteen katuosoite. |
| **Osoite voimassa alkaen**<br>mshr_addressvalidfrom<br>*Päivämäärä* | Luku/Kirjoitus<br>Valinnainen | Päivämäärä, josta alkaen henkilön ensisijainen osoite on voimassa. |
| **Osoite voimassa asti**<br>mshr_addressvalidto<br>*Päivämäärä* | Luku/Kirjoitus<br>Valinnainen | Päivämäärä, johon asti henkilön ensisijainen osoite on voimassa. |
| **Osoitteen postinumero**<br>mshr_addresszipcode<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaisen osoitteen postinumero. Määritetään mshr_logisticsaddresspostalcodeentity-yksikössä. |
| **Osoite on yksityinen**<br>mshr_addressisprivate<br>*mshr_noyes-asetusjoukko* | Luku/Kirjoitus<br>Valinnainen | Määrittää, jaetaanko henkilön ensisijainen osoite organisaation muiden käyttäjien kanssa. |
| **Osoitteen kuvaus**<br>mshr_addressdescription<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaisen osoitteen kuvaus. |
| **Ensisijainen yhteyshenkilön sähköposti**<br>mshr_primarycontactemail<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijainen sähköpostiosoite. |
| **Yhteyshenkilön ensisijaisen sähköpostin kuvaus**<br>mshr_primarycontactemaildescription<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Ensisijaista sähköpostiosoitetta varten annettu kuvaus. |
| **Ensisijainen yhteyshenkilön sähköposti on IM**<br>mshr_primarycontactemailisim<br>*mshr_noyes-asetusjoukko* | Luku/Kirjoitus<br>Valinnainen | Määrittää, onko ensisijainen sähköpostiosoite käytettävissä pikasanomia varten. |
| **Yhteyshenkilön ensisijaisen sähköpostin tarkoitus**<br>mshr_primarycontactemailpurpose<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Ensisijaisen sähköpostiosoitteen tarkoitus. Määritetään mshr_logisticslocationroleentity-yksikössä. |
| **Yhteyshenkilön ensisijainen faksi**<br>mshr_primarycontactfax<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Ensisijainen faksinumero. |
| **Yhteyshenkilön ensisijaisen faksin kuvaus**<br>mshr_primarycontactfaxdescription<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Ensisijaista faksinumeroa varten annettu kuvaus. |
| **Yhteyshenkilön ensisijaisen faksin alanumero**<br>mshr_primarycontactfaxextension<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Ensisijaisen faksinumeron alanumero. |
| **Yhteyshenkilön ensisijaisen faksin tarkoitus**<br>mshr_primarycontactfaxpurpose<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Ensisijaisen faksinumeron tarkoitus. Määritetään mshr_logisticslocationroleentity-yksikössä.
| **Yhteyshenkilön ensisijainen puhelin**<br>mshr_primarycontactphone<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Ensisijainen puhelinnumero. |
| **Yhteyshenkilön ensisijaisen puhelinnumeron kuvaus**<br>mshr_primarycontactphonedescription<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Ensisijaista puhelinnumeroa varten annettu kuvaus. |
| **Yhteyshenkilön ensisijaisen puhelimen alanumero**<br>mshr_primarycontactphoneextension<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Ensisijaisen puhelinnumeron alanumero. |
| **Yhteyshenkilön ensisijainen puhelin on matkapuhelin**<br>mshr_primarycontactphoneismobile<br>*mshr_noyes-asetusjoukko* | Luku/Kirjoitus<br>Valinnainen | Määrittää, onko ensisijainen puhelinnumero matkapuhelin. |
| **Yhteyshenkilön ensisijaisen puhelinnumeron tarkoitus**<br>mshr_primarycontactphonepurpose<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Ensisijaisen puhelinnumeron tarkoitus. Määritetään mshr_logisticslocationroleentity-yksikössä. |
| **Yhteyshenkilön ensisijainen teleksi**<br>mshr_primarycontacttelex<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Ensisijainen teleksinumero. |
| **Yhteyshenkilön ensisijaisen teleksin kuvaus**<br>mshr_primarycontacttelexdescription<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaista teleksinumeroa varten annettu kuvaus. |
| **Yhteyshenkilön ensisijaisen teleksin tarkoitus**<br>mshr_primarycontacttelexpurpose<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaisen teleksinumeron tarkoitus. Määritetään mshr_logisticslocationroleentity-yksikössä. |
| **Yhteyshenkilön ensisijainen URL**<br>mshr_primarycontacturl<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Ensisijainen URL-osoite. |
| **Yhteyshenkilön ensisijaisen URL-osoitteen kuvaus**<br>mshr_primarycontacturldescription<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaisen URL-osoitteen kuvaus. |
| **Yhteyshenkilön ensisijaisen URL-osoitteen tarkoitus**<br>mshr_primarycontacturldescription<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaisen URL-osoitteen tarkoitus. Määritetään mshr_logisticslocationroleentity-yksikössä. |
| **Yhteyshenkilön ensisijainen Facebook-tili**<br>mshr_primarycontactfacebook<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Ensisijainen Facebook-tili. Tunnistetaan käyttäjätunnuksen avulla. |
| **Yhteyshenkilön ensisijaisen Facebook-tilin kuvaus**<br>mshr_primarycontactfacebookdescription<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaisen Facebook-tilin kuvaus. |
| **Yhteyshenkilön ensisijainen Facebook-tili on yksityinen**<br>mshr_primarycontactfacebookisprivate<br>*mshr_noyes-asetusjoukko* | Luku/Kirjoitus<br>Valinnainen | Määrittää, näkyykö ensisijainen Facebook-tili muille käyttäjille. |
| **Yhteyshenkilön ensisijaisen Facebook-tilin tarkoitus**<br>mshr_primarycontactfacebookpurpose<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaisen Facebook-tilin tarkoitus. Määritetään mshr_logisticslocationroleentity-yksikössä. |
| **Yhteyshenkilön ensisijainen LinkedIn-tili**<br>mshr_primarycontactlinkedin<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Ensisijainen LinkedIn-tili. Tunnistetaan käyttäjänimen avulla. |
| **Yhteyshenkilön ensisijaisen LinkedIn-tilin kuvaus**<br>mshr_primarycontactlinkedindescription<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaisen LinkedIn-tilin kuvaus. |
| **Yhteyshenkilön ensisijainen LinkedIn-tili on yksityinen**<br>mshr_primarycontactlinkedinisprivate<br>*mshr_noyes-asetusjoukko* | Luku/Kirjoitus<br>Valinnainen | Määrittää, jaetaanko henkilön ensisijaisen LinkedIn-tilin tiedot muiden käyttäjien kanssa. |
| **Yhteyshenkilön ensisijaisen LinkedIn-tilin tarkoitus**<br>mshr_primarycontactlinkedinpurpose<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaisen LinkedIn-tilin tarkoitus. Määritetään mshr_logisticslocationroleentity-yksikössä. |
| **Yhteyshenkilön ensisijainen Twitter-tili**<br>mshr_primarycontacttwitter<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijainen Twitter-tili. Tunnistetaan @käyttäjänimen avulla. |
| **Yhteyshenkilön ensisijaisen Twitter-tilin kuvaus**<br>mshr_primarycontacttwitterdescription<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaisen Twitter-tilin kuvaus. |
| **Yhteyshenkilön ensisijainen Twitter-tili on yksityinen**<br>mshr_primarycontacttwitterisprivate<br>*mshr_noyes-asetusjoukko* | Luku/Kirjoitus<br>Valinnainen | Määrittää, jaetaanko henkilön ensisijaisen Twitter-tilin tiedot muiden käyttäjien kanssa. |
| **Yhteyshenkilön ensisijaisen Twitter-tilin tarkoitus**<br>mshr_primarycontacttwitterpurpose<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaisen Twitter-tilin tarkoitus. Määritetään mshr_logisticslocationroleentity-yksikössä. |
| **Osapuolen tyyppi**<br>mshr_partytype<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön osapuolityyppi. Ehdokkailla arvo on aina **Henkilö**. |
| **Nimien järjestys – näytä muodossa**<br>mshr_namesequencedisplayas<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Järjestys, jossa henkilön nimen ominaisuudet on ketjutettu ominaisuuden Name (mshr_name) arvoksi. |
| **Etunimi**<br>mshr_firstname<br>*Merkkijono* | Luku/Kirjoitus<br>Vaadittu | Henkilön etunimi. |
| **Toinen nimi**<br>mshr_middlename<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön toinen nimi. |
| **Sukunimen etuliite**<br>mshr_lastnameprefix<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön sukunimen etuliite. |
| **Sukunimi**<br>mshr_lastname<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön sukunimi. |
| **Sähköisen sijainnin tunnus**<br>mshr_electroniclocationid<br>*Merkkijono* | Luku/Kirjoitus<br>Valinnainen | Henkilön sähköisen sijainnin tunnus. |
| **Osoitteen aikavyöhyke**<br>mshr_addresstimezone<br>*Int* | Luku/Kirjoitus<br>Valinnainen | Henkilön ensisijaisen osoitteen aikavyöhyke. |

## <a name="see-also"></a>Lisätietoja

[Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely](hr-admin-integration-ats-api-introduction.md)<br>
[Esimerkkikysely palkattavalle hakijalle](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
