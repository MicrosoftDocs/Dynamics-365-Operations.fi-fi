---
title: Lean-organisaation mallinnus
description: "Artikkelissa on tietoja Lean-organisaation mallintamisen tärkeimmistä käsitteistä."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow, PlanActivity
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53141
ms.assetid: 4f272f2f-ec2c-4b0d-a652-00a63b719b9e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: c8e24234cfa54dcbbf3638c31ced7fb83881bb9f
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---

# <a name="modeling-a-lean-organization"></a>Lean-organisaation mallinnus

[!include [banner](../includes/banner.md)]

Artikkelissa on tietoja Lean-organisaation mallintamisen tärkeimmistä käsitteistä. 

Yleensä Lean-valmistusskenaario enemmän kuin yhteen kuulumattomien kanban-sääntöjen tai materiaalin ostokäytäntöjen kokoelma. Työsolujen ja sijaintien läpi kulkevaa, tiettyä tuotantoa tai toimitusskenaariota koskevaa materiaali- ja tuotevirtaa voidaan kuvata pienten, toisiaan seuraavien prosessi- tai siirtotöiden verkostoksi. Tätä järjestystä tai verkostoa sanotaan tuotantovirraksi.

## <a name="production-flows-in-lean-manufacturing"></a>Lean-valmistuksen tuotantovirrat
Tuotantotilauksiin perustuvissa tuotantoskenaarioissa materiaali määritetään tiettyä tuotantotilausta varten. Tuoterakenteeseen ja reititykseen perustuvien työvaiheiden järjestyksen aikana tuotteita luodaan ja lopulta vastaanotetaan annetussa sijaintipaikassa. Tuotantotilausten läpimenoaika vaihtelee minuuteista viikkoihin. Kaikki prosessiin liittyvät kustannukset, materiaalit ja työ kerätään tuotantotilaukselle. 

Jotta toimituksen läpimenoajat lyhenevät ja ylimääräinen, erätuotannosta johtuva varastointi kuormituspaikkojen välillä pienenee, Lean-valmistus käyttää kanban-täydennystä ja supermarketteja valmistuksen ja varastoinnin täydennyksessä. Tämä nämä toiminnot keskeyttävät osittain itsenäisten kanban-syklien tuotannon. Kanbanin täydennystä puolivalmiille tuotteelle ei enää käynnistä valmista tuotetta koskeva tilaus. 

Jotta tuotannon ja kulujen konteksti voidaan luoda uudelleen eri Microsoft Dynamics 365 for Finance and Operationsin ehdottamille kanban-skenaarioille, tehtäväpohjaiset tuotantovirrat on luotu Lean-valmistuksen rungoksi. Kaikki kanban-säännöt viittaavat tähän ennalta määritettyyn rakenteeseen. Tehtäväpohjainen malli tukee laajempaa skenaariovalikoimaa kuin Dynamics AX:n tukemat aiemmat Lean-valmistuksen versiot. Tämä malli ei kuitenkaan tee ohjelmaa monimutkaisemmaksi työntekijöille, koska kaikissa skenaarioissa käytetään samaa tehtäväpohjaista käyttöliittymää.

## <a name="semi-finished-products-non-bom-levels"></a>Puolivalmiit tuotteet (ei-tuoterakennetasot)
Microsoft Dynamics AX:n Lean-valmistus integroi kanbanit inventoidulle tuotteille ja puolivalmiille tuotteille yhteen kehykseen ja tarjoaa tämän vuoksi yhtenäisen käyttäjäkokemuksen kaikissa tapauksissa. Tämän arkkitehtuurin vuoksi puolivalmiissa tuotteissa käytettävien kanbaneiden käytössä tarvittavia lisätuoterakenteiden tasoja ei enää ole lisätty. Tämä arkkitehtuuri auttaa myös varastotapahtumien vähentämisessä pienimmälle mahdolliselle tasolle.

## <a name="products-and-material-in-work-in-progress"></a>Tuotteet ja materiaalit keskeneräisissä töissä
Eräkokojen pienentäminen ihanteelliseen yhden kappaleen virran tilaan Lean-valmistuksessa voi aiheuttaa dramaattisen varastotapahtumien kasvun, jos jokainen keräilyprosessi tai kanban-rekisteröinti aiheuttaa tapahtumia kulutetuille nimikkeille. Tuotantovirran arkkitehtuuri sallii materiaalien siirron tuotantovirtaan yhdessä varaston otto-kanbaneiden tai toimituksen käsittely-yksiköiden koon avulla. Määritettyjen materiaalien arvo lisätään tuotantovirtaan liittyvälle keskeneräisten töiden KET-tilille. Tämä toiminta muistuttaa tuotantotilaukselle määritetyn materiaalin toimintaa. Samaa periaatetta voidaan soveltaa tuotteille ja puolivalmiille tuotteille. Ellei näitä tuotteita ole luotu, siirretty tai kulutettu tuotantovirrassa, varastotapahtumat ovat valinnaisia. Sen jälkeen kun tuotteet on kirjattu varastoon, tuotantovirran KET-tili pienenee kyseisen standardikulun vähennyksellä.

## <a name="value-streams-and-value-stream-mapping"></a>Arvovirrat ja arvovirtojen yhdistäminen
Dynamics AX:n Lean-valmistuksen arkkitehtuuria on inspiroinut viisi Womack and Jonesin muotoilemaa Lean-periaatetta: asiakasarvo, arvovirta, virtaus, imu ja täydellisyys. Eräs hyväksytty tapa toteuttaa Lean-valmistuksen ratkaisuja valmistuksen fyysisessä maailmassa on arvovirtojen yhdistäminen (VSM). Rother and Shook esittelivät tämän tavan Learning to See -kirjassaan Lean Manufacturing Institutessa. 

Dynamics AX:ssä tulevan tilan arvovirta voidaan mallintaa tuotantovirtaversiona. Kaikki arvovirran prosessit mallinnetaan prosessitehtävinä. Liikkeet tai siirrot voidaan mallintaa siirtotehtävinä, jos siirtotila on rekisteröitävä, tai jos varastopoiminta tai konsolidoidut toimitukset vaativat integrointia. 

Itse arvovirta mallinnetaan Dynamics AX:n toimintayksikkönä. Tämän vuoksi arvovirtaa voidaan käyttää taloushallinnon dimensiona.

## <a name="costing-for-lean-manufacturing-based-on-the-production-flow"></a>Lean-valmistuksen kustannuslaskenta tuotantovirtaan perustuen
Ajoittainen tuotantovirran kustannusten konsolidaatio korjaa siihen liittyvän KET-tilin ja mahdollistaa tuotantovirran toimittamien tuotteiden varianssien määrittämisen.

## <a name="continuous-improvement"></a>Jatkuva parantaminen
Jotta ne tukisivat paremmin jatkuvaa parantamista, tuotantovirrat on toteutettu aikatehokkaina versioina. Tämän vuoksi aiemmin luotu tuotantovirran versio ja kaikki liittyvät kanban-säännöt voidaan kopioida tuotantovirran tulevaan versioon. Lisäksi tuleva tuotantovirta voidaan mallintaa ennen sen tarkistamista ja tuotantoon aktivoimista. Vanhojen tuotantovirran versioiden olemassa olevat kanbanit liitetään automaattisesti uuteen versioon. Näin varmistetaan saumaton materiaalivirta siirtymäpäivänä ja sen jälkeen.

## <a name="simplicity"></a>Yksinkertaisuus
Lean-valmistuksen toteuttamiseen Dynamics AX:ssä olemme valinneet tuotantovirta- ja tehtävä-menettelyn, joka mahdollistaa yksinkertaisten ja monimutkaisten tuotantoskenaarioiden mallintamisen yhdessä skaalautuvassa arkkitehtuurissa. Tarkempi toimintokonseptin tarkastelu paljastaa uuden yksinkertaisen elementin sitä todella tarvitseville: tuotannon ja logistiikan työntekijöille. Kun raportoidaan toimintoperusteisia tehtäviä varastotapahtumien sijaan, yhtenäinen, kaikkia Lean-valmistuksen variantteja koskeva käyttöliittymä siirtää liiketoiminnan monimutkaisuuden käyttöliittymästä sinne, mihin se kuuluu: tuotantovirtaan Lean-valmistuksen selkärankana.




