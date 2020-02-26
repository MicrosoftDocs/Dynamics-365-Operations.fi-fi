---
title: Common Data Service -yksiköt
description: Microsoft Dynamics 365 Human Resources käyttää Common Data Serviceä laajennettavuuden ja integroinnin skenaarioiden mahdollistamiseksi.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 85dd95e8209fff28f214986f7960372db200351b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008931"
---
# <a name="common-data-service-entities"></a>Common Data Service -yksiköt

Microsoft Dynamics 365 Human Resources käyttää Common Data Serviceä laajennettavuuden ja integroinnin skenaarioiden mahdollistamiseksi.

Lisätietoja Common Data Servicestä on kohdassa [Mikä on Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro) .

Seuraavat henkilöstöhallinnon resurssiyksiköt ovat käytettävissä Common Data Servicessä.

## <a name="benefit-entities"></a>Etuyksiköt

**Edun laskentatiheys**

| **Kentät**        | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|-------------------|---------------|--------------|----------------|
| Kuvaus       | Text          |              | X              |
| Toistuvuuden hallinta | Asetusjoukko    | X            | X              |
| On pysyvä      | Kaksi vaihtoehtoa   |              | X              |
| Nimi              | Text          | X            | X              |


**Edun laskentahinta**

| **Kentät**  | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|-------------|---------------|--------------|----------------|
| Kuvaus | Text          |              | X              |
| Nimi        | Text          | X            | X              |
| TierType    | Asetusjoukko    | X            | X              |


**Edun laskentahinnan tiedot**

| **Kentät**                             | **Tietotyyppi**  | **Vaadittu** | **Etsittävissä** |
|----------------------------------------|----------------|--------------|----------------|
| Edun laskentahinnan tietojen numero | Text           | X            | X              |
| Laskelman hintatunnus                    | Haku         | X            | X              |
| Osuusmenetelmä                    | Asetusjoukko     | X            | X              |
| Voimassa                              | Vain päivämäärä      | X            | X              |
| Työnantajan osuus                  | Desimaalinumero |              | X              |
| Vanhentumisaika                             | Vain päivämäärä      | X            | X              |
| WorkerDeduction                        | Desimaalinumero |              | X              |


**Edun tyyppi**

| **Kentät**           | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|----------------------|---------------|--------------|----------------|
| ConcurrentEnrollment | Asetusjoukko    |              | X              |
| Kuvaus          | Text          |              | X              |
| Nimi                 | Text          | X            | X              |
| PayrollCategory      | Asetusjoukko    |              | X              |


**Etuussuunnitelma**

| **Kentät**                               | **Tietotyyppi**  | **Vaadittu** | **Etsittävissä** |
|------------------------------------------|----------------|--------------|----------------|
| Velvoitteen rajoitusmenetelmä                      | Asetusjoukko     |              | X              |
| Edun tyyppi                             | Haku         | X            | X              |
| Osuuden rajoitusmenetelmä                | Asetusjoukko     |              | X              |
| Osuusmenetelmä                      | Asetusjoukko     |              | X              |
| Valuutta                                 | Haku         |              | X              |
| Vähennyksen prioriteetti                       | Koko numero   |              | X              |
| Oletusosuuden rajan summa        | Valuutta       |              | X              |
| Oletusosuusrajan summa | Valuutta       |              | X              |
| Osuuden rajan oletusjakso        | Asetusjoukko     |              | X              |
| Oletusvähennyksen rajan summa           | Valuutta       |              | X              |
| Oletusvähennysrajan summa    | Valuutta       |              | X              |
| Vähennyksen rajan oletusjakso           | Asetusjoukko     |              | X              |
| Kuvaus                              | Text           |              | X              |
| Vaihtokurssi                            | Desimaalinumero |              | X              |
| On lisäpalkanlaskenta                | Kaksi vaihtoehtoa    |              | X              |
| On Affordable Care Act -raportoitava        | Kaksi vaihtoehtoa    |              | X              |
| On velvoite luotu                      | Kaksi vaihtoehtoa    |              | X              |
| On brutto                              | Kaksi vaihtoehtoa    |              | X              |
| On ensisijainen                               | Kaksi vaihtoehtoa    |              | X              |
| Nimi                                     | Text           | X            | X              |
| Palkanlaskentavaikutus                           | Asetusjoukko     |              | X              |
| Eläkkeelle siirtymisen tyyppi                          | Asetusjoukko     |              | X              |


**Työsuhdeyksikkö**

| **Kentät**                     | **Tietotyyppi**  | **Vaadittu** | **Etsittävissä** |
|--------------------------------|----------------|--------------|----------------|
| Mukautettu työntekijän aloituspäivämäärä     | Päivämäärä ja aika  |              | X              |
| Yritys                         | Haku         | X            | X              |
| Työnantajan ilmoituksen yksikön summa | Desimaalinumero |              | X              |
| Työnantajan ilmoituksen yksikkö        | Asetusjoukko     |              | X              |
| Työsuhteen päättymispäivämäärä            | Päivämäärä ja aika  |              | X              |
| Työllisyysluku              | Text           | X            | X              |
| Työsuhteen alkamispäivä          | Päivämäärä ja aika  |              | X              |
| Viimeinen työpäivä              | Päivämäärä ja aika  |              | X              |
| Siirtopäivämäärä                | Päivämäärä ja aika  |              | X              |
| Voimassaolo alkaa                     | Päivämäärä ja aika  | X            | X              |
| Voimassaolo päättyy                       | Päivämäärä ja aika  |              | X              |
| Työntekijä                         | Haku         | X            | X              |
| Työntekijän ilmoitusten määrä           | Desimaalinumero |              | X              |
| Työntekijän aloituspäivämäärä             | Päivämäärä ja aika  |              | X              |
| Työntekijätyyppi                    | Asetusjoukko     | X            | X              |
| Työntekijän ilmoituksen yksikkö          | Asetusjoukko     |              | X              |

## <a name="worker-entities"></a>Työntekijäyksiköt

**Etninen tausta**

| **Kentät**         | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|--------------------|---------------|--------------|----------------|
| Kuvaus        | Text          |              | X              |
| Etninen taustanimi | Text          | X            | X              |


**Kieli**

| **Kentät**    | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|---------------|---------------|--------------|----------------|
| Kuvaus   | Text          |              | X              |
| Kielen nimi | Text          | X            | X              |


**Sotaveteraanitila**

| **Kentät**           | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|----------------------|---------------|--------------|----------------|
| Kuvaus          | Text          |              | X              |
| On suojattu veteraani | Kaksi vaihtoehtoa    |              | X              |
| Kielen nimi        | Text          | X            | X              |


**Työntekijä**

| **Kentät**                | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|---------------------------|---------------|--------------|----------------|
| Syntymäpäivämäärä                 | Vain päivämäärä     |              | X              |
| Kuvaus               | Text          |              | X              |
| Sähköpostiosoite 1           | Sähköposti         |              | X              |
| Sähköpostiosoite 2           | Sähköposti         |              | X              |
| Facebook-käyttäjätiedot         | Text          |              | X              |
| Etunimi                | Text          |              | X              |
| Koko nimi                 | Text          |              | X              |
| Sukupuoli                    | Asetusjoukko    |              | X              |
| Luonti                | Text          |              | X              |
| On yhteyshenkilön sähköpostiosoite sallittu  | Kaksi vaihtoehtoa   |              | X              |
| On yhteyshenkilön puhelinnumero sallittu  | Kaksi vaihtoehtoa   |              | X              |
| Sukunimi                 | Text          |              | X              |
| LinkedIn-käyttäjätiedot         | Text          |              | X              |
| Esimies                   | Haku        |              | X              |
| Toinen nimi               | Text          |              | X              |
| Matkapuhelin              | Puhelinnumero         |              | X              |
| Office Graph -tunniste   | Text          |              | X              |
| Ensisijainen sähköpostiosoite     | Sähköposti         |              | X              |
| Ensisijainen puhelin         | Puhelinnumero         |              | X              |
| Ammatti                | Text          |              | X              |
| Sosiaalinen verkko 1          | Asetusjoukko    |              | X              |
| Sosiaalinen verkko 2          | Asetusjoukko    |              | X              |
| Yhteisöpalvelun käyttäjätiedot 1 | Text          |              | X              |
| Yhteisöpalvelun käyttäjätiedot 2 | Text          |              | X              |
| Lähde                    | Asetusjoukko    | X            | X              |
| Tila                    | Asetusjoukko    | X            | X              |
| Puhelin 1               | Puhelinnumero         |              | X              |
| Puhelin 2               | Puhelinnumero         |              | X              |
| Puhelin 3               | Puhelinnumero         |              | X              |
| Twitter-identiteetti          | Text          |              | X              |
| Käyttäjä                      | Haku        |              | X              |
| Internet-sivuston URL               | URL-osoite           |              | X              |
| Työntekijänumero             | Text          | X            | X              |
| Työntekijätyyppi               | Asetusjoukko    | X            | X              |
| Yomi-etunimi           | Text          |              | X              |
| Yomi-koko nimi            | Text          |              | X              |
| Yomi-sukunimi            | Text          |              | X              |
| Yomi-toinen nimi          | Text          |              | X              |


**Työntekijän osoite**

| **Kentät**           | **Tietotyyppi**  | **Vaadittu** | **Etsittävissä** |
|----------------------|----------------|--------------|----------------|
| Osoitteen numero       | Text           | X            | X              |
| Osoitteen tyyppi         | Asetusjoukko     | X            | X              |
| Paikkakunta                 | Text           |              | X              |
| Maa tai alue    | Text           |              | X              |
| Piirikunta               | Text           |              | X              |
| Faksi                  | Puhelinnumero          |              | X              |
| On ensisijainen         | Kaksi vaihtoehtoa    |              | X              |
| Leveyspiiri             | Desimaalinumero |              | X              |
| Rivi 1               | Text           |              | X              |
| Rivi 2               | Text           |              | X              |
| Rivi 3               | Text           |              | X              |
| Pituuspiiri            | Desimaalinumero |              | X              |
| Postinumero          | Text           |              | X              |
| Postilokero      | Text           |              | X              |
| Toimitustapakoodi | Koko numero   |              | X              |
| Osavaltio tai provinssi    | Text           |              | X              |
| Puhelin 1          | Puhelinnumero          |              | X              |
| Puhelin 2          | Puhelinnumero          |              | X              |
| Puhelin 3          | Puhelinnumero          |              | X              |
| UPS-vyöhyke             | Text           |              | X              |
| UTC-poikkeama           | Koko numero   |              | X              |
| Työntekijä               | Haku         | X            | X              |


**Työntekijän henkilötiedot**

| Kentät                             | Tietotyyppi    | Tarvitaan | Etsittävissä |
|------------------------------------|--------------|----------|------------|
| Syntymäkaupunki                         | Text         |          | X          |
| Syntymämaa tai -alue            | Asetusjoukko   |          | X          |
| Syntymäpäivämäärä                          | Vain päivämäärä    |          | X          |
| Kansalaisuus, maa tai alue      | Asetusjoukko   |          | X          |
| Kuolinpäivämäärä                      | Vain päivämäärä    |          | X          |
| Käytöstä poistettu veteraanitarkistuspäivämäärä | Vain päivämäärä    |          | X          |
| Koulutus                          | Text         |          | X          |
| Etninen tausta                     | Haku       |          | X          |
| ExpatriateEndDate                  | Vain päivämäärä    |          | X          |
| ExpatriateStartDate                | Vain päivämäärä    |          | X          |
| Isän syntymämaa tai -alue     | Asetusjoukko   |          | X          |
| Sukupuoli                             | Asetusjoukko   |          | X          |
| On käytöstä poistettu                        | Kaksi vaihtoehtoa  |          | X          |
| On sotainvalidi                | Kaksi vaihtoehtoa  |          | X          |
| Soveltuuko ekspatriaattisääntö tilanteeseen    | Kaksi vaihtoehtoa  |          | X          |
| On kokoaikainen opiskelija               | Kaksi vaihtoehtoa  |          | X          |
| Siviilisääty                     | Asetusjoukko   |          | X          |
| Sotilaspalveluksen päättymispäivämäärä          | Vain päivämäärä    |          | X          |
| Sotilaspalveluksen alkamispäivämäärä        | Vain päivämäärä    |          | X          |
| Äidin syntymämaa tai -alue     | Asetusjoukko   |          | X          |
| Kansalaisuus, maa tai alue      | Asetusjoukko   |          | X          |
| Äidinkieli                    | Haku       |          | X          |
| Huollettavien määrä               | Koko numero |          |            |
| Sotaveteraanitila                     | Haku       |          | X          |
| Työntekijä                             | Haku       | X        | X          |
| Työntekijän henkilönumero      | Text         | X        | X          |


**Työntekijän pankkitili**

| **Kentät**                 | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|----------------------------|---------------|--------------|----------------|
| Tilin omistaja             | Text          |              | X              |
| Tilitunnus     | Text          |              | X              |
| Osoitteen kuvaus        | Text          |              | X              |
| Pankkitilin tyyppi          | Asetusjoukko    |              | X              |
| Pankin sijaintikoodi         | Text          |              | X              |
| Haaran nimi                | Text          |              | X              |
| Sivuliikkeen numero              | Text          |              | X              |
| Paikkakunta                       | Text          |              | X              |
| Maa tai alue          | Text          |              | X              |
| Piirikunta                     | Text          |              | X              |
| Kuvaus                | Text          |              | X              |
| Alueen nimi              | Text          |              | X              |
| Sähköposti                      | Text          |              | X              |
| Alanumero                  | Text          |              | X              |
| Faksi                        | Text          |              | X              |
| IBAN-tilinumero                       | Text          |              | X              |
| Rivi 1                     | Text          |              | X              |
| Rivi 2                     | Text          |              | X              |
| Rivi 3                     | Text          |              | X              |
| Matkapuhelin               | Text          |              | X              |
| Henkilön nimi             | Text          |              | X              |
| Postinumero                | Text          |              | X              |
| Postilokero            | Text          |              |                |
| Reititysnumero             | Text          |              | X              |
| Pankkikoodityyppi        | Asetusjoukko    |              | X              |
| Osavaltio tai provinssi          | Text          |              | X              |
| SWIFT-koodi                 | Text          |              | X              |
| Puhelin                  | Text          |              | X              |
| Teleksinumero               | Text          |              | X              |
| Internet-sivuston URL                | Text          |              | X              |
| Työntekijä                     | Haku        | X            | X              |
| Työntekijän tilinumero | Text          |              | X              |
| Työntekijän tilinumero | Text          | X            | X              |

**Työntekijän kiinteä kompensaatio**

| Kentät                                | Tietotyyppi      | Tarvitaan | Etsittävissä |
|---------------------------------------|----------------|----------|------------|
| Yritys                                | Haku         | X        | X          |
| Kompensaation tyyppi                     | Asetusjoukko     |          | X          |
| Valuutta                              | Haku         |          | X          |
| Voimassaolon alkamispäivämäärä                        | Vain päivämäärä      |          | X          |
| Tapahtuma                                 | Haku         | X        | X          |
| Vaihtokurssi                         | Desimaalinumero |          | X          |
| Vanhentumispäivä                       | Vain päivämäärä      |          | X          |
| Rivin numero                           | Desimaalinumero |          | X          |
| Maksutiheys                         | Haku         | X        | X          |
| Palkkio                              | Valuutta       |          | X          |
| Palkan määrä (perus)                       | Valuutta       |          | X          |
| Suunnitelma                                  | Haku         | X        | X          |
| Sijainti                              | Haku         | X        | X          |
| Prosessityyppi                          | Asetusjoukko     | X        | X          |
| Viitepisteen asetusrivit            | Haku         |          | X          |
| Työntekijä                                | Haku         | X        | X          |
| Työntekijän kiinteä kompensaationumero      | Text           | X        | X          |

**Työntekijän tunnusnumero**

| Kentät                 | Tietotyyppi   | Tarvitaan | Etsittävissä |
|------------------------|-------------|----------|------------|
| Kuvaus            | Text        |          | X          |
| Merkinnän tyyppi             | Text        |          | X          |
| Vanhentumispäivä        | Vain päivämäärä   |          | X          |
| Tunnusnumero  | Text        | X        | X          |
| Tunnuksen tyyppi    | Haku      | X        | X          |
| On ensisijainen             | Kaksi vaihtoehtoa |          | X          |
| Myöntämispäivämäärä             | Vain päivämäärä   |          | X          |
| Myöntäjätaho         | Haku      | X        | X          |
| Työntekijä                 | Haku      | X        | X          |


## <a name="position-entities"></a>Toimen yksiköt

**Tehtävänimike**

| **Kentät**               | **Tietotyyppi**  | **Vaadittu** | **Etsittävissä** |
|--------------------------|----------------|--------------|----------------|
| Aktivointi               | Päivämäärä ja aika  |              | X              |
| Käytettävissä toimeksiantoa varten | Päivämäärä ja aika  |              | X              |
| Osasto               | Haku         |              | X              |
| Kuvaus              | Text           |              | X              |
| Laskennallinen kokopäiväinen henkilömäärä     | Desimaalinumero |              | X              |
| Tehtävä                      | Haku         | X            | X              |
| Työpaikan numero      | Text           | X            | X              |
| Päätyön sijainti      | Haku         |              | X              |
| Toimityyppi            | Haku         |              | X              |
| Eläkkeelle siirtyminen               | Päivämäärä ja aika  |              | X              |
| Titteli                    | Asetusjoukko     |              | X              |
| Voimassaolo alkaa               | Päivämäärä ja aika  | X            | X              |
| Voimassaolo päättyy                 | Päivämäärä ja aika  |              | X              |


**Toimityyppi**

| **Kentät**         | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|--------------------|---------------|--------------|----------------|
| Luokittelu     | Asetusjoukko    |              | X              |
| Kuvaus        | Text          |              | X              |
| Toimityypin nimi | Text          | X            | X              |


**Toimen työntekijän toimeksianto**

| **Kentät**                        | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|-----------------------------------|---------------|--------------|----------------|
| Tehtävänimike                      | Haku        | X            | X              |
| Toimen työntekijän toimeksiannon numero | Text          | X            | X              |
| Voimassaolo alkaa                        | Text          | X            | X              |
| Voimassaolo päättyy                          |               |              | X              |
| Työntekijä                            |               | X            | X              |

## <a name="job-entities"></a>Työyksikköjä

**Työ**

| **Kentät**                   | **Tietotyyppi**  | **Vaadittu** | **Etsittävissä** |
|------------------------------|----------------|--------------|----------------|
| Salli rajoittamaton määrä toimia    | Kaksi vaihtoehtoa    |              | X              |
| Oletusarvoisesti kokopäiväinen (FTE) | Desimaalinumero |              | X              |
| Kuvaus                  | Text           |              | X              |
| Työnkuvaus              | Text           |              | X              |
| Työtehtävä                 | Haku         |              | X              |
| Työtyyppi                     | Haku         |              | X              |
| Toimien enimmäismäärä  | Koko numero   |              | X              |
| Nimi                         | Text           | X            | X              |
| Titteli                        | Asetusjoukko     |              | X              |
| Voimassaolo alkaa                   | Päivämäärä ja aika  | X            | X              |
| Voimassaolo päättyy                     | Päivämäärä ja aika  |              | X              |


**Työtehtävä**

| **Kentät**        | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|-------------------|---------------|--------------|----------------|
| Kuvaus       | Text          | X            | X              |
| Työtehtävän nimi | Text          | X            | X              |


**Työlaji**

| **Kentät**    | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|---------------|---------------|--------------|----------------|
| Kuvaus   | Text          | X            | X              |
| Vapautustila | Asetusjoukko    | X            | X              |
| Työtyypin nimi | Text          | X            | X              |

## <a name="leave-and-absence-entities"></a>Loman ja poissaolon kohteet

**Lomailmoittautuminen**

| **Kentät**            | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|-----------------------|---------------|--------------|----------------|
| Jaksotuspäiväperuste    | Vain päivämäärä     | X            | X              |
| Todellinen aloituspäivä    | Vain päivämäärä     | X            | X              |
| Tullauspäivämäärä           | Vain päivämäärä     | X            | X              |
| On keskeytetty jaksotus  | Kaksi vaihtoehtoa   |              | X              |
| LeaveEnrollmentNumber | Text          | X            | X              |
| Lomasuunnitelma            | Haku        | X            | X              |
| Aloituspäivä            | Vain päivämäärä     | X            | X              |
| Tasoperuste            | Asetusjoukko    | X            | X              |
| Työntekijä                | Haku        | X            | X              |


**Loman pankkitapahtuma**

| **Kentät**                    | **Tietotyyppi**  | **Vaadittu** | **Etsittävissä** |
|-------------------------------|----------------|--------------|----------------|
| Määrä                        | Desimaalinumero | X            | X              |
| Yritys                        | Haku         | X            | X              |
| Jätä pankkitapahtuman numero | Text           | X            | X              |
| Lomasuunnitelma                    | Haku         |              | X              |
| Lomatyyppi                    | Haku         | X            | X              |
| Tapahtuman päivämäärä              | Vain päivämäärä      | X            | X              |
| Tapahtumanumero            | Desimaalinumero | X            | X              |
| Tapahtumatyyppi              | Asetusjoukko     | X            | X              |
| Työntekijä                        | Haku         | X            | X              |


**Lomasuunnitelma**

| **Kentät**        | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|-------------------|---------------|--------------|----------------|
| Jaksotusväli | Asetusjoukko    | X            | X              |
| Yritys            | Haku        | X            | X              |
| Kuvaus       | Text          |              | X              |
| Lomatyyppi        | Haku        | X            | X              |
| Nimi              | Text          | X            | X              |
| Aloituspäivä        | Vain päivämäärä     | X            | X              |


**Lomapyyntö**

| **Kentät**           | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|----------------------|---------------|--------------|----------------|
| Kommentti              | Text          | X            | X              |
| Yritys               | Haku        | X            | X              |
| Lomapyynnön numero | Text          |              | X              |
| Pyynnön päivämäärä         | Päivämäärä ja aika | X            | X              |
| Tila               | Asetusjoukko    | X            | X              |
| Työntekijä               | Haku        | X            | X              |


**Lomapyynnön tiedot**

| **Kentät**                  | **Tietotyyppi**  | **Vaadittu** | **Etsittävissä** |
|-----------------------------|----------------|--------------|----------------|
| Määrä                      | Desimaalinumero | X            | X              |
| Loman päivämäärä                  | Päivämäärä ja aika  | X            | X              |
| Lomapyyntö               | Haku         | X            | X              |
| Lomapyynnön tiedot -numero | Text           | X            | X              |
| Lomatyyppi                  | Haku         | X            | X              |


**Lomatyyppi**

| **Kentät**      | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|-----------------|---------------|--------------|----------------|
| Yritys          | Haku        | X            | X              |
| Kuvaus     | Text          |              | X              |
| Ansiokoodi    | Haku        |              | X              |
| Lomatyypin nimi | Text          | X            | X              |


**Työkalenteri**

| **Kentät**  | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|-------------|---------------|--------------|----------------|
| Yritys      | Haku        | X            | X              |
| Kuvaus | Text          |              | X              |
| Nimi        | Text          | X            | X              |


**Työkalenteripäivämäärä**

| **Kentät**               | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|--------------------------|---------------|--------------|----------------|
| Kalenteripäivämäärä            | Vain päivämäärä     | X            | X              |
| Yritys                   | Haku        |              | X              |
| Tila                   | Text          |              | X              |
| Työkalenteri            | Haku        | X            | X              |
| Työkalenteripäivämäärän numero | Text          | X            | X              |


**Työkalenterin lomapäivä**

| **Kentät**  | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|-------------|---------------|--------------|----------------|
| Nimi        | Text          |              | X              |
| Kuvaus | Text          | X            | X              |


**Työkalenterin lomapäivärivi**

| **Kentät**                        | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|-----------------------------------|---------------|--------------|----------------|
| Loman päivämäärä                      | Vain päivämäärä     | X            | X              |
| Nimi                              | Text          |              | X              |
| Työkalenterin lomapäivä             | Haku        | X            | X              |
| Työkalenterin lomapäivärivin numero | Text          | X            | X              |


**Työkalenterin aikaväli**

| **Kentät**                         | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|------------------------------------|---------------|--------------|----------------|
| Yritys                             | Haku        |              | X              |
| Päättymisaika                           | Koko numero  |              | X              |
| Aloitusaika                         | Koko numero  |              | X              |
| Työkalenteri                      | Haku        | X            | X              |
| Työkalenteripäivämäärä                  | Haku        | X            | X              |
| Työkalenterin aikavälin numero | Text          | X            | X              |

## <a name="organization-entities"></a>Organisaatioyksiköt

**Yritys**

| **Kentät**   | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|--------------|---------------|--------------|----------------|
| Yrityskoodi | Text          | X            | X              |
| Nimi         | Text          | X            | X              |


**Osasto**

| **Kentät**        | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|-------------------|---------------|--------------|----------------|
| Osaston numero | Text          | X            | X              |
| Kuvaus       | Text          |              | X              |
| Nimi              | Text          | X            | X              |
| Pääosasto | Haku        |              | X              |


**Valuutta**

| **Kentät**         | **Tietotyyppi**  | **Vaadittu** | **Etsittävissä** |
|--------------------|----------------|--------------|----------------|
| Valuuttakoodi      | Text           | X            | X              |
| Valuutan nimi      | Text           | X            | X              |
| Valuutan tarkkuus | Koko numero   | X            | X              |
| Valuuttasymboli    | Text           | X            | X              |
| Entiteetin kuva       | Kuva          |              |                |
| Vaihtokurssi      | Desimaalinumero | X            | X              |
| Organisaatio       | Haku         | X            | X              |
| Tila             | Asetusjoukko     |              | X              |

## <a name="payroll-entities"></a>Palkanlaskentayksiköt

**Maksujakso**

| **Kentät**  | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|-------------|---------------|--------------|----------------|
| Kuvaus | Text          | X            | X              |
| Tiheys   | Asetusjoukko    | X            | X              |
| Nimi        | Text          | X            | X              |


**Maksukausi**

| **Kentät**           | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|----------------------|---------------|--------------|----------------|
| Oletusmaksupäivä | Vain päivämäärä     |              | X              |
| Kuvaus          | Text          |              | X              |
| Maksujakso            | Katso          | X            | X              |
| Maksukauden numero    | Text          | X            | X              |
| Kauden päättymispäivä      | Vain päivämäärä     | X            | X              |
| Kauden aloituspäivä    | Vain päivämäärä     | X            | X              |
| Tila               | Asetusjoukko    |              | X              |


**Palkanlaskennan ansiokoodi**

| **Kentät**              | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|-------------------------|---------------|--------------|----------------|
| Kuvaus             | Text          | X            | X              |
| Sisällytä maksutyyppiin | Asetusjoukko    | X            | X              |
| On tuottava           | Kaksi vaihtoehtoa   | X            | X              |
| Nimi                    | Text          |              | X              |
| Määräyksikkö           | Asetusjoukko    |              | X              |
| Seuraa FMLA-tunteja        | Kaksi vaihtoehtoa   |              | X              |


**Verotusalue**

| **Kentät**        | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|-------------------|---------------|--------------|----------------|
| Paikkakunta              | Text          |              | X              |
| Maa tai alue | Text          |              | X              |
| Piirikunta            | Text          |              | X              |
| Nimi              | Text          | X            | X              |
| Osavaltio tai provinssi | Text          |              | X              |


**Edun laskennan toistuvuuden maksukausi**

| **Kentät**                                      | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|-------------------------------------------------|---------------|--------------|----------------|
| Edun laskentatiheys                   | Haku        | X            | X              |
| Edun laskennan toistuvuuden maksukausi | Text          | X            | X              |
| Maksukausi                                      | Haku        | X            | X              |


**Pankkitilisuoritukset**

| **Kentät**                       | **Tietotyyppi**  | **Vaadittu** | **Etsittävissä** |
|----------------------------------|----------------|--------------|----------------|
| Määrä                           | Valuutta       |              | X              |
| Summa (perus)                    | Valuutta       |              | X              |
| Pankkitili                     | Haku         | X            | X              |
| Pankkitilisuoritusten numero | Text           | X            | X              |
| Yritys                           | Haku         | X            | X              |
| Valuutta                         | Haku         |              | X              |
| Vaihtokurssi                    | Desimaalinumero |              | X              |
| On jäljellä oleva määrä                     | Kaksi vaihtoehtoa    |              | X              |
| Prioriteetti                         | Koko numero   |              | X              |

**Henkilötunnuksen myöntänyt virasto**

| **Kentät**           | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|----------------------|---------------|--------------|----------------|
| Osoitteen kuvaus  | Text          |              | X              |
| Osoiterivi 1       | Text          |              | X              |
| Osoiterivi 2       | Text          |              | X              |
| Osoiterivi 3       | Text          |              | X              |
| Paikkakunta                 | Text          |              | X              |
| Maa tai alue    | Asetusjoukko    |              | X              |
| Piirikunta               | Text          |              | X              |
| Kuvaus          | Text          |              | X              |
| Sähköposti                | Text          |              | X              |
| Alanumero            | Text          |              | X              |
| Faksi                  | Text          |              | X              |
| Myöntäjätahon nimi  | Text          | X            | X              |
| Matkapuhelin         | Text          |              | X              |
| Sivu                 | Text          |              | X              |
| Postinumero          | Text          |              | X              |
| Postilokero      | Text          |              | X              |
| Tekstiviesti                  | Text          |              | X              |
| Osavaltio tai provinssi    | Text          |              | X              |
| Puhelin            | Text          |              | X              |
| Teleksi                | Text          |              | X              |
| Internet-sivuston URL          | Text          |              | X              |

**Työntekijän tunnustyyppi**

| **Kentät**                        | **Tietotyyppi**  | **Vaadittu** | **Etsittävissä** |
|-----------------------------------|----------------|--------------|----------------|
| Sallitut arvot                    | Asetusjoukko     |              | X              |
| Maa tai alue                 | Text           |              | X              |
| Kuvaus                       | Text           |              | X              |
| Kiinteä pituus                      | Koko numero   |              | X              |
| Tunnusnumeron muoto      | Text           |              | X              |
| Laji                              | Asetusjoukko     |              | X              |
| Työntekijän tunnustyyppi | Text           | X            | X              |

## <a name="fixed-compensation-entities"></a>Kiinteät kompensaatioyksiköt

**Kiinteä kompensaatiosuunnitelma**

| **Kentät**                  | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|-----------------------------|---------------|--------------|----------------|
| Yritys                      | Haku        | X            | X              |
| Kompensaatioruudukko           | Haku        |              | X              |
| Valuutta                    | Haku        | X            | X              |
| Kuvaus                 | Text          | X            | X              |
| Voimassaolon alkamispäivämäärä              | Vain päivämäärä     | X            | X              |
| Vanhentumispäivä             | Vain päivämäärä     | X            | X              |
| Työhönottosääntö                   | Asetusjoukko    | X            | X              |
| Nimi                        | Text          | X            | X              |
| Alueen ulkopuolisuuden toleranssi      | Asetusjoukko    | X            | X              |
| Maksutiheys               | Haku        | X            | X              |
| Suositus sallitaan      | Kaksi vaihtoehtoa   | X            | X              |
| Viitepisterivin määritys  | Haku        |              | X              |
| Laji                        | Asetusjoukko    | X            | X              |

**Kompensaatioruudukko**

| **Kentät**                  | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|-----------------------------|---------------|--------------|----------------|
| Yritys                      | Haku        | X            | X              |
| Valuutta                    | Haku        |              | X              |
| Kuvaus                 | Text          | X            | X              |
| Voimassaolon alkamispäivämäärä              | Vain päivämäärä     |              | X              |
| Vanhentumispäivä             | Vain päivämäärä     |              | X              |
| Nimi                        | Text          | X            | X              |
| Viitepisteen määritys       | Haku        | X            | X              |
| Laji                        | Asetusjoukko    | X            | X              |

**Kompensaatiotaso**

| **Kentät**      | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|-----------------|---------------|--------------|----------------|
| Kuvaus     | Text          |              | X              |
| Nimi            | Text          | X            | X              |
| Laji            | Asetusjoukko     | X            | X              |

**Kompensaation maksutiheys**

| **Kentät**                  | **Tietotyyppi**   | **Vaadittu** | **Etsittävissä** |
|-----------------------------|-----------------|--------------|----------------|
| Vuosittainen muuntokerroin    | Desimaalinumero  |              | X              |
| Yritys                      | Haku          | X            | X              |
| Kuvaus                 | Text            |              | X              |
| Tunnittainen muuntokerroin    | Desimaalinumero  |              | X              |
| Kuukausittainen muuntokerroin   | Desimaalinumero  |              | X              |
| Nimi                        | Text            | X            | X              |
| Kausi                      | Asetusjoukko      |              | X              |
| Viikoittainen muuntokerroin    | Asetusjoukko      |              | X              |


**Kompensaation viitepisteiden asetukset**

| **Kentät**          | **Tietotyyppi**   | **Vaadittu** | **Etsittävissä** |
|---------------------|-----------------|--------------|----------------|
| Yritys              | Haku          | X            | X              |
| Kompensaation tyyppi   | Asetusjoukko      | X            | X              |
| Kuvaus         | Text            | X            | X              |
| Nimi                | Text            | X            | X              |

**Kompensaation viitepisteen asetusrivi**

| **Kentät**            | **Tietotyyppi**   | **Vaadittu** | **Etsittävissä** |
|-----------------------|-----------------|--------------|----------------|
| Yritys                | Haku          | X            | X              |
| Kuvaus           | Text            | X            | X              |
| Rivin numero           | Desimaalinumero  | X            | X              |
| Nimi                  | Text            | X            | X              |
| Viitepisteen määritys | Haku          | X            | X              |

**Kompensaatioalue**

| **Kentät**      | **Tietotyyppi** | **Vaadittu** | **Etsittävissä** |
|-----------------|---------------|--------------|----------------|
| Kuvaus     | Text          | X            | X              |
| Nimi            | Text          | X            | X              |

**Kompensaatiorakenne**

| **Kentät**                    | **Tietotyyppi**   | **Vaadittu** | **Etsittävissä** |
|-------------------------------|---------------  |--------------|----------------|
| Määrä                        | Valuutta        |              | X              |
| Summan peruste                   | Valuutta        |              | X              |
| Yritys                        | Haku          | X            | X              |
| Kompensaatiorakenteen numero | Text            | X            | X              |
| Valuutta                      | Haku          |              | X              |
| Vaihtokurssi                 | Desimaalinumero  |              | X              |
| Ruudukko                          | Haku          | X            | X              |
| Tasaa                         | Haku          | X            | X              |
| Viitepiste               | Haku          | X            | X              |
| Viitepisterivin määritys    | Haku          | X            | X              |

**Kiinteä kompensaatiotapahtuma**

| **Kentät**            | **Tietotyyppi**   | **Vaadittu** | **Etsittävissä** |
|-----------------------|-----------------|--------------|----------------|
| Yritys                | Haku          | X            | X              |
| Kuvaus           | Text            | X            | X              |
| Tapahtumatyyppi            | Asetusjoukko      | X            | X              |
| On aktiivinen             | Kaksi vaihtoehtoa     | X            |                |
| Nimi                  | Text            | X            | X              |

## <a name="entity-relationship-models"></a>Yksikkösuhteen mallit

### <a name="worker"></a>Työntekijä
![Työntekijä](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Työ ja työn sijainti
![Työ ja työn sijainti](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Edut
![Edut](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Kompensaatio
![Kompensaatio](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Poistu
![Poistu](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Työkalenteri
![Työkalenteri](./media/HCMCommon-work-calendar-entity-diagram.png)
