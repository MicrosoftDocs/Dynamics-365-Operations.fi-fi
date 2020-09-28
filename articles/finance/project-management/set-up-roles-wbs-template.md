---
title: Työrakennemallien roolien määrittäminen
description: Tässä aiheessa on tietoja työrakennemallien roolin tietojen määrittämisestä.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5dfb429eae933ba4d687ec4cbd417d2f78308e47
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760536"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Työrakennemallien roolien määrittäminen

[!include [banner](../includes/banner.md)]

Projektipäälliköt voivat määrittää työrakennemalleja ja käyttää niitä luodessaan uusille projekteille työrakennetta. Projektipäälliköt voivat lisätä rooleja malleja luodessaan. Voit määrittää roolin työrakennemalliin seuraavasti. 

1. Valitse **Projektinhallinta ja kirjanpito** > **Asetukset** > **Projektit** > **Työrakennemallit**.
2. Valitse valitun työrakennemallin **Tiedot**-kohta.
3. Valitse luettelosta haluamasi tehtävä ja valitse sitten **Rooli**-kentästä tehtävään määritettävä rooli.

## <a name="work-with-a-wbs"></a>Työrakenteen käsitteleminen

Voit luoda uuden työrakenteen tai kopioida sen aiemmin luodusta työrakennemallista. Projektipäällikkö voi hallita resursseja helposti määrittämällä työrakenteessa roolit uusille tehtäville. Roolit voidaan korvata, kun resurssi on hankittu tai kun vahvistettu resurssi tehtävään on määritetty. Näin projektipäälliköt voivat suorittaa joustavasti seuraavat tehtävät:

- Määrittää työrakenteen työpaketteihin tarvittavan resurssien määrän.
- Arvioida projektikustannukset.
- Määritellä alustavan budjetin.
- Arvioida tehtävän kestoa roolien ja resurssien perusteella.
- Kehittää joitakin projektinhallintasuunnitelmia käytettävissä olevien projektitietojen pohjalta.

Työrakenteeseen on liitetty lisäasetuksia, jotka helpottavat resursointitoimintojen käyttöä.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Vaihtoehto</th>
<th>Kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Resurssimääritykset</td>
<td>Tarkastele määritettyjä resursseja, päivämääriä, tuntimääriä ja tehtävien varaustyyppiä työrakenteessa.</td>
</tr>
<tr class="even">
<td>Luo ryhmä automaattisesti</td>
<td>Lisää suunnitellut resurssit automaattisesti käyttämällä tehtävään liitettyjä rooleja. Finance ehdottaa suunniteltuja resursseja automaattisesti käyttämällä rooleihin perustuvaa useiden ehtojen analyysia. Kun tehtäville on määritetty roolit ja työaika (tunnit) työrakenteessa ja rakenne on julkaistu, valitse <strong>Luo ryhmä automaattisesti</strong>. Tarvittava suunniteltujen resurssien määrä lisätään työrakenteeseen ja <strong>Projektiryhmä ja ajoitus</strong> -välilehteen.</td>
</tr>
<tr class="odd">
<td>Resurssi (avattava luettelo)</td>
<td><strong>Käynnistä resurssimääritys</strong> -sivulla voit valita resurssit kiinteää tai alustavaa varausta varten määritetyn keston perusteella. Voit muokata näyttöasetuksia niin, että saat näkyviin ja voit määrittää resurssitehtävien keston. Voit valita ja määrittää resursseja työpakettitasolla käyttämällä seuraavia vaihtoehtoja:
<ul>
<li><strong>Hyväksy</strong> – vahvistaa tehtävään liitettyyn resurssiin tehdyt muutokset.</li>
<li><strong>Peruuta</strong> – peruuttaa tehtävään liitettyyn resurssiin tehdyt muutokset.</li>
<li><strong>Määritä automaattisesti</strong> – Valitulle tehtävälle valitaan automaattisesti käytettävissä oleva henkilöstöllisen resurssi ja sitä vastaava rooli.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Valitse **Kaikki projektit** -sivulla **XYZ-päivitysvaihe 2** -projekti.
2. Valitse **Suunnitelma** > **Tehtävät** > **Työrakenne**.
3. Valitse **Uusi** ja lisää seuraavat ykköstason tehtävät työrakenteeseen:

    - Aloittaminen
    - Suunnittelu
    - Suoritetaan
    - Valvonta ja ohjaus
    - Sulje

4. Määritä päivämäärät ja työmäärä (tunteina) kuvassa esitetyllä tavalla.

    [![Päivämäärien ja työmäärän määrittäminen](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Valitse **Aloittaminen**-tehtävärivi ja valitse sitten **Rooli**-kentästä **Vastaava projektipäällikkö**.
6. Valitse **Julkaise**.
7. Valitse samalta riviltä **Resurssi**-kentästä **Daniel Goldschmidt** ja valitse sitten **Hyväksy**.
8. Valitsemalla **Suunnittelu**-tehtävärivi ja valitse sitten **Rooli**-kentästä **Yritysanalyytikko**.
9. Valitse **Julkaise** ja sitten **Luo ryhmä automaattisesti**.
10. Valitse näyttöön tulevassa viesti-ikkunassa **Kyllä**.
11. Tarkista, että **Resurssi**-kentässä arvona on **Yritysanalyytikko 1**.
12. Avaa hakutoiminto **Yritysanalyytikko 1** -resurssin kohdalla ja valitse **Käynnistä resurssimäärityksen lomake**. Valitse tehtävään työntekijä.
13. Valitse **Määritä alustavasti** &gt; **Koko kapasiteetti**.

    > [!NOTE] 
    > Näyttöön ei tule varoitusta siitä, että määritetyn resurssin arvo on nyt 2, koska resurssien määrä on edelleen 1.

14. Tarkista **Työrakenne**-sivulta työrakenteen resurssimääritys ja valitse sitten **Tallenna**.
