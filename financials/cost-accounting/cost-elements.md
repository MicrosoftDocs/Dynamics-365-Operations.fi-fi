---
title: Kustannustason dimensiot
description: "Koska kustannustasodimensio on yksi kustannuslaskennan perustekijöistä, sitä käytetään luokittelemaan ja jäljittämään kustannusvirran suuntaa."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c06f4f636a58ac8068415b1291bd8668e7a977d5
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017

---

# <a name="cost-element-dimensions"></a>Kustannustason dimensiot

[!include[banner](../includes/banner.md)]


Koska kustannustasodimensio on yksi kustannuslaskennan perustekijöistä, sitä käytetään luokittelemaan ja jäljittämään kustannusvirran suuntaa. 

Kustannustaso vastaa kustannusten kannalta merkittävää nimikettä tilikartassa. Periaatteessa se voi olla minkä tahansa tyyppinen liiketoiminnan alatason elementti, johon kustannusvirta suuntautuu. Kustannustaso käsitteenä vaihtelee kirjanpitotilistä kaikkiin kustannusten kannalta merkittäviin resursseihin. Tällä hetkellä kustannuslaskenta tukee kirjanpitotilejä.

## <a name="two-types-of-cost-elements"></a>Kaksi kustannustasotyyppiä
Kustannustasoja on kahdenlaisia: ensisijaiset ja toissijaiset kustannustasot. Seuraavassa taulukossa esitetään kahden kustannustasotyypin erot:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Ensisijaiset kustannustasot</strong></td>
<td><strong>Toissijaiset kustannustasot</strong></td>
</tr>
<tr class="even">
<td>Ensisijaiset kustannustasot edustavat kustannusvirtaa kirjanpidosta kustannuslaskentaan. Kustannustasorakenne vastaa kirjanpidon tuloksen tilirakennetta, jossa kustannustaso voi vastata päätiliä. Liiketoiminnan tarpeiden mukaisesti kaikkia päätilejä ei välttämättä voida merkitä kustannustasoiksi. Esimerkkejä ensisijaisista kustannustasoista:
<ul>
<li>Myytyjen tuotteiden kustannukset (COG)</li>
<li>Epäsuorat materiaalikustannukset</li>
<li>Henkilökunnan kustannukset</li>
<li>Energiakustannukset</li>
</ul></td>
<td>Toissijaiset kustannustasot edustavat sisäistä kustannusvirtaa, koska nämä kustannukset luodaan ja niitä käytetään ainoastaan kustannuslaskennassa. Niitä käytetään varmistamaan, että kustannuslähde voidaan jäljittää. Näitä kustannustasoja käytetään kustannusten kohdistuksiin ja yleiskustannuslaskelmiin. Esimerkkejä toissijaisista kustannustasoista:
<ul>
<li>Tuotantokustannukset</li>
<li>Tuotannon, materiaalien ja markkinoinnin yleiskustannukset</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a>Kustannustason dimensiot ja kustannustason dimension jäsenet
Kustannustasoja kutsutaan *kustannustasodimensioiksi* . Yksittäisiä dimensioarvoja kutsutaan *kustannusluokkien dimensiojäseniksi*. Esimerkki: US tilikartan rakennetta (COA) käytetään lakisääteinen raportoinnin perustana. Tätä tilikarttaa käytetään kustannustason dimensiona. Tilit, jotka ovat ensisijaisia kustannustasoja, esitetään kustannustason dimensiojäseninä kustannuslaskennassa. Seuraavassa kuvankaappauksessa on esimerkki päätileistä kustannustasodimensioina ja toteutuneista päätileistä kustannustasodimension jäseninä. 

[![cost-element-dimensions](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)

## <a name="import-cost-element-dimension-members-through-data-connectors"></a>Kustannustason dimension jäsenten tuominen tietoyhdistimillä
Voit helpottaa kustannustason dimension jäsenten asetusta kustannuslaskennassa käyttämällä valmiita tai mukautettuja tietoyhdistimiä, joilla haetaan ensisijaiset kustannustasot yhdestä tai useammasta lähdejärjestelmästä.

## <a name="implementation-considerations"></a>Toteutuksessa huomioitavaa
Koska kustannustasot vastaavat alimman tason kustannustietoja, varmista, että kaikki kustannustasot, joita tarvitaan johdon raportointiin, sisältyvät käyttämääsi kustannustasorakenteeseen. Riittävän kustannustasomäärän saaminen kustannusseurantaa varten voi olla haastavaa. Jos kustannustasoja on tuhansia, yksittäisen kustannustason tarkastaminen voi olla vaikeaa. Vaihtoehtoisesti voit ryhmitellä kustannustasot ja hallita kustannusseurantaa yhdistetyllä tasolla.




