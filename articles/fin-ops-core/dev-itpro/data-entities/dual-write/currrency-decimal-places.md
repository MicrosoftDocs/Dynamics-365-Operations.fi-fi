---
title: Valuutta-tietotyypin siirto kaksoiskirjoitusta varten
description: Tässä ohjeaiheessa käsitellään kaksoiskirjoituksen valuutan osalta tukemien desimaalien määrän muuttamista.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 04/06/2020
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
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 78820ff49958fc3b474038c0fcd126bcf6886d0d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560820"
---
# <a name="currency-data-type-migration-for-dual-write"></a>Valuutta-tietotyypin siirto kaksoiskirjoitusta varten

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Valuutta-arvoissa tuettujen desimaalien määrän voi kasvattaa enintään kymmeneen. Oletusraja on neljä desimaalia. Desimaalien määrää lisäämällä voi estää tietojen menettämisen, kun tietojen synkronointiin käytetään kaksoiskirjoitusta. Desimaalien määrän lisääminen on muutos, joka on hyväksyttävä. Muutoksen tekemiseen tarvitaan Microsoftin apua.

Desimaalien määrään muuttamisessa on kaksi vaihetta:

1. Siirtoa pyydetään Microsoftilta.
2. Desimaalien määrää muutetaan Dataversessa.

Finance and Operations -sovelluksen ja Dataversen on tuettava samaa valuutta-arvojen desimaalimäärää. Muussa tapauksessa tietoja menetetään, kun tietoja synkronoidaan sovellusten välillä. Vaikka siirtoprosessi määrittää uudelleen tavan, jolla valuutta- ja vaihtokurssiarvot tallennetaan, itse tiedot eivät muutu. Kun siirto on valmis, desimaalien määrää voi lisätä valuuttakoodeissa ja hinnoittelussa, minkä lisäksi käyttäjien antamien ja tarkastelemien tietojen desimaalitarkkuus voi parantua.

Siirto on valinnainen toiminto. Jos desimaalien lisäämisestä saattaa olla hyötyä, siirtoa kannattaa harkita. Organisaatioiden, jotka eivät tarvitse yli neljän desimaalin arvoja, ei tarvitse siirtyä.

## <a name="requesting-migration-from-microsoft"></a>Siirron pyytäminen Microsoftilta

Dataversen nykyisten valuuttasarakkeiden tallennustila hyväksyy enintään neljä desimaalia. Tämän vuoksi valuutta-arvot kopioidaan siirtoprosessin aikana tietokannan uusiin, sisäisiin sarakkeisiin. Tämä prosessi jatkuu siihen saakka, että kaikki tiedot on siirretty. Vaikka siirron päätyttyä uudet tallennustilatyypit korvaavat sisäisesti vanhat tallennustilat, tietoarvot eivät ole muuttuneet. Valuuttasarakkeet voivat tämän jälkeen tukea enintään 10 desimaalia. Dataversen käyttöä voi jatkaa siirtoprosessin aikana ilman keskeytyksiä.

Valuuttakursseja muokataan samanaikaisesti siten, että ne tukevat enintään 12 desimaalia nykyisen 10 desimaalin rajan sijaan. Tämä muutos on välttämätön, jotta desimaalien määrä on sama Finance and Operations -sovelluksessa ja Dataversessa.

Siirto ei muuta tietoja millään tavalla. Kun valuutta- ja vaihtokurssisarakkeet on muunnettu, järjestelmänvalvojat voivat määrittää järjestelmän käyttämään valuuttasarakkeissa 10 desimaalia. Se tehdään määrittämällä kunkin tapahtuman valuutan ja hinnoittelun desimaalien määrä.

### <a name="request-a-migration"></a>Siirron pyytäminen

Tämä toiminto saadaan käyttöön lähettämällä sähköpostia osoitteeseen **CDSExpandDecimal@microsoft.com** ja lisäämällä viestiin seuraavat tiedot:

+ **Aihe:** Pyyntö ottaa käyttöön laajennettu desimaalituki organisaatiossa \<organizationID\>
+ **Teksti:** Haluan ottaa käyttöön laajennetun desimaalituen organisaatiossa \<organizationID\>.

Microsoftin edustaja ottaa yhteyttä kahden tai kolmen arkipäivän kuluessa, jonka jälkeen tehdään seuraavat vaiheet.

Kun pyydät siirtoa, seuraavat tiedot on hyvä tiedostaa ja ne on otettava huomioon suunnittelussa:

+ Tietojen siirtämiseen tarvittava aika määräytyy järjestelmässä olevien tietojen mukaan. Suurten tietokantojen siirtäminen voi kestää useita päiviä.
+ Tietokannan koko suurenee tilapäisesti siirron aikana, koska indeksejä varten tarvitaan tilaa. Suurin osa tästä tilasta vapautuu, kun siirto on valmis.
+ Jos siirtoprosessin aikana tapahtuu virhe, joka estää siirron valmistumisen, järjestelmää ilmoittaa siitä Microsoft-tuelle, jotta tukihenkilöstö voi ratkaista ongelma. Dataverse on kuitenkin koko käytettävissä tavalliseen tapaa, vaikka siirron aikana esiintyisi virheitä.
+ Siirtoprosessia ei voi peruuttaa.

## <a name="changing-the-number-of-decimal-places"></a>Desimaalien määrän muuttaminen

Kun siirto on valmis, Dataverse voi tallentaa lukuja, joissa on enemmän desimaaleja. Järjestelmänvalvojat voivat valita, kuinka monta desimaalia tietyissä valuuttakoodeissa ja hinnoittelussa on. Microsoft Power Appsin, Power BI:n ja Power Automaten käyttäjät voivat sitten tarkastella ja käyttää lukuja, joissa on enemmän desimaaleja.

Tämän muutoksen tekeminen edellyttää, että seuraavat Power Appsin asetukset päivitetään:

+ **Järjestelmäasetukset: valuutan tarkkuus hinnoittelussa** – **Määritä desimaalien määrä, jota käytetään hinnoittelussa koko järjestelmässä** -sarake määrittää, miten valuutta reagoi organisaatiossa, kun **Hinnoittelun tarkkuus** on valittu.
+ **Liiketoiminnan hallinta: valuutat** – **Valuutan tarkkuus** -sarakkeessa voi määrittää mukautetun desimaalien määrän tietyn valtuutan osalta. Varmistuksena on paluu koko organisaatiota koskevaan asetukseen.

Rajoituksia:

+ Valuuttasaraketta ei voi määrittää taulussa.
+ Yli neljä desimaalia voidaan määrittää vain **Hinnoittelu**- ja **Tapahtumavaluutta**-tasoilla.

### <a name="system-settings-currency-precision-for-pricing"></a>Järjestelmäasetukset: valuutan tarkkuus hinnoittelussa

Kun siirto on valmis, järjestelmänvalvojat voivat määrittää valuutan tarkkuuden. Valitse ensin **Asetukset \> Hallinta** ja sitten **Järjestelmäasetukset**. Muuta sitten **Yleiset**-välilehden arvo **Määritä desimaalien määrä, jota käytetään hinnoittelussa koko järjestelmässä** -sarakkeessa, kuten seuraavassa kuvassa.

![Valuutan järjestelmäasetukset](media/currency-system-settings.png)

### <a name="business-management-currencies"></a>Liiketoiminta-asiakirjat: valuutat

Jos tietyn valuutan tarkkuuden on erottava hinnoittelussa käytetyn valuutan tarkkuudesta, sitä on muutettava. Valitse ensin **Asetukset \> Liiketoiminnan hallinta** ja sitten **Valuutat** ja muutettava valuutta. Määritä sitten **Valuutan tarkkuus** -sarakkeeseen sopiva desimaalien määrä, mistä on esimerkki seuraavassa kuvassa.

![Tietyn alueen valuutta-asetukset](media/specific-currency.png)

### <a name="tables-currency-column"></a>taulut: Valuutta-sarake

Tiettyihin valuuttasarakkeisiin määritettävien desimaalien määrä on rajoitettu neljään.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]