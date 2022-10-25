---
title: Asynkroninen asiakkaan luontitila
description: Tässä artikkelissa kuvataan asynkronista asiakkaan luontitilaa Microsoft Dynamics 365 Commercessa.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: b2926339021991f87dd3eadef94da3b500c954cf
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690286"
---
# <a name="asynchronous-customer-creation-mode"></a>Asynkroninen asiakkaan luontitila

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan asynkronista asiakkaan luontitilaa Microsoft Dynamics 365 Commercessa.

Commercessa asiakkaan luomisessa on kaksi eri tilaa: Synkroninen ja Asynkroninen. Oletusarvon mukaan asiakkaat luodaan synkronisesti. Toisin sanoen ne luodaan Commerce headquarters -sovelluksessa reaaliaikaisesti. Synkroninen asiakkaan luontitila on hyödyllinen, koska uusia asiakkaita voidaan hakea välittömästi eri kanavien kautta. Sillä on kuitenkin myös haittapuolensa. Koska se luo [Commerce Data Exchange: Real-time Service](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) -kutsuja Commerce headquarters -sovelluksessa, suorituskykyyn voi vaikuttaa, jos tehdään samanaikaisia asiakkaan luontikutsuja.

Jos **Luo asiakas asynkronisessa tilassa** -asetus on **Kyllä** myymälän toimintoprofiilissa (**Retail ja Commerce \> Kanavan asetukset \> Verkkokaupan määritys \> Toimintoprofiilit**), Real-time Service -kutsuja ei käytetä asiakastietueiden luomiseen kanavatietokannassa. Asynroninen asiakkaan luontitila ei vaikuta Commerce headquarters -ohjelman suorituskykyyn. Jokaiselle uudelle asynkroniselle asiakastietueelle liitetään väliaikainen, yleinen yksilöivä tunnus (GUID), jota käytetään asiakastilin tunnuksena. GUID ei näy myyntipisteen (POS) käyttäjille. Sen sijaan käyttäjät näkevät **Odottaa synkronointia** asiakastilin tunnuksena.

> [!IMPORTANT]
> Kun myyntipiste siirtyy offline-tilaan, järjestelmä luo asiakkaat automaattisesti asynkronisesti, vaikka asynkronisen asiakasluonnin tila olisi pois käytöstä. Siksi riippumatta siitä, oletko valinnut synkronisen vai asynkronisen asiakasluonnin, Commerce headquartersin järjestelmänvalvojien on luotava ja ajoitettava toistuva erätyö **P-työlle**, **Synkronoi asiakkaat ja yrityskumppanit asynkronisesta tilasta** -työlle ja **1010**-työlle, jotta kaikki asynkroniset asiakkaat muunnetaan Commerce-pääkonttorissa synkronoiduiksi asiakkaiksi.

## <a name="async-customer-limitations"></a>Asynkronisen asiakkaan rajoitukset

Asynkronisen asiakkaan toiminnallisuuteen liittyy tällä hetkellä seuraava rajoitus:

- Kanta-asiakaskortteja ei voi myöntää asynkronisille asiakkaille, ellei uutta asiakastilitunnusta ole synkronoitu takaisin kanavaan.

## <a name="async-customer-enhancements"></a>Asynkronisen asiakkaan parannukset

Kun haluat auttaa organisaatioita käyttämään asynkronista asiakkaan luontitilaa asiakkaiden hallintaan ja vähentämään reaaliaikaista viestintää Commerce Headquartersin kanssa, on tehty seuraavat parannukset, jotka tuovat pariteetin kanavien synkronisen ja asynkronisen tilan välillä. 

| Ominaisuuksien parannukset | Commerce-versio | Ominaisuuden tiedot |
|---|---|---|
| Suorituskykyä koskevat parannukset, kun asiakastietoja haetaan kanavatietokannasta | 10.0.20 ja sitä uudempi | Suorituskyvyn parantamiseksi asiakasentiteetti jakautuu pienemmiksi entiteeteiksi. Järjestelmä hakee sitten vain tarvittavat tiedot kanavatietokannasta. |
| Kyky luoda osoite asynkronisesti uloskuittauksen aikana | 10.0.22 ja sitä uudempi | <p>Ominaisuusvalitsin: **Asynkronisen luomisen käyttöönotto asiakkaan osoitteissa**</p><p>Ominaisuuden tiedot:</p><ul><li>Kyky lisätä osoitteita ilman reaaliaikaisia palvelukutsuja Commerce headquartersissa</li><li>Mahdollisuus tunnistaa kanavan tietokannan osoitteet yksilöllisesti ilman tietuetunnusta (**RecId**-arvo)</li><li>Ajanseurannan aikaleimat osoitteen luomista varten</li><li>Osoitteiden synkronointi Commerce headquartersissa</li></ul><p>Tämä ominaisuus vaikuttaa sekä synkronoituihin että asynkronoituihin asiakkaisiin. Jos haluat muokata osoitteita asynkronisesti sekä luoda ne asynkronisesti, ota käyttöön **asiakkaiden muokkaaminen asynkronisessa tilassa**.</p> |
| Ota käyttöön pariteetti synkronisen ja asynkronisen asiakkaan luonnin välillä. | 10.0.24 ja sitä uudempi | <p>Ominaisuusvalitsin: **Ota käyttöön laajennettu asynkronisen asiakkaan luonti**</p><p>Ominaisuuksien tiedot: Mahdollisuus siepata lisätietoja, kuten otsikko, liitokset oletusasiakkaalta sekä toissijaiset yhteystiedot (puhelinnumero ja sähköpostiosoite), kun asiakkaita luodaan asynkronisesti</p> |
| Käyttäjäystävälliset virhesanomat | 10.0.28 ja sitä uudempi | Nämä parannukset auttavat parantamaan käyttäjäystävällisiä virhesanomia, jos käyttäjä ei voi muokata tietoja heti synkronoinnin aikana. Voit ottaa nämä parannukset käyttöön käyttämällä **Salli se, että asynkroninen asiakas ei voi muokata tiettyjä käyttöliittymäelementtejä** -asetusta kohdassa **Sivuston asetukset \> Laajennukset** Commercen sivustonmuodostimessa. |
| Mahdollisuus muokata asiakastietoja asynkronisesti | 10.0.29 ja sitä uudempi | <p>Ominaisuusvalitsin: **Ota käyttöön asiakkaiden muokkaaminen asynkronisessa tilassa**</p><p>Ominaisuuksien tiedot: Mahdollisuus muokata asiakastietoja asynkronisesti</p><p>Vastauksia yleisiin kysymyksiin, jotka liittyvät asiakastietojen asynkroniseen muokkaamiseen, on kohdassa [Asynkroninen asiakkaan luontitila – Usein kysytyt kysymykset](async-customer-mode-faq.md).</p> |
| Asiakkaiden hallintatoimintojen synkronisoinnin tarkistusmahdollisuus | 10.0.31 ja sitä uudempi | Tämän parannuksen avulla käyttäjät voivat tarkistaa asiakkaiden hallintatoimintojen synkronoinnin Commerce headquartersissa. Lisäksi käyttäjät voivat tarvittaessa tehdä muutoksia ja synkronoida tiedot. |

### <a name="feature-switch-hierarchy"></a>Ominaisuusvalitsimen hierarkia

Ominaisuusvalitsimien hierarkian vuoksi seuraavat toiminnot on otettava käyttöön ennen **Ota käyttöön asiakkaiden muokkaaminen asynkronisessa tilassa** -ominaisuuden ottamista käyttöön: 

- **Asiakastilausten ja -tapahtumien suorituskyvyn parannukset** – Tämä ominaisuus on ollut pakollinen Commerce-version 10.0.28 julkaisun jälkeen. 
- **Ota käyttöön laajennettu asynkronisen asiakkaan luonti**
- **Asynkronisen luomisen käyttöönotto asiakkaan osoitteissa**

Vastaukset yleisiin vianmäärityskysymyksiin on kohdassa [Asynkroninen asiakkaan luontitila – Usein kysytyt kysymykset](async-customer-mode-faq.md). 

Kun olet ottanut aiemmin mainitut ominaisuudet käyttöön, sinun on ajoitettava toistuva erätyö **P-työlle**, **Synkronoi asiakkaat ja liikekumppanit asynkronisesta tilasta** -työlle ja **1010**-työlle, jotta kaikki asynkroniset asiakkaat muunnetaan synkronointiasiakkaiksi Commerce headquartersissa.

### <a name="customer-creation-in-pos-offline-mode"></a>Asiakkaan luonti myyntipisteen offline-tilassa

Kuten aiemmin mainittiin, kun myyntipiste siirtyy offline-tilaan, järjestelmä luo asiakkaat automaattisesti asynkronisesti, vaikka asynkronisen asiakasluonnin tila olisi pois käytöstä. Siksi Commerce headquartersin järjestelmänvalvojien on luotava ja ajoitettava toistuva erätyö **P-työlle**, **Synkronoi asiakkaat ja yrityskumppanit asynkronisesta tilasta** -työlle ja **1010**-työlle, jotta kaikki asynkroniset asiakkaat muunnetaan Commerce headquartersissa synkronoiduiksi asiakkaiksi.

> [!NOTE]
> Jos **Suodata jaetut asiakastietotalut** -asetus on **Kyllä** **Commerce-kanavan rakenne** -sivulla (**Retail ja Commerce \> Headquartersin asetuukset \> Commerce-ajastus \> Kanavan tietokantaryhmä**), asiakastietueita ei luoda myyntipisteen offline-tilassa. Lisätietoja on kohdassa [Offline-tietojen poissulkeminen](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Lisäresurssit

[Myymälöiden asiakashallinta](customer-mgmt-stores.md)

[Asynkronisten asiakkaiden muuntaminen synkronisiksi asiakkaiksi](convert-async-to-sync.md)

[Asiakkaan määritteet](dev-itpro/customer-attributes.md)

[Offline-tietojen poissulkeminen](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
