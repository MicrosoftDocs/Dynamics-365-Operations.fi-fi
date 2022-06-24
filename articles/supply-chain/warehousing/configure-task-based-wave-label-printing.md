---
title: Aallon etikettien tulostamisen ajoittaminen aallon aikana
description: Tässä artikkelissa kuvataan, miten tehtäväpohjaisen aallon etikettien tulostustoiminnon voi määrittää ja käyttää.
author: perlynne
ms.date: 06/09/2021
ms.topic: article
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ac2bc4cce42bada43334b82301d716414cd6d654
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889454"
---
# <a name="schedule-wave-label-printing-during-wave"></a>Aallon etikettien tulostamisen ajoittaminen aallon aikana

[!include [banner](../../includes/banner.md)]

Käytä *Tehtäväpohjainen aallon etikettitulostus* -ominaisuutta osana aaltoprosessia parantaaksesi tehokkuutta ja saadaksesi järjestelmän luomaan aallon etiketit ja toimimaan erillisissä tehtävissä.

Aallon etikettien tulostuksen määritys on monimutkainen prosessi, joka perustuu tarkkoihin konfiguraatioihin ja päätietoihin. Ei ole epätavallista, että aallon etikettien tulostuksen luonti epäonnistuu, ja kun näin tapahtuu, koko aaltoprosessi peruutetaan. *Tehtäväpohjaisen etikettien tulostustoiminnon* avulla voit välttää työn ja työrivien uudelleen luomisen aina, kun aallon lappu tulostetaan väärin.

Kun käytät *Tehtäväpohjaista aallon etikettien tulostustoimintoa*, järjestelmä luo ensin työn ja työrivit. Sen jälkeen se luo ja tulostaa aallon etiketit. Lopuksi, jos aallon etiketit on luotu oikein, se vapauttaa työn ja aallon keräystä varten.

## <a name="turn-on-the-task-based-wave-label-printing-feature-in-feature-management"></a>Ota tehtäväpohjainen aallon etikettitulostusominaisuudet käyttöön ominaisuuksien hallinnassa

Jos haluat käyttää tässä artikkelissa kuvattuja ominaisuuksia, niiden on oltava käytössä järjestelmässäsi. Ota [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa käyttöön ominaisuudet seuraavassa järjestyksessä:

1. *Aallon etikettien tulostus* – Tämä ominaisuus on pakollinen, jotta voit aaltoprosessimenetelmässä ottaa käyttöön aallon etikettien tulostuksen.
1. *Organisaation laajuinen töiden esto* – Tämä ominaisuus tarvitaan ajoitetun työn luomisen sekä manuaaliseen että automaattiseen määritykseen. (Supply Chain Managementin versiosta 10.0.21 alkaen tämä ominaisuus on pakollinen, joten se on oletusarvoisesti otettu käyttöön eikä sitä poistaa uudelleen käytöstä.)
1. *Tehtäväpohjainen aallon etikettien tulostaminen* – Tätä toimintoa tarvitaan, jotta aallon etiketti voidaan jakaa erilliseen tapahtuma-alueeseen.

## <a name="manually-enable-the-new-wave-step-method"></a>Uuden aallon vaihemenetelmän ottaminen käyttöön manuaalisesti

Luo ensin uusi aallon vaihemenetelmä ja ota se käyttöön rinnakkaisessa, asynkronisessa tehtävän käsittelyssä.

1. Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aallon käsittelymenetelmät**.
1. Valitse toimintoruudussa **Luo menetelmä uudelleen**. Huomaa, että *waveLabelPrinting* on lisätty aaltoprosessimenetelmien luetteloon, jota voit käyttää toimitusaaltomalleissasi.
1. Valitse tietue, jossa **Menetelmän nimi** -kentän arvoksi on asetettu *waveLabelPrinting* , ja valitse sitten toimintoruudusta **Tehtävän konfiguraatio**.
1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**. Määritä sitten uudelle rivillä seuraavat kentät:

    - **Varasto** – valitse varasto, jota käytetään työn luonnin käsittelyn aikatauluttamiseen. (Jos testausta varten käytetään esittelytietoja, voit valita varaston *24*.)
    - **Erätehtävien enimmäismäärä** – Määritä erätehtävien enimmäismäärä. Useimmissa tapauksissa arvon on oltava välillä *8* - *16*. Suosittelemme kuitenkin, että testaat skenaarioillesi parhaan asetuksesi.
    - **Aallon käsittelyn eräryhmä** – valitse erillinen aallon käsittelyn eräryhmä optimoimaan eräjonon käsittely.

Voit nyt päivittää aiemmin luodun aaltomallin niin, että se käyttää *Aallon etikettien tulostus* -aaltokäsittelymenetelmää. Voit myös luoda uuden aaltomallin, joka käyttää sitä.

1. Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**.
1. Valitse toimintoruudussa **Muokkaa**.
1. Valitse luetteloruudusta aaltomalli, jonka haluat päivittää. (Jos testausta varten käytetään esittelytietoja, voit valita varaston *24 - oletustoimitus*.)
1. Valitse **Menetelmät**-pikavälilehden **Jäljellä olevat menetelmät** -sarakkeessa rivi, jossa **Nimi** -kentän asetuksena on *waveLabelPrinting*.
1. Siirrä valittu rivi **Valitut menetelmät** -sarakkeeseen valitsemalla **lisää** (oikea nuolipainike).
1. Kirjoita **Aaltovaihekoodi**-kenttään se aaltovaihekoodi, jota käytetään muodostettaessa yhteys aaltomallista aallon etikettimalliin.

## <a name="set-wave-task-processing-threshold-data"></a>Aallon tehtävän käsittelyn raja-arvotietojen määrittäminen

Järjestelmä luo oletusarvoiset aallon tehtävän käsittelyn raja-arvotiedot, kun aaltokäsittely suoritetaan ensimmäisen kerran käyttämällä tehtävään perustuvaa käsittelyä. Näiden tietojen avulla määritetään, milloin aaltokäsittely suoritetaan asynkronisesti ja tehtävään perustuen, jolloin työn rinnakkainen käsittely ja luonti on mahdollista.

Oletustiedot käyttävät aluksi työtunnusten miniminumeron (`MinimumWorkThresholdForLabelPrinting`) raja-arvona lukua *1*. Siksi, kun järjestelmä käsittelee aallon, jossa on enemmän kuin yksi työtunnus, se käyttää erillisenä tapahtumana tehtäväpohjaista prosessointia aallon etiketteihin. Voit lisätä tai päivittää nämä tiedot manuaalisesti testiympäristöjen `WHSWaveTaskProcessingThresholdParameters`-taulukkoon. Voit muuttaa tätä asetusta tuotantoympäristössä pyytämällä päivityksen Microsoft-tuesta.

## <a name="changes-to-the-wave-processing-logic-when-task-based-wave-label-printing-is-used"></a>Muuttaa sen aallon käsittelylogiikkaan, kun tehtäväpohjaista aallon etikettien tulostusta käytetään

Jos aallon etikettien käsittely ylittää aallon tehtävien käsittelyrajan, tehtäväpohjainen käsittely aloitetaan. Seuraavassa aaltokäsittelyssä, joka sopii aaltomalliin, aallon etikettien tulostus suorittaa erillisen *ttsbegin*/*ttscommit* -tapahtuman välittömästi työn luonnin jälkeen. Jos työn vapauttaminen (eston poistaminen) on määritetty suoritettavaksi automaattisesti aaltomallissa, se suoritetaan vasta, kun aallon etikettien tulostusprosessi on suoritettu onnistuneesti loppuun.

Jos aallon etiketin luonti epäonnistuu (esimerkiksi työmäärän muuntaminen aallon etikettimääräksi epäonnistuu ja heittää virheen), vain asianmukainen tapahtuma epäonnistuu. Aiemmin luotu työ pysyy jäädytettynä. Voit korjata virheet ja tulostaa sen aallon etiketit noudattamalla seuraavia vaiheita.

1. Valitse **Varastonhallinta \> Lähtevät aallot \> Lähetysaallot \> Kaikki aallot**.
1. Valitse sopiva aalto ruudukossa.
1. Valitse toimintoruudun **Aalto**-välilehden **Tulosta**-ryhmässä **Aallon etiketit**.
1. Voit lähettää etiketit tulostettavaksi näyttöön tulevia ohjeita noudattamalla.
1. Valitse toimintoruudun **Aalto**-välilehden **Aalto**-ryhmästä **Vapauta**, jos haluat vapauttaa valitun aallon työt manuaalisesti.

## <a name="additional-resources"></a>Lisäresurssit

- [Aallon etiketin tulostus](configure-wave-label-printing.md)
- [Työn luomisen ajoitus aallon aikana](configure-wave-schedule-work-creation.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
