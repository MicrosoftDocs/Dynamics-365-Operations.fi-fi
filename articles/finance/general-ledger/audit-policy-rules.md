---
title: Tilinarkastuskäytännön säännöt
description: Voit käyttää tarkistuskäytäntöjä kuluraporttien, toimittajan laskujen ja ostotilausten arvioimiseen, jotta voit varmistua luomiesi käytäntösääntöjen noudattamisesta. Kaikki tarkastuskäytäntöön liittyvät säännöt suoritetaan erätilassa määrittämäsi aikataulun mukaisesti.  Jokainen käytäntösääntö on käytäntösäännön tyypin esiintymä. Jokaisella käytäntösääntötyypillä voi olla kerrallaan aktiivisena vain yksi käytäntösääntö.
author: panolte
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: kfend
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8272cd516f1b31f20ded7c2fdb8bfc4c4d984d42
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710498"
---
# <a name="audit-policy-rules"></a>Tilinarkastuskäytännön säännöt

[!include [banner](../includes/banner.md)]

Voit käyttää tarkistuskäytäntöjä kuluraporttien, toimittajan laskujen ja ostotilausten arvioimiseen, jotta voit varmistua luomiesi käytäntösääntöjen noudattamisesta. Kaikki tarkastuskäytäntöön liittyvät säännöt suoritetaan erätilassa määrittämäsi aikataulun mukaisesti.  Jokainen käytäntösääntö on käytäntösäännön tyypin esiintymä. Jokaisella käytäntösääntötyypillä voi olla kerrallaan aktiivisena vain yksi käytäntösääntö. 

## <a name="queries-and-query-types"></a>Kyselyt ja Kyselytyypit

Kun luot tarkistuskäytännön sääntö, sinun on valittava käytäntösääntötyyppi. Käytäntösäännön tyyppi määrittää sovellusobjektipuu (AOT) -kyselyn, jota käytetään aloituskohtana käytäntösäännön luomisessa. Se määrittää myös käytäntösäännölle käytettävän kyselyn tyypin. Kysely määrittää lähdeasiakirjan, jolle käytäntösääntötyyppi tulkitaan. Se määrittää myös lähdeasiakirjan kentät, joiden avulla tunnistetaan sekä yritys että käytettävä päivämäärä, kun asiakirjoja valitaan auditointiin. Kyselytyyppi hallitsee kyselysivun ja tilintarkastuskäytäntö sääntöjen sivun oletuskenttiä. Seuraavassa taulukossa on kyselytyypit, joiden on oltava käytettävissä tarkistuksen käytäntösäännöille.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Kyselytyyppi</th>
<th>Tarkoitus</th>
<th>Lisätietoja</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ehdollinen</td>
<td>Arvioi lähdeasiakirjan määritteitä määritettyjen arvojen kanssa.</td>
<td></td>
</tr>
<tr class="even">
<td>Kooste</td>
<td>Arvioi useita lähdeasiakirjoja tai lähdeasiakirjarivejä käytäntösäännön kanssa yhdistämällä numeroarvoja.</td>
<td></td>
</tr>
<tr class="odd">
<td>Otanta</td>
<td>Valitse satunnaisesti tietty lähde-tiedostojen prosenttiosuus arvioidaksesi käytännön rikkomuksia.</td>
<td>Kun valitset tämän vaihtoehdon, käytä tilintarkastuksen käytäntösääntösivua määrittämään asiakirjojen prosenttiosuuden satunnaisesti valiten auditoinnin.</td>
</tr>
<tr class="even">
<td>Monista</td>
<td>Arvioi lähdeasiakirjat, jotta voit määrittää sisältävätkö ne kaksoismerkintöjä tietyissä kentissä.</td>
<td>Kun valitset tämän vaihtoehdon, käytä tilintarkastus käytäntösääntö sivua määrittämään päivien määrän, joka lisätään asiakirjan valitun päivämäärävälin alkuun asiakirjoja arvioitaessa kaksoiskappaleita varten.</td>
</tr>
<tr class="odd">
<td>Luettelohaku</td>
<td>Arvioi tiettyjen yksiköiden lähdeasiakirjat.</td>
<td>Kyselyn pääasiakirja määrittää auditoitavan asiakirjan. Kyselyn on oltava luettelokysely, joka sisältää viittauksen dirpartytable taulukkoon. Tätä asetusta voidaan käyttää vain seuraavissa AOT-kyselyissä:
<ul>
<li><span class="ui">Tilintarkastuskäytäntölista</span> (Kuluraporteissa valvonnassa olevat työntekijät)</li>
<li><span class="ui">TilintarkastuskäytäntöOstoLista</span> (Ostotilauksissa valvonnassa olevat toimittajat)</li>
<li><span class="ui">TilintarkastuskäytäntöToimittajaLaskuLista</span> (Toimittajalaskuissa seuratut toimittajat)</li>
</ul>
Kun valitset tämän vaihtoehdon, määritä valvotut kohteet Tilintarkastuskäytännön säännöt -sivulla.</td>
</tr>
<tr class="even">
<td>Avainsanahaku</td>
<td>Arvioi lähdeasiakirjat, jotta voit määrittää sisältävätkö ne tietyt sanat.</td>
<td>Kun valitset tämän vaihtoehdon, syötä sanat, joita etsitään Tilintarkastuskäytännön säännöt -sivulla. Tilintarkastussäännöt-sivu sisältää myös asetukset, joiden avulla voit määrittää taulut ja kentät kirjoittamiesi sanojen arvioimiseksi.</td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a>Yleiset parametrit
Kaikilla tietyn tarkastuskäytännön säännöillä on samat eräparametrit ja sama asiakirjan valinnan päivämääräväli. Nämä parametrit on määritetty käytännölle Lisävaihtoehdot-sivulla.



## <a name="additional-resources"></a>Lisäresurssit

[Tarkistuskäytäntörikkomukset ja -tapaukset](audit-policy-violations-cases.md)
[Tarkistuskäytäntöjen määrittäminen lähdeasiakirjoille](tasks/define-audit-policies-source-documents.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
