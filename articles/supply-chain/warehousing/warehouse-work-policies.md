---
title: Varaston työkäytännöt – yleiskatsaus
description: Varaston työkäytännöt määrittävät, onko varastotyö luotu varastoprosessia varten valmistuksessa työtilaustyypin, varaston sijainnin ja tuotteen perusteella.
author: johanhoffmann
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 7476cf797685feb4c50e3cefef4c53ca37b82dff
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251405"
---
# <a name="warehouse-work-policies-overview"></a>Varaston työkäytännöt – yleiskatsaus

[!include [banner](../includes/banner.md)]

Varaston työkäytännöt määrittävät, onko varastotyö luotu varastoprosessia varten valmistuksessa työtilaustyypin, varaston sijainnin ja tuotteen perusteella.

Tämä työkäytäntö määrittää, onko varastotyö luotu varastoprosessia varten valmistuksessa. Voit määrittää työkäytännön käyttämällä yhdistelmää **työtilaustyypit**, **varastosijainti** ja **tuote**. Esimerkiksi tuote L0101 ilmoitetaan valmiiksi tuotossijaintiin 001. Valmis tuote käytetään myöhemmin toisessa tuotantotilauksessa tuotossijainnissa 001. Tässä tapauksessa voit määrittää työkäytännön, joka estää luomasta työtä, jossa käytetään valmiita sivuun siirrettyjä tuotteita, kun raportoit tuotteen L0101 valmiiksi tuotossijaintiin 001. Työkäytäntö on yksittäinen yksikkö, jota voidaan kuvata seuraavien tietojen avulla:

-   **Työkäytännön nimi**(työkäytännön yksilöivä tunnus)
-   **Työtilaustyypit** ja **Työn luontimenetelmä**
-   **Varastosijainnit**
-   **Tuotteet**

## <a name="work-order-types"></a>Työtilaustyypit
Voit valita seuraavista työtilaustyypeistä:

-   Valmiiden tuotteiden poispano
-   Rinnakkaistuotteen ja sivutuotteen poispano
-   Raaka-aineiden keräily

**Työn luontimenetelmä** -kentän arvo on **Ei koskaan**. Tämä arvo ilmaisee, että työkäytäntö estää työn varastotyön luomisen valitulle työtilaustyypille.

## <a name="inventory-locations"></a>Varastosijainnit
Voit valita sijainnin, johon työkäytäntö sopii. Jos sijaintia ei ole liitetty työkäytäntöön, työkäytäntö ei koske mitään prosessia. **Sijainnit**-sivulla voidaan valita tai peruuttaa työkäytännön valinta määrätyssä sijainnissa.

## <a name="products"></a>Tuotteet
Voit valita tuotteen, johon työkäytäntö sopii. Voi soveltaa työkäytäntöä joko kaikkiin tai valittuihin tuotteisiin.

## <a name="example"></a>Esimerkki
Seuraavassa esimerkissä on kaksi tuotantotilausta RD-001 ja PRD-00*2*. Tuotantotilaus PRD-001 sisältää **Kokoonpano**-työvaiheen, jolla tuote SC1 raportoidaan valmiiksi sijainnissa O1. Tuotantotilaus PRD-002 sisältää **maalaus**-työvaiheen ja käyttää tuotetta SC1 sijainnista O1. Tuotantotilaus PRD-002 käyttää myös raaka-ainetta RM1 sijainnissa O1. RM1 varastoidaan varastosijaintiin BULK-001, josta raaka-ainekeräilyn varastotyö kerää sen sijaintiin O1. Keräilytyö luodaan, kun tuotanto PRD 002 vapautetaan. 

[![Varaston työkäytännöt](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png) 

Kun suunnittelet tämän skenaarion mukaista varastotyön konfigurointia, ota huomioon seuraava:

-   Valmiiden tuotteiden poispanon varastotyötä ei tarvita, kun raportoit tuotteen SC1 valmiiksi tuotantotilauksesta PRD 001 sijainnissa O1. Tämä johtuu siitä, että **Maalaus**-työvaihe tuotantotilauksessa PRD-002 käyttää SC1:n samassa sijainnissa.
-   Raaka-aineen keräilyn varastotyö vaaditaan, jotta raaka-aine RM1 siirretään varastosijainnista BULK-001 sijaintiin O1.

Seuraavassa on esimerkki työmenettelystä jonka voit määrittää näiden havaintojen perusteella.


|                                       |                                       |
|---------------------------------------|---------------------------------------|
| <strong>Työkäytännön nimi</strong><br> | <strong>Työtilaustyypit</strong><br> |
|         Ei pantu pois 01     `          |     - Valmiiden tuotteiden poispano<br>      |
|                                       |    <strong>Sijaintipaikat</strong><br>     |
|                                       |                 - O1                  |
|                                       |    <strong>Tuotteet</strong> <br>     |
|                                       |                 - SC1                 |

Seuraavissa menettelyissä saadaan vaiheittaiset ohjeet varastotyökäytännön määrittämiseksi tässä skenaariossa. Esimerkkiasetuksissa kuvataan myös, miten tuotantotilaus raportoidaan valmiiksi tiettyyn sijaintiin, jossa ei ole varastorekisterinumero-ohjausta.

## <a name="set-up-a-warehouse-work-policy"></a>Määritä varaston työkäytäntö
Varastointiprosessit eivät aina sisällä varastotyötä. Voit määrittää työn käytännön, joka estää raaka-aineen keräilytyön ja valmiiden tuotteiden poispanotöiden luonnin tietyille tuotejoukoille tietyissä sijainneissa. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. 

STEPS (21)

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| 1.  | Valitse Varastonhallinta &gt; Asetukset &gt; Työ &gt; Työkäytännöt.        |
| 2.  | Valitse Uusi.                                                                 |
| 3.  | Kirjoita Työkäytännön nimi -kenttään Ei poispanotyötä.                    |
| 4.  | Valitse Tallenna.                                                                |
| 5.  | ValitseLisää.                                                                 |
| 6.  | Merkitse valittu rivi luettelossa.                                        |
| 7.  | Valitse Työtilauksen tyyppi -kentässä Valmiiden tuotteiden poispano.            |
| 8.  | ValitseLisää.                                                                 |
| 9.  | Merkitse valittu rivi luettelossa.                                        |
| 10. | Valitse Työtilauksen tyyppi -kenttään Rinnakkaistuotteen ja sivutuotteen poispano. |
| 11. | Laajenna Varastosijainnit-osa.                                    |
| 12. | ValitseLisää.                                                                 |
| 13. | Merkitse valittu rivi luettelossa.                                        |
| 14. | Kirjoita varasto-luetteloon arvo 51.                                         |
| 15. | Syötä tai valitse Sijainti-kentän arvoksi 001.                              |
| 16. | Laajenna Tuotteet-osa.                                               |
| 17. | Valitse Tuotteen valinta -kentän arvoksi Valittu.                         |
| 18. | ValitseLisää.                                                                 |
| 19. | Merkitse valittu rivi luettelossa.                                        |
| 20. | Syötä tai valitse Nimiketunnus-kentän arvoksi L0101.                         |
| 21. | Valitse Tallenna.                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a>Raportoi tuotantotilaus valmistuneeksi sijaintiin, jossa ei ole varastorekisterinumero-ohjausta
Tässä menettelyssä näytetään esimerkki valmiiksi ilmoittamisesta sijaintiin, jota ei ohjata rekisterikilvellä. Tehtävä edellyttää käytettävää työkäytäntöä. Työkäytännön määrittäminen on esitelty edellisessä menettelyssä. 

STEPS (25)

<table>
<tbody>
<tr>
<td colspan="3"><strong>Alitehtävä: Määritä tulostussijainti.</strong></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td>Valitse Organisaation hallinto &gt; Resurssit &gt; Resurssiryhmät.</td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td>Valitse luettelosta resurssiryhmä 5102.</td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td>Valitse Muokkaa.</td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td>Kirjoita Tulostusvarasto-kenttään arvo 51.</td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td>Kirjoita Tulostussijainti-kenttään arvo 001.</td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td>Sijainti 001 ei ole rekisterikilven mukaan ohjattu sijainti. Voit määrittää rekisterikilven mukaan ohjaamattoman sijainnin ainoastaan, jos sijainnille on olemassa soveltuva työkäytäntö.</td>
</tr>
<tr>
<td colspan="3"><strong>Alitehtävä: Luo tuotantotilaus ja ilmoita se valmiiksi.</strong></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td>Sulje sivu.</td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td>Siirry kohtaan Tuotannonhallinta &gt; Tuotantotilaukset &gt; Kaikki tuotantotilaukset.</td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td>Valitse Uusi tuotantotilaus.</td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td>Kirjoita Nimiketunnus-kenttään arvo L0101.</td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td>Valitse Luo.</td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td>Valitse toimintoruudussa Tuotantotilaus.</td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td>Valitse Arvio.</td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td>Valitse OK.</td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td>Valitse Käynnistys.</td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td>Valitse Yleiset-välilehti.</td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td>Valitse Automaattinen tuoterakennekulutus -kentässä Ei koskaan.</td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td>Valitse OK.</td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td>Valitse Ilmoita automaattisesti valmiiksi.</td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td>Valitse Yleiset-välilehti.</td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td>Valitse Hyväksy virhe -kentässä Kyllä.</td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td>Valitse OK.</td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td>Valitse toimintoruudussa Varasto.</td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td>Valitse Työn tiedot.</td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td>Kun tuotantotilaus on raportoitu päättyneeksi, poispanotöitä ei luotu. Tämä johtuu siitä, että määritettynä on työn käytäntö, joka estää töiden luonnin, kun tuote L0101 ilmoitetaan valmiiksi sijaintiin 001.</td>
</tr>
</tbody>
</table>



