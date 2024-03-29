---
title: Lausekerajoitukset ja taulurajoitukset tuotemääritysmalleissa
description: Tässä artikkelissa kuvataan lauseke- ja taulurajoitusten käyttö. Rajoittaa sellaisten määritearvojen hallitsemista, joita käytät tuotteiden määrittämiseen myyntitilaukselle, myyntitarjoukselle, ostotilaukselle tai tuotantotilaukselle. Voit käyttää lausekerajoituksia tai taulurajoituksia, riippuen siitä, kuinka haluat luoda rajoitukset.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e504f6996b401e72792d910c8df74bb9611c4d60
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895551"
---
# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a>Lausekerajoitukset ja taulurajoitukset tuotemääritysmalleissa

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan lauseke- ja taulurajoitusten käyttö. Rajoittaa sellaisten määritearvojen hallitsemista, joita käytät tuotteiden määrittämiseen myyntitilaukselle, myyntitarjoukselle, ostotilaukselle tai tuotantotilaukselle. Voit käyttää lausekerajoituksia tai taulurajoituksia, riippuen siitä, kuinka haluat luoda rajoitukset. 

Rajoituksilla hallitaan valittavissa olevia määritearvoja, kun tuotteita määritetään myyntitilaukseen, myyntitarjoukseen, ostotilaukseen tai tuotantotilaukseen. Voit käyttää lausekerajoituksia tai taulurajoituksia, riippuen siitä, kuinka haluat luoda rajoitukset.

## <a name="what-are-expression-constraints"></a>Mitä ovat lausekkeen rajoitukset?
Lausekerajoituksissa on lauseke, joka käyttää aritmeettisia tai Boolen operaattoreita ja funktioita. Lausekerajoitus kirjoitetaan tuotemääritysmallin tietylle komponentille. Sitä ei voi käyttää uudelleen tai jakaa toisen komponentin kanssa. Komponentin lausekerajoitukset voivat kuitenkin viitata komponentin alikomponenttien määritteisiin.

## <a name="what-are-table-constraints"></a>Mitä ovat taulukon rajoitukset?
Taulurajoitukset kuvaavat sellaisia arvoyhdistelmiä, jotka sallitaan määritteille, kun määrität tuotetta. Taulurajoituksen määrityksiä voidaan käyttää yleisesti. Luodessasi taulurajoituksen komponentille tuotteen konfiguraatiomallissa, valitset taulukon rajoitusmäärityksen. Jos haluat luoda sallittuja yhdistelmiä, lisää tietyn tyyppisiä määritteitä komponentteihin. Jokaisella määritteen tyypillä on tietty arvo.

### <a name="example-of-a-table-constraint"></a>Esimerkki taulurajoituksesta

Tämä esimerkki osoittaa, miten voit rajoittaa kaiuttimen kokoonpanon tiettyihin viimeistelyihin ja etulevyihin. Ensimmäisessä taulukossa ovat ne kaappien viimeistelyt ja etulevyt, jotka kokoonpanolle on yleisesti saatavilla. Arvot on määritetty **Kaapin viimeistely**- ja **Etusäleikkö**-määritetyypeille.

| Määritteen tyyppi | Arvot                      |
|----------------|-----------------------------|
| Kaapin viimeistely | Musta, tammi, ruusupuu, valkoinen |
| Etusäleikkö    | Musta, metalli, valkoinen         |

Seuraavassa taulukossa näkyvät **Väri ja viimeistely** -taulurajoituksen määrittämät yhdistelmät. Tämän taulurajoituksen avulla voit määrittää kaiuttimen, jonka viimeistelynä on tammi ja jonka etusäleikkö on musta, jonka viimeistelynä on ruusupuu ja etusäleikkö valkoinen ja niin edelleen.

| Lopetus         | Säleikkö                       |
|----------------|-----------------------------|
| Tammi            | Musta                       |
| Ruusupuu       | Valkoinen                       |
| Valkoinen          | Musta                       |
| Valkoinen          | Valkoinen                       |
| Musta          | Musta                       |
| Musta          | Metalli                       | 

Voit luoda järjestelmän määrittämiä ja käyttäjän määrittämiä taulukkorajoitteita. Lisätietoja on kohdassa [Järjestelmän ja käyttäjän määrittämät taulurajoitukset](system-defined-user-defined-table-constraints.md).

## <a name="what-syntax-should-be-used-to-write-constraints"></a>Mitä syntaksia pitäisi käyttää rajoitusten kirjoittamiseen?
Käytä rajoituksia kirjoittaessasi Optimization Modeling Language (OML) -syntaksia. Järjestelmä käyttää Microsoft Solver Foundation -rajoitusratkaisinta rajoitusten selvittämiseen.

## <a name="should-i-use-table-constraints-or-expression-constraints"></a>Tulisiko minun käyttää taulurajoituksia vai lausekerajoituksia?
Voit käyttää joko lausekerajoituksia tai taulurajoituksia sen mukaan, miten haluat luoda rajoitukset. Taulurajoitus kootaan matriisiksi, kun taas lausekerajoitus on yksittäinen lauseke. Määrittäessäsi tuotteen se ei ole merkitystä millaista rajoitetta käytetään. Seuraava esimerkki osoittaa näiden menetelmien erot.  

Nämä yhdistelmät ovat sallittuja, kun määrität tuotteen käyttämällä seuraavia rajoitusasetuksia:

-   Tuote, väri Musta, koko 30 tai 50
-   Tuote, väri Punainen, koko 20

### <a name="table-constraint-setup"></a>Taulurajoituksen asetukset

| Väri | Koko |
|-------|------|
| Musta | 30   |
| Musta | 50   |
| Punainen   | 20   |

### <a name="expression-constraint-setup"></a>Lausekerajoituksen asetukset

(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a>Tulisiko minun käyttää operaattoreita vai infix-merkintää, kun kirjoitan lausekerajoituksia?
Voit kirjoittaa lausekerajoituksen käyttämällä joko käytettävissä olevia etuliiteoperaattoreita tai infix-merkintää. **Min**-, **Max**- ja **Abs**-operaattorien kanssa ei voi käyttää infix-merkintää. Nämä operaattorit sisältyvät vakiona useimpiin ohjelmointikieliin.

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a>Mitä operaattoreita ja infix-merkintöjä voin käyttää kirjoittaessani lausekerajoituksia?
Seuraavissa taulukoissa on kuvattu operaattorit ja infix-merkinnät, joita voidaan käyttää, kun tuotemääritysmallin komponentille kirjoitetaan lausekerajoitus. Ensimmäisen taulukon esimerkit osoittavat, miten lauseke kirjoitetaan käyttämällä joko infix-merkintää tai operaattoreita.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Käyttäjä</th>
<th>Kuvaus</th>
<th>Syntaksi</th>
<th>Esimerkkejä</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Sisältää</td>
<td>Jos ehto a on tosi, käytä sitten rajoitusta b.</td>
<td>Tarkoittaa [a, b] infix:-: b</td>
<td><ul>
<li><strong>Operaattori:</strong> Implies[x! = 0, y &gt; = 0]</li>
<li><strong>Infix-merkintä:</strong> x != 0 -: y &gt;= 0</li>
</ul></td>
</tr>
<tr class="even">
<td>Ja</td>
<td>Tämä on tosi vain, jos kaikki ehdot ovat tosia. Jos ehtojen määrä on 0 (nolla), tuloksena on <strong>Tosi</strong>.</td>
<td>And[args], infix: a &amp; b &amp; ... &amp; z</td>
<td><ul>
<li><strong>Operaattori</strong>: And[x == 2, y &lt;= 2]</li>
<li><strong>Infix-merkintä:</strong> x == 2 &amp; y &lt;= 2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Tai</td>
<td>Näin tapahtuu, jos mikä tahansa ehto on tosi. Jos ehtojen määrä on 0 (nolla), tuloksena on <strong>Epätosi</strong>.</td>
<td>Or[args], infix: a | b | ... | z</td>
<td><ul>
<li><strong>Operaattori:</strong> Or[x == 2, y &lt;= 2]</li>
<li><strong>Infix-merkintä:</strong> x == 2 | y &lt;= 2</li>
</ul></td>
</tr>
<tr class="even">
<td>Plus</td>
<td>Tämä koostaa sen ehdot. Jos ehtojen määrä on 0 (nolla), tuloksena on <strong>0</strong>.</td>
<td>Plus[args], infix: a + b + ... + z</td>
<td><ul>
<li><strong>Operaattori:</strong> Plus[x, y, 2] == z</li>
<li><strong>Infix-merkintä:</strong> x + y + 2 == z</li>
</ul></td>
</tr>
<tr class="odd">
<td>Miinus</td>
<td>Tämä kääntää sen argumentin. Ehtoja on oltava täsmälleen yksi.</td>
<td>Miinus [lauseke], operandien välinen merkintä: -expr</td>
<td><ul>
<li><strong>Operaattori:</strong> Minus[x] == y</li>
<li><strong>Infix-merkintä:</strong> -x == y</li>
</ul></td>
</tr>
<tr class="even">
<td>Itseisarvo</td>
<td>Tämä vaatii ehtoonsa itseisarvon. Ehtoja on oltava täsmälleen yksi.</td>
<td>Itseisarvo[lauseke]</td>
<td><strong>Operaattori:</strong> Abs[x]</td>
</tr>
<tr class="odd">
<td>Ajat</td>
<td>Tämä vaatii tuotteen ehtoonsa. Jos ehtojen määrä on 0 (nolla), tuloksena on <strong>1</strong>.</td>
<td>Times[args], infix: a * b * ... * z</td>
<td><ul>
<li><strong>Operaattori:</strong> Times[x, y, 2] == z</li>
<li><strong>Infix-merkintä:</strong> x * y * 2 == z</li>
</ul></td>
</tr>
<tr class="even">
<td>Teho</td>
<td>Tämä vaatii eksponentiaalin. Tämä koskee potenssiinkorotusta oikealta vasemmalle. (Tämä tarkoittaa, että se on oikea-assosiatiivinen.) Siksi <strong>Power[a, b, c]</strong> on sama kuin <strong>[a, Power[b, c]]</strong>. <strong>Power</strong>-operaattoria voidaan käyttää vain, jos eksponentti on positiivinen vakio.</td>
<td>Power[args], infix: a ^ b ^ ... ^ z</td>
<td><ul>
<li><strong>Operaattori:</strong> Power[x, 2] == y</li>
<li><strong>Infix-merkintä:</strong> x ^ 2 == y</li>
</ul></td>
</tr>
<tr class="odd">
<td>Enintään</td>
<td>Tämä tuottaa suurimman ehdon. Jos ehtojen määrä on 0 (nolla), tuloksena on <strong>Ääretön</strong>.</td>
<td>Maksimi [argumentit]</td>
<td><strong>Operaattori:</strong> Max[x, y, 2] == z</td>
</tr>
<tr class="even">
<td>Vähintään</td>
<td>Tämä tuottaa pienimmän ehdon. Jos ehtojen määrä on 0 (nolla), tuloksena on <strong>Ääretön</strong>.</td>
<td>Minimi [argumentit]</td>
<td><strong>Operaattori:</strong> Min[x, y, 2] == z</td>
</tr>
<tr class="odd">
<td>Ei</td>
<td>Tämä tuottaa loogisen käänteisen version ehdostansa. Ehtoja on oltava täsmälleen yksi.</td>
<td>Not[expr], infix: !expr</td>
<td><ul>
<li><strong>Operaattori:</strong> Not[x] &amp; Not[y == 3]</li>
<li><strong>Infix-merkintä:</strong> !x!(y == 3)</li>
</ul></td>
</tr>
</tbody>
</table>

Seuraavan taulukon esimerkit kuvaavat, kuinka infix-merkintä kirjoitetaan.


|  Operandien välinen merkintä   |                                          kuvaus                                          |
|-------------------|-----------------------------------------------------------------------------------------------|
|     x + y + z     |                                           Lisäys                                            |
|    x \* y \* z    |                                        Kertolasku                                         |
|       x - y       | Binäärimuotoinen vähennys tehdään samalla tavalla kuin binäärimuotoinen lisäys käänteisen toisen kanssa. |
|     x ^ y ^ z     |                          Potenssiinkorotus, jolla on oikea-assosiatiivisuus                          |
|        !x         |                                          Totuusarvo ei                                          |
|      x -: y       |                                      Looginen vaikutus                                      |
|         x         |                                               y                                               |
|     x & y & z     |                                          Totuusarvo ja                                          |
|    x == y == z    |                                           Yhtäsuuruus                                            |
|    x != y != z    |                                           Erilliset                                            |
|  x &lt; y &lt; z  |                                           Pienempi kuin                                           |
|  x &gt; y &gt; z  |                                         Suurempi kuin                                          |
| x &lt;= y &lt;= z |                                     Pienempi tai yhtä suuri                                     |
| x &gt;= y &gt;= z |                                   Suurempi tai yhtä suuri                                    |
|        (x)        |                           Sulkeet ohittavat oletusarvoisen tärkeysjärjestyksen.                            |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a>Miksi lausekerajoitusteni vahvistaminen ei onnistu?
Et voi käyttää varattuja avainsanoja ratkaisimen niminä määritteille, komponenteille tai alikomponenteille tuotemääritysmallissa. Seuraavassa luettelossa on varatut sanat, jotka eivät ole käytettävissä:

-   Katto
-   Elementti
-   Yhtäläinen
-   Kerros
-   Jos
-   Pienempi
-   Suurempi
-   Sisältää
-   Loki
-   Enintään
-   Min
-   Miinus
-   Plus
-   Teho
-   Ajat
-   Aika
-   Malli
-   Päätöksenteko
-   Tavoite


## <a name="additional-resources"></a>Lisäresurssit

[Luo lausekerajoitus](tasks/add-expression-constraint-product-configuration-model.md)

[Lisää laskelma tuotemääritysmalliin](tasks/add-calculation-product-configuration-model.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
