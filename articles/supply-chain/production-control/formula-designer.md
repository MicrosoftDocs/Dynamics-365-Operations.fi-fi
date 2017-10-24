---
title: Reseptien suunnittelu
description: "Tässä ohjeaiheessa käsitellään kaavojen analysointia ja ylläpitoa puunäkymässä kaavan suunnittelutyökalulla."
author: cvocph
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: cvocph
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 159aa0fd5d057ed4105a79f11b3658133f417319
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="formula-designer"></a>Reseptien suunnittelu

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään kaavojen analysointia ja ylläpitoa puunäkymässä kaavan suunnittelutyökalulla.

Kun avaat **Reseptien suunnittelu** -sivun **Vapautetut tuotteet** -sivulta, vasemmassa ruudussa on luettelo oheistuotteista ja vapautetun tuotteen ainesosista. Rakenne johdetaan niiden kaavojen hierarkiasta, jotka ovat aktiivisia ja jotka on hyväksytty valitulle nimikkeelle ja sen ainesosille, nimikkeen oletustilaussivustoja ja todellisesta päivämäärästä.

Valitsemalla **Asetukset** voit valita erilaisia kokoonpanoja ja määrittää, mitkä tiedot puurakenteen riveillä näkyvät.

Valitse **Suodata** muuttaaksesi näkymän alkuperäistä valintaa. Jos valitset näyttötavaksi **Valittu/aktiivinen** tai **Valittu**, voit valita yksittäisen kaavan tai reitin version käytettäväksi näkymässä. Voit valita hyväksymättömiä ja ei-aktiivisia kaavan versioita näytettäväksi tai ylläpidettäväksi kaavojen suunnittelutoimintoon.  

> [!NOTE]
> Jos avaat **Kaavojen suunnittelutoiminto** -sivun **Tuoterakenne**-luettelosivulta, siinä ei näytetä reititystietoja. Tällä hetkellä valittu kaava tai reititysversio koskee kaikkia kaavan suunnittelutoiminnon esiintymiä.  

Seuraavissa osissa käsitellään rakennesuunnitteluikkunassa olevia toimintoja.

## <a name="analyze-a-formula-structure-by-using-the-formula-designer"></a>Kaavan rakenteen analysointi kaavojen suunnittelutoiminnon avulla
Kaavojen suunnittelutoiminnossa on kaksi osaa:

-   Kaavarakenteen puunäkymä.
-   Lisätieto-osa, jossa näytetään valitun datan lisätiedot. Kun valitset solmun puunäkymässä, lisätieto-osan pikavälilehtien tiedot päivitetään solmun perusteella:
    -   **Kaavarivin tiedot** – näyttää puunäkymässä valitun kaavanrivin tiedot.
    -   **Nimikkeen tiedot** – Näyttää päänimikkeen tai valitussa solmussa käytettävän nimikkeen tiedot. Voit napsauttaa **Muokkaa julkaistua tuotetta** -painiketta ylläpitääksesi valittua nimikettä.
    -   **Kaava** – näyttää valittuun solmuun liittyvän kaavan otsikon.
    -   **Reititys** – näyttää valittuun solmuun liittyvän reitityksen otsikon.
    -   **Reitityksen työvaiheet** – näyttää esikatseluikkunan reitityksen työvaiheista. Kun tiettyyn työvaiheeseen liitetty tuoterakenteen rivi valitaan, työvaiheeseen lisätään merkintä **Komponentti tarvitaan työvaiheessa**.

## <a name="select-a-formula-and-route"></a>Kaavan ja reititykseen valinta
Kaavojen suunnittelutoiminnon otsikossa näytetään suodatin, jota käytetään kaavalle ja reititykselle. Voit vaihtaa suodatinta **Suodatin** -valintaikkunassa. Seuraavassa taulukossa kuvaillaan tämän valintaikkunan kentät.

<table>
<thead>
<tr class="header">
<th>Kenttä</th>
<th>Kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tuotedimensiot</td>
<td>Jos valittu lopputuote on päätuote, voit määrittää aktiivisen tuotteen mitat päävalintaan. Huomaa, että jos avaat muun kuin päätuotteen kaavan suunnittelutoiminnon, tuotedimensioita ei voi valita <strong>Suodatut</strong>-valintaruudussa.</p></td>
</tr>
<tr class="even">
<td>Sivusto</td>
<td>Vaihda sivusto, jonka ainesosapuu näytetään. Oletustoimipaikka on lopputuotteen oletusvarastointipaikka.</td>
</tr>
<tr class="odd">
<td>Näyttötapa</td>
<td><p>Valitse sellainen version näyttötapa, joka koskee nykyistä kaavaa ja nykyistä reititystä.</p>
<ul>
<li>Kun tavaksi valitaan <strong>Aktiivinen</strong> tai <strong>Valittu/Aktiivinen</strong>, saadaan kuluvan päivän kaava tai reititysversio.</li>
<li>Kun tavaksi valitaan <strong>Valittu/aktiivinen</strong> tai <strong>Valittu</strong>, voit valita kaava- tai reititysversion valitsemalla <strong>Kaava</strong> &gt; <strong>Kaavaversio</strong> tai <strong>Reititys</strong> &gt; <strong>Reititysversiot</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Version päivämäärä</td>
<td>Annan kaavan ja reitityksen version päivämäärä. Version ilmaisee, mitä kaavaversiota tiettynä päivänä käytetään. Tämä määräytyy kaavaversion asetusten version päivämäärien mukaan.</td>
</tr>
<tr class="odd">
<td>Määrästä</td>
<td>Voit suodattaa versioita valitsemalla tietyn alkumäärän. Jos määrität arvon, voit valita vaihtoehtoisia kaava- ja reititysversioita.</td>
</tr>
<tr class="even">
<td>Näytä vain voimassa olevat</td>
<td>Kun valitset tämän valintaruudun, puurakenteessa näytetään vain ne kaavarivit, joilla on voimassaolopäivämäärä. Avaa <strong>Muokkaa kaavarakenneriviä</strong> -sivun napsauttamalla hiiren kakkospainikkeella tai kaksoisnapsauttamalla. Voit tarkistaa kyseisen kaavarivin voimassaolopäivämäärät tällä sivulla.</td>
</tr>
</tbody>
</table>

Kun tarkastelet tai muokkaat kaavojen suunnittelutoiminnolla kaavoja, jotka sisältävät haamunimikkeitä vähintään yhdellä tasolla, ylimpään nimikkeeseen liittyvä reitti kattaa yleensä kaavahierarkian kokonaisuudessaan. Yhteenvetoa voit helpottaa lukitsemalla ylätason reitityksen näyttöön napsauttamalla **Näytä** &gt; **Lukitse reititys**. Reitityksen lukituksen voit poistaa napsauttamalla **Näytä** &gt; **Poista reitityksen lukitus**.

## <a name="add-and-edit-formulas-and-formula-lines"></a>Kaavojen ja kaavarivien lisääminen ja muokkaaminen
Muokkaa kaavariviä tai kaavoja **Tuoterakennerivit**- tai **Kaava**-toiminnoilla. Kun valitset puurakenteessa solmun, solmun tyyppi määrittelee saatavilla olevat toiminnot.

| Toiminto                            | kuvaus                                                                                               | Solmutyyppi ja ehdot |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|--------------------------|
| Tuoterakennerivit &gt; Muokkaa                 | Voit muokata avautuvassa valintaikkunassa kaavarivin määritteitä.                                         | Tämä toiminto on käytettävissä silloin, kun kaavarivin solmu on valittuna. |
| Tuoterakennerivit &gt; Poista               | Poista kaavarivi valitusta kaavasta.                                                          | Tämä toiminto on käytettävissä silloin, kun kaavarivin solmu on valittu eikä kaavaa ole lukittu muokkauksen estämiseksi. |
| Tuoterakennerivit &gt; Lisää ennen riviä      | Avaa valintaikkuna, jossa voit valita kaavariviä edeltäväksi sisällytettävät tuotevariantit.     | Tämä toiminto on käytettävissä silloin, kun kaavarivin solmu on valittuna. |
| Tuoterakennerivit &gt; Lisää komponentin tuoterakenteeseen | Avaa valintaikkuna, jossa voit valita kaavan loppuun sisällytettävän tuotevariantin.   | Tämä toiminto on käytettävissä silloin, kun valitulla solmulla on valittu kaava. Jos toiminto ei ole käytettävissä, jokin kaavaversio voi puuttua valitusta nimikevariantista. Voit luoda siinä tapauksessa valitun solmun puuttuvan version valitsemalla **Kaava** &gt; **Luo versio**. |
| Tuoterakennerivit &gt; Lisää rivin jälkeen       | Avaa valintaikkuna, jossa voit valita kaavarivin jälkeen sisällytettävät tuotevariantit.      | Tämä toiminto on käytettävissä silloin, kun kaavarivin solmu on valittuna. |
| Kaava &gt; Luo versio         | Luo uusi valitun solmun tuotevariantin kaavaversio tai kaava.                     | Tämä toiminto on käytettävissä, kun valittu kaavarivin solmu linkitetään nimikkeeseen, jonka tuotantotyyppi on **Tuoterakenne** tai **Kaava**. |
| Kaava &gt; Laskenta            | Näyttöön tulee valintaikkuna, jossa voidaan suorittaa kustannuksen tai myyntihinnan laskenta valitulle tuotevariantille. | Tämä toiminto on käytettävissä silloin, kun valittu solmu liittyy kaavan versioon. |
| Kaava &gt; Tarkistus                  | Vahvista ja tarkista valittu kaava.                                                                  | Tämä toiminto on käytettävissä silloin, kun valittu solmu liittyy kaavan versioon. |

## <a name="configuring-the-tree-view"></a>Puunäkymän määrittäminen
Mukauta kaavan suunnittelutoiminnon puunäkymässä näkyviä tietoja valitsemalla **Asetukset**.

| Kenttäryhmä | kuvaus |
|-------------|-------------|
| Tuoterakenne         | Käytä valintaruutuja valitaksesi puurakenteessa näytettävät ehdot. Valitut ehdot näkyvät kaavan suunnittelutoiminnossa kummankin välilehden alaosassa. |
| Reititys       | Käytä valintaruutuja valitaksesi reitityksessä näytettävät ehdot. |

