---
title: Jaetun tilausten hallinnan (JTH) kustannusten määrittäminen
description: Tässä aiheessa kuvataan Dynamics 365 Commerce -sovelluksen jaetun tilausten hallinnan (JTH) toimintojen kustannusten määrittämistä.
author: josaw1
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: ba4e24052599d431de88d00236a4a99899ca413c136f4627e69c8937541dac03
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730980"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a>Jaetun tilausten hallinnan (JTH) kustannusten määrittäminen

[!include [banner](../includes/banner.md)]

Organisaatiot käyttävät useita kustannuskomponentteja tilauksen täyttämisen optimaalisen sijainnin määrittämisessä. Kustannuskomponentteja ovat esimerkiksi lähetys-, käsittely- ja pakkauskustannukset. Näiden kustannusten yhteenlaskettu kustannus määrittää tilauksen täyttämissijainnin.

Kun Dynamics 365 Commerce -sovelluksen jaetun tilausten hallinnan (JTH) ensimmäinen iteraatio optimoi tilausten määrityksen täyttämissijainteihin, se otetaan huomioon vain etäisyytenä. Vaikka etäisyys voi korreloida kustannuksen kanssa, se ei ole sama kuin kustannus. Esimerkiksi lähetystapa yön yli maksaa enemmän kuin kolmen tai seitsemän päivän lähetys samalla etäisyydellä.

Kustannusten määritystoiminnon avulla jälleenmyyjät voivat määrittää lisäkustannuskomponentteja, jotka lasketaan ja otetaan huomioon tilausrivien toteuttamisessa käytettävän optimaalisen sijainnin määrittämisessä.

Kun kustannuskomponentit määritetään, JTH:n selvitystoiminto käyttää vain näitä kustannusten määrityksiä tilauksen toteuttamisen optimaalisen sijainnin määrittämisessä. Se ei ota huomioon etäisyyskomponenttia kustannuksena. Jos kustannuskomponentteja ei kuitenkaan määritetä, JTH:n selvitystoiminto käyttää etäisyyskomponenttia kustannuksessa tilauksen toteuttamisen optimaalisen sijainnin määrittämisessä.

## <a name="set-up-cost-components"></a>Kustannuskomponenttien määrittäminen

Järjestelmässä voidaan määrittää kaksi pääkustannuskomponenttia: **lähetys** ja **muu**.

Molemmat kustannuskomponentin tyypit tukevat useita laskentaperusteita seuraavassa taulukossa esitetyllä tavalla.

<table>
<thead>
<tr>
<th>Kustannuskomponentin tyyppi</th>
<th>Laskuperuste</th>
</tr>
</thead>
<tbody>
<tr>
<td>Lähetys</td>
<td>
<ul>
<li>Yksinkertainen</li>
<li>Porrastettu</li>
</ul>
</td>
</tr>
<tr>
<td>Muu</td>
<td>
<ul>
<li>Myyntitilaus</li>
<li>Myyntirivi</li>
<li>Sijainti</li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a>Lähetyskustannuskomponentin tyyppi

Tässä osassa kerrotaan, miten kunkin **lähetys** kustannuskomponentin tyypin ja lähetyskustannusten laskentaperusteen yhdistelmä määritetään. Osassa kerrotaan myös, miten JTH:n selvitystoiminto käyttää kutakin yhdistelmää.

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a>Kustannuskomponentin tyyppi = lähetys ja laskentaperuste = yksinkertainen

Jos käytetään **lähetys** kustannuksen tyyppiä ja **yksinkertaista** laskentaperustetta, toimitustavan lähetyskustannukset perustuvat kiinteään kustannukseen tai etäisyyteen.

Tälle yhdistelmälle on määritettävä seuraavat kentät:

- **Kustannustekijä** – Anna kustannustekijän yksilöivä tunniste.
- **Kuvaus** – Anna kustannustekijän nimi ja kuvaus.
- **Alkamis**- ja **päättymispäivä** – Näiden kenttien avulla kustannustekijän voi rajata koskemaan tiettyä ajanjaksoa. Jos nämä kentät jätetään tyhjiksi, kustannustekijä on voimassa toistaiseksi.
- **Aktiivinen** – Osoittaa, onko kustannustekijä aktiivinen. JTH ottaa huomioon vain aktiiviset täyttämisprofiilin liitetyt kustannustekijät.
- **Yritys** – Määritä yritys, jolle kustannustekijä on määritetty. Kaikkien laskentakriteerien rivien on koskettava samaa yritystä.
- **Toimitustavat** – Määritä toimitustavat, joille kustannus on määritetty.
- **Laskentatyyppi** – Määritä, miten tietyn toimitustavan kustannus lasketaan. Tuettuja laskentatyyppejä on kaksi:

    - **Kiinteä** – Toimitustavassa käytetään kiinteää kustannusta. Jos valitset tämän laskentatyypin, **Kustannus**-kenttä määrittää kiinteän kustannuksen.
    - **Etäisyysyksikköä kohti** – Toimitustavan kustannus lasketaan kustannuksen arvona. Se määritetään kertomalla **Kustannus**-kentän arvo toimitusosoitteen ja sijaintien etäisyydellä.

- **Kustannus** – Määritä kustannusarvo, jota käytetään yhdessä **Laskentatyyppi**-kentän arvon kanssa, kun toimitustavan kustannus lasketaan.

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a>Kustannuskomponentin tyyppi = lähetys ja laskentaperuste = porrastettu

Jos käytetään **lähetys** kustannuksen tyyppiä ja **porrastettua** laskentaperustetta, toimitustavan lähetyskustannukset perustuvat kiinteään kustannukseen tai etäisyyteen. Tässä yhdistelmässä etäisyys perustuu kuitenkin etäisyyksien porrastettuun väliin.

Tälle yhdistelmälle on määritettävä seuraavat kentät:

- **Kustannustekijä** – Anna kustannustekijän yksilöivä tunniste.
- **Kuvaus** – Anna kustannustekijän nimi ja kuvaus.
- **Oletuskustannus** – Määritä kustannus, jota käytetään toimitustavassa silloin, kun toimitusosoitteen ja sijainnin etäisyys ei ole mikään toimitustavan porrastetuista etäisyyksistä.
- **Alkamis**- ja **päättymispäivä** – Näiden kenttien avulla kustannustekijän voi rajata koskemaan tiettyä ajanjaksoa. Jos nämä kentät jätetään tyhjiksi, kustannustekijä on voimassa toistaiseksi.
- **Aktiivinen** – Osoittaa, onko kustannustekijä aktiivinen. JTH ottaa huomioon vain aktiiviset täyttämisprofiilin liitetyt kustannustekijät.
- **Yritys** – Määritä yritys, jolle kustannustekijä on määritetty. Kaikkien laskentakriteerien rivien on koskettava samaa yritystä.
- **Toimitustavat** – Määritä toimitustavat, joille kustannus on määritetty.
- **Etäisyyden tyyppi** – Määritä, onko porrastettu etäisyys määritetty linnuntietä vai teitä pitkin.
- **Etäisyyden yksiköt** – Määritä yksikkö, jossa porrastettu etäisyys mitataan.
- **Etäisyys kohteesta** – Määritä porrastetun etäisyyden aloitusalue.
- **Etäisyys kohteeseen** – Määritä porrastetun etäisyyden lopetusalue.
- **Laskentatyyppi** – Määritä, miten tietyn toimitustavan ja porrastetun etäisyyden kustannus lasketaan. Tuettuja laskentatyyppejä on kaksi:

    - **Kiinteä** – Toimitustavassa käytetään kiinteää kustannusta. Jos valitset tämän laskentatyypin, **Kustannus**-kenttä määrittää kiinteän kustannuksen.
    - **Etäisyysyksikköä kohti** – Toimitustavan ja porrastetun etäisyyden kustannus lasketaan kustannuksen arvona. Se määritetään kertomalla **Kustannus**-kentän arvo toimitusosoitteen ja sijaintien etäisyydellä.

- **Kustannus** – Määritä kustannusarvo, jota käytetään yhdessä **Laskentatyyppi**-kentän arvon kanssa, kun toimitustavan kustannus lasketaan.

> [!NOTE]
> - Kun määrität porrastetut etäisyydet, järjestelmä tarkistaa, että etäisyyksiä ei puutu ja että ne eivät ole päällekkäisiä.
> - Toimitustavassa käytettävän etäisyyden tyypin on oltava sama kaikissa porrastetuissa etäisyyksissä.

### <a name="other-cost-component-type"></a>Muu kustannuskomponentin tyyppi

Tässä osassa kerrotaan, miten kunkin **muun** kustannuskomponentin tyypin ja muun kuin lähetyskustannusten muun kustannustyypin laskentaperusteen yhdistelmä määritetään. Osassa kerrotaan myös, miten JTH:n selvitystoiminto käyttää kutakin yhdistelmää.

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a>Kustannuskomponentin tyyppi = muu ja muun kustannuksen tyyppi = myyntitilaus

**Muun** kustannuskomponentin tyypin ja **myyntitilauksen** muun kustannuksen tyypin yhdistelmää käytetään määritettäessä muita kuin lähetyskustannuksia myyntitilauksen tasolla.

Tälle yhdistelmälle on määritettävä seuraavat kentät:

- **Kustannustekijä** – Anna kustannustekijän yksilöivä tunniste.
- **Kuvaus** – Anna kustannustekijän nimi ja kuvaus.
- **Alkamis**- ja **päättymispäivä** – Näiden kenttien avulla kustannustekijän voi rajata koskemaan tiettyä ajanjaksoa. Jos nämä kentät jätetään tyhjiksi, kustannustekijä on voimassa toistaiseksi.
- **Aktiivinen** – Osoittaa, onko kustannustekijä aktiivinen. JTH ottaa huomioon vain aktiiviset täyttämisprofiilin liitetyt kustannustekijät.
- **Kustannus** – Määritä muiden kuin lähetyskustannusten kustannusarvo myyntitilauksen tasolla.

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a>Kustannuskomponentin tyyppi = muu ja muun kustannuksen tyyppi = myyntirivi

**Muun** kustannuskomponentin tyypin ja **myyntirivin** muun kustannuksen tyypin yhdistelmää käytetään määritettäessä muita kuin lähetyskustannuksia myyntitilausrivin tasolla.

Tälle yhdistelmälle on määritettävä seuraavat kentät:

- **Kustannustekijä** – Anna kustannustekijän yksilöivä tunniste.
- **Kuvaus** – Anna kustannustekijän nimi ja kuvaus.
- **Alkamis**- ja **päättymispäivä** – Näiden kenttien avulla kustannustekijän voi rajata koskemaan tiettyä ajanjaksoa. Jos nämä kentät jätetään tyhjiksi, kustannustekijä on voimassa toistaiseksi.
- **Aktiivinen** – Osoittaa, onko kustannustekijä aktiivinen. JTH ottaa huomioon vain aktiiviset täyttämisprofiilin liitetyt kustannustekijät.
- **Kustannus** – Määritä muiden kuin lähetyskustannusten kustannusarvo myyntitilausrivin tasolla.

#### <a name="cost-component-type--other-and-other-cost-type--location"></a>Kustannuskomponentin tyyppi = muu ja muun kustannuksen tyyppi = sijainti

**Muun** ja **sijainnin** muun kustannustyypin yhdistelmää käytetään sijaintiryhmien tai yksittäisen sijainnin muiden kuin lähetyskustannusten määrittämisessä.

Tälle yhdistelmälle on määritettävä seuraavat kentät:

- **Kustannustekijä** – Anna kustannustekijän yksilöivä tunniste.
- **Kuvaus** – Anna kustannustekijän nimi ja kuvaus.
- **Alkamis**- ja **päättymispäivä** – Näiden kenttien avulla kustannustekijän voi rajata koskemaan tiettyä ajanjaksoa. Jos nämä kentät jätetään tyhjiksi, kustannustekijä on voimassa toistaiseksi.
- **Aktiivinen** – Osoittaa, onko kustannustekijä aktiivinen. JTH ottaa huomioon vain aktiiviset täyttämisprofiilin liitetyt kustannustekijät.
- **Täyttämisryhmä** – Määritä niiden sijaintien ryhmä, joille muun kuin lähetyksen kustannus määritetään.
- **Täyttämissijainti** – Määritä se sijainti, jolle muun kuin lähetyksen kustannus määritetään.

    > [!NOTE]
    > Et voi määrittää täyttämisryhmää ja -sijaintia samalle sijaintiin perustuvalle laskentakriteerien riville.

- **Kustannus** – Määritä muun kuin lähetyskustannuksen kustannusarvo täyttämisryhmän tai täyttämissijainnin tasolla.

> [!IMPORTANT]
> Lisää kustannustekijä soveltuvaan täyttämisprofiiliin, jotta JTH voi käyttää näitä kustannuksia suorittamisen aikana.


[!INCLUDE[footer-include](../includes/footer-banner.md)]