---
title: Rakennesuunnittelun toiminnot
description: "Tässä artikkelissa kuvataan, miten tuoterakennesuunnittelijan sivua käytetään tuoterakenteiden puurakenteiden suunnittelussa ja käsittelyssä. Valitsemalla Asetukset voit valita erilaisia konfiguraatioita ja määrittää, mitkä tiedot puurakenteen riveillä näkyvät."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMDesigner
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 20981
ms.assetid: 2b92eec1-d28c-4965-9086-939c77b3c62b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: ff482c183276a99a3c9a632d41d9121bf77befbf
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="bom-designer-functionality"></a>Rakennesuunnittelun toiminnot

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kuvataan, miten tuoterakennesuunnittelijan sivua käytetään tuoterakenteiden puurakenteiden suunnittelussa ja käsittelyssä. Valitsemalla Asetukset voit valita erilaisia konfiguraatioita ja määrittää, mitkä tiedot puurakenteen riveillä näkyvät.

Kun avaat **Graafisen rakennesuunnittelun** sivun **Julkaistut tuotteet** -sivulta, näytetään siinä aktiivisten ja hyväksyttyjen tuoterakenteiden hierarkia hierarkian valitulle nimikkeelle, nimikkeen oletustilaussivusto ja todellinen päivämäärä.  

Valitse **Suodata** muuttaaksesi näkymän alkuperäistä valintaa. Määrittämällä näyttötavaksi **Valitut/Aktiiviset tai Valitut** voit valita yksittäisiä tuoterakenteen tai reitin versioita käytettäväksi näkymässä. Voit valita hyväksymättömiä ja ei-aktiivisia tuoterakenteen versioita näytettäväksi tai ylläpidettäväksi rakennesuunnitteluikkunaan.  

**Huomautus:** Jos avaat graafisen rakennesuunnitteluikkunan **Tuoterakenne**-luettelosivulta, siinä ei näytetä reititystietoja. Tällä hetkellä valitun tuoterakenteen tai reitityksen versio on tuoterakenteen ja reitityksen version ominaisuus, joka koskee kaikkia graafinen rakennesuunnitteluikkunan esiintymiä.  

Seuraavissa osissa kuvataan graafisen rakennesuunnitteluikkunan eri välilehdissä käytettävissä olevat toiminnot.

## <a name="analyzing-a-bom-structure-by-using-the-bom-designer"></a>Tuoterakenteen analysointi graafisessa rakennesuunnitteluikkunassa
Graafinen rakennesuunnitteluikkuna on jaettu kahteen osaan:

-   Tuoterakenteen puunäkymä.
-   Lisätieto-osa, jossa näytetään valitun datan lisätiedot. Kun valitset solmun puunäkymässä, lisätieto-osan pikavälilehtien tiedot päivitetään solmun perusteella:
    -   **Tuoterakennerivin tiedot** – Näyttää puunäkymässä valitun tuoterakenteen rivin tiedot.
    -   **Nimikkeen tiedot** – Näyttää päänimikkeen tai valitussa solmussa käytettävän nimikkeen tiedot. Voit napsauttaa **Muokkaa julkaistua tuotetta** -painiketta ylläpitääksesi valittua nimikettä.
    -   **Tuoterakenne** – Näyttää valittuun solmuun liittyvän tuoterakenteen otsikon.
    -   **Reititys** – Näyttää valittuun solmuun liittyvän reitityksen otsikon.
    -   **Reitityksen työvaiheet** – Näyttää esikatseluikkunan reitityksen työvaiheista. Kun tiettyyn työvaiheeseen liitetty tuoterakenteen rivi valitaan, työvaiheelle lisätään merkintä **Komponentti tarvitaan työvaiheessa**.

## <a name="selecting-a-bom-and-route"></a>Tuoterakenteen ja reitityksen valitseminen
Graafisen rakennesuunnitteluikkunan otsikossa näytetään suodatin, jota käytetään tuoterakenteelle ja reititykselle. Voit vaihtaa suodatinta **Suodatin** -valintaikkunassa. Seuraavassa taulukossa kuvaillaan tämän valintaikkunan kentät.

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
<td>Valitun lopputuotteen ollessa päätuote, voit määrittää ensisijaiselle valinnalle aktiiviset tuotedimensiot. <strong>Huomautus:</strong> Jos avaat graafisen rakennesuunnitteluikkunan tuotteelle, joka ei ole päätuote, <strong>Suodatin</strong>-valintaikkunassa ei voi valita tuotedimensioita.</td>
</tr>
<tr class="even">
<td>Sivusto</td>
<td>Vaihda näytettävän tuoterakenteen puun toimipaikka. Oletustoimipaikka on lopputuotteen oletusvarastointipaikka.</td>
</tr>
<tr class="odd">
<td>Näyttötapa</td>
<td>Valitse sellainen version näyttötapa, joka kohdistuu nykyiseen tuoterakenteeseen ja nykyiseen reititykseen:
<ul>
<li>Kun tavaksi määritetään <strong>Aktiivinen tai Valittu/Aktiivinen</strong>, tämän päivän aikana voimassa oleva tuoterakenne tai reititysversio löytyy.</li>
<li>Kun tavaksi määritetään <strong>Valittu/Aktiivinen tai Valittu</strong>, voit valita tuoterakenne- tai reititysversion napsauttamalla <strong>Tuoterakenne</strong> &gt; <strong>Tuoterakenteen versiot</strong> tai <strong>Reititys</strong> &gt; <strong>Reititysversiot</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Version päivämäärä</td>
<td>Kirjoita tuoterakenteen ja reitityksen version päivämäärä. Version avulla määritetään, mitä tuoterakenneversiota on käytettävä tiettynä päivänä, joka määräytyy tuoterakenneversion asetusten version päivämäärien mukaan.</td>
</tr>
<tr class="odd">
<td>Määrästä</td>
<td>Voit suodattaa versioita valitsemalla tietyn alkumäärän. Jos määrität arvon, voit valita vaihtoehtoisia tuoterakenne- ja reititysversioita.</td>
</tr>
<tr class="even">
<td>Näytä vain voimassa olevat</td>
<td>Kun valitset tämän valintaruudun, puurakenteessa näkyvät vain ne tuoterakennerivit, joilla on voimassaolopäivämäärä. Napsauta hiiren kakkospainikkeella tai kaksoisnapsauta tuoterakenneriviä avataksesi <strong>Muokkaa tuoterakenneriviä</strong> -sivun, jossa näkyy tuoterakenteen rivin voimassaolopäivämäärät.</td>
</tr>
</tbody>
</table>

Kun käytät graafista rakennesuunnitteluikkunaa tarkastellaksesi tai muokataksesi tuoterakenteita, jotka sisältävät haamunimikkeitä vähintään yhdellä tasolla, reitti, joka liittyy päänimikkeeseen kattaa yleensä tuotehierarkian kokonaisuudessaan. Yhteenvetoa voit helpottaa lukitsemalla ylätason reitityksen näyttöön napsauttamalla **Näytä** &gt; **Lukitse reititys**. Reitityksen lukituksen voit poistaa napsauttamalla **Näytä** &gt; **Poista reitityksen lukitus**.

## <a name="adding-and-editing-boms-and-bom-lines"></a>Tuoterakenteiden ja tuoterakennerivien lisääminen ja muokkaaminen
Käytä **Tuoterakennerivit**- tai **Tuoterakenne**-toimintoja muokataksesi tuoterakenteen rivejä tai itse rakennetta. Kun valitset solmun puurakenteesta, solmun tyyppi määrittelee saatavilla olevat toiminnot.

| Toiminto                            | kuvaus                                                                                               | Solmutyyppi ja ehdot                                                                                                                                                                                                                                                                       |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tuoterakennerivit &gt; Muokkaa                 | Näyttöön tulee valintaikkuna, jossa voit muokata tuoterakenteen rivin ominaisuuksia.                                             | Tämä toiminto on käytettävissä silloin, kun tuoterakennerivin solmu on valittuna.                                                                                                                                                                                                                                   |
| Tuoterakennerivit &gt; Poista               | Poista valittu tuoterakennerivi valitusta rakenteesta.                                                                  | Tämä toiminto on käytettävissä silloin, kun tuoterakennerivin solmu on valittuna ja tuoterakenne ei ole lukittuna muokkausta varten.                                                                                                                                                                                             |
| Tuoterakennerivit &gt; Lisää ennen riviä      | Avaa valintaikkunan, jossa voit valita tuoterakenneriviä edeltäväksi sisällytettävät tuotevariantit.         | Tämä toiminto on käytettävissä silloin, kun tuoterakennerivin solmu on valittuna.                                                                                                                                                                                                                                   |
| Tuoterakennerivit &gt; Lisää komponentin tuoterakenteeseen | Avaa valintaikkunan, jossa voit valita tuoterakenteen loppuun sisällytettävän tuotevariantin.       | Tämä toiminto on käytettävissä silloin, kun valitulla solmulla on valittu tuoterakenne. Jos toiminto ei ole käytettävissä, valitulta nimikevariantilta saattaa puuttua jokin tuoterakenteen versio. Tässä tapauksessa voit napsauttaa **Tuoterakenne** &gt; **Luo versio** luodaksesi puuttuvan version valitsemallesi solmulle. |
| Tuoterakennerivit &gt; Lisää rivin jälkeen       | Avaa valintaikkunan, jossa voit valita tuoterakennerivin jälkeiseksi sisällytettävät tuotevariantit.          | Tämä toiminto on käytettävissä silloin, kun tuoterakennerivin solmu on valittuna.                                                                                                                                                                                                                                   |
| Tuoterakenne &gt; Luo versio             | Luo uuden tuoterakenneversion tai tuoterakenteen valitun solmun tuotevariantille.                             | Tämä toiminto on käytettävissä, kun valittu tuoterakennerivin solmu linkitetään nimikkeeseen, jonka tuotantotyyppi on **Tuoterakenne** tai **Kaava**.                                                                                                                                                  |
| Tuoterakenne &gt; Laskenta                | Näyttöön tulee valintaikkuna, jossa voidaan suorittaa kustannuksen tai myyntihinnan laskenta valitulle tuotevariantille. | Tämä toiminto on käytettävissä silloin, kun valittu solmu liittyy johonkin tuoterakenteen versioon.                                                                                                                                                                                                         |
| Tuoterakenne &gt; Tarkista                      | Vahvista ja tarkista valittu tuoterakenne.                                                                      | Tämä toiminto on käytettävissä silloin, kun valittu solmu liittyy johonkin tuoterakenteen versioon.                                                                                                                                                                                                         |

## <a name="configuring-the-tree-view"></a>Puunäkymän määrittäminen
Napsauta **Asetukset** mukauttaaksesi graafisen rakennesuunnitteluikkunan puunäkymässä näytettäviä tietoja.

| Kenttäryhmä | Kuvaus                                                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tuoterakenne         | Käytä valintaruutuja valitaksesi puurakenteessa näytettävät ehdot. Valitut ehdot näkyvät suunnitteluikkunassa molempien välilehtien alaosassa. |
| Reitti       | Käytä valintaruutuja valitaksesi reitityksessä näytettävät ehdot.                                                                                    |






