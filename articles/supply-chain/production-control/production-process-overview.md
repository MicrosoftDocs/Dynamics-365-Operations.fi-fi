---
title: Tuotantoprosessin yleiskatsaus
description: Tässä ohjeaiheessa on yleiskuvaus tuotantoprosesseista. Artikkelissa kuvataan tuotantotilausten, erätilausten ja kanbanien vaiheita tilauksen luonnista tilikauden sulkemiseen.
author: cvocph
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgShopSupervisorWorkspace, Kanban, ProdTable, ProdTableOverview, EcoResProductDiscreteManufacturingWorkspace, KanbanPrepareProductForLeanWorkspace, EcoResProductProcessManufacturingWorkspace, OpResLifecycleManagementWorkspace, ProdParmCostEstimation, ProdParmRelease, ProdSchedule, ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "19832"
- intro-internal
ms.assetid: 0e83c7ea-feba-4ed6-8717-8b48a3b8804a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 42a71d9f8a7229b147d5e322456c44c4d0d7b7f7303d8b13946eed7e68c75343
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776845"
---
# <a name="production-process-overview"></a>Tuotantoprosessin yleiskatsaus

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on yleiskuvaus tuotantoprosesseista. Artikkelissa kuvataan tuotantotilausten, erätilausten ja kanbanien vaiheita tilauksen luonnista tilikauden sulkemiseen. 

Tuotteiden tuotanto, jota kutsutaan toisinaan myös tuotannon elinkaareksi, noudattaa tiettyjä nimikkeen valmistamiseen vaadittavia vaiheita. Elinkaari alkaa tuotantotilauksen, erätilaus tai kanbanin luonnista. Se päättyy valmiiseen nimikkeeseen, joka on valmiina toimitettavaksi asiakkaalle tai toiseen tuotantovaiheeseen. Elinkaaren kussakin vaiheessa tarvitaan erilaisia tietoja prosessin suorittamiseksi. Kunkin vaiheen valmistuminen näkyy tuotantotilauksessa, erätilauksessa tai kanbanissa tuotannon tilan muuttumisena. Erityyppiset tuotteet edellyttävät erilaisia valmistusprosesseja.  

**Tuotannonhallinta**-moduuli on linkitetty muihin moduuleihin, joita ovat esimerkiksi **Tuotetietojen hallinta**, **Varastonhallinta**, **Kirjanpito**, **Varastonhallinta**, **Projektikirjanpito** ja **Organisaation hallinto**. Tämä integrointi tukee nimikkeen valmistamisessa vaadittavien tietojen kulkua.  

Tuotantoprosessiin vaikuttavat yleensä sille valitut kustannuslaskenta- ja varastonarvostusmenetelmät. Supply Chain Management tukee sekä todellisten kustannusten (\[FIFO\], \[LIFO\], liukuva keskiarvo ja kausittainen painotettu keskiarvo) että standardikustannusten laskentamenetelmiä. Lean-valmistus toteutetaan jälkikustannusperiaatteella.  

Kustannusten mittaustavan valinta määrittää myös materiaalien ja resurssien kulutusta koskevat raportointivaatimukset tuotantoprosessin aikana. Yleensä todellisten kustannusten menetelmät edellyttävät tarkkaa raportointia työn tasolla, kun taas kausittaisissa kustannusten laskumenetelmissä materiaalien ja resurssien kulutus voidaan raportoida yleisemmällä tasolla.

## <a name="mixed-mode-manufacturing"></a>Monen tilan tuotanto
Eri tuotteet ja tuotantotopologiat edellyttävät erilaisten tilaustyyppien käyttöä. Supply Chain Managementissa eri tilaustyyppejä voi käyttää monissa tiloissa. Toisin sanoen kaikki tilaustyypit voivat tapahtua yhden valmiin tuotteen valmistuksessa alusta loppuun.

-   **Tuotantotilaus** – Tämä on perinteinen tilaustyyppi, jolla tiettyä tuotetta tai tuotevarianttia valmistetaan tietty määrä määrättynä päivämääränä. Tuotantotilaukset perustuvat tuoterakenteisiin ja reitityksiin.
-   **Erätilaus** – Tätä tilaustyyppiä käytetään prosessiteollisuudessa ja erillisissä prosesseissa, joissa tuotannon muunto perustuu tiettyyn kaavaan tai joissa rinnakkais- ja sivutuotteet voivat olla lopputuotteita päätuotteen lisäksi tai sijasta. Erätilauksissa käytetään **Resepti**-tyyppisiä tuoterakenteita ja reitityksiä.
-   **Kanban** – Kanbaneilla ilmaistaan toistuvia lean-valmistusprosesseja, jotka perustuvat tuotantovirtoihin, kanban-sääntöihin ja tuoterakenteisiin.
-   **Projekti** – Valmistusprojektissa tuotteet ja palvelut yhdistyvät tiettyyn aikatauluun ja budjettiin. Tuotannon valmistusosuus voidaan toimittaa minkä tahansa muun tilaustyypin kautta.

## <a name="manufacturing-principles"></a>Valmistusperiaatteet
Tiettyä tuotetta ja niihin liittyviä markkinoita parhaimmin vastaavan valmistusperiaatteen valinnassa on otettava huomioon tuotanto- ja logistiikkavaatimukset sekä toimitusaikoihin liittyvät asiakkaiden odotukset.

-   **Valmistus varastoon** – Tämä on perinteinen valmistusperiaate, jossa tuotteita valmistetaan varastoon ennakoidun tai minimaalisen varastotäydennyksen mukaan (jälkimmäinen lasketaan yleensä ennakoidun tai historiallisen kulutuksen perusteella).
-   **Valmistus tilauksesta** – Vakiotuotteita valmistetaan tai viimeistellään tilauksesta. Vaikka esituotanto voidaan tehdä Valmistus varastoon -periaatteella, myynti- tai siirtotilaus voi käynnistää kalliita arvoketjun vaiheita tai variantteja luovia vaiheita.
-   **Määritys tilauksesta** – Valmistus tilauksesta -periaatteessa arvoketjun lopulliset työvaiheet suoritetaan tilauksesta. Tuotettavaa todellista tuotevarianttia ei määritetä etukäteen, vaan se luodaan tilausta syötettäessä myytävän tuotteen määritysmallin perusteella. Määritä tilauksesta -periaate edellyttää jonkin verran prosessin yhtenäistämistä tiettyä tuoteriviä varten.
-   **Suunnittelu tilauksesta** – Suunnittelu tilauksesta -prosessit liittyvät yleensä tilaukseen ja käynnistyvät tavallisesti suunnitteluvaiheessa. Suunnitteluvaiheessa suunnitellaan ja kuvaillaan varsinaiset tuotteet, joiden valmistusta tilauksen täyttäminen edellyttää. Tuotanto- ja erätilauksia tai kanbaneja voidaan tämän jälkeen luoda tuotteiden tuotantoa varten.

## <a name="overview-of-the-production-life-cycle"></a>Tuotannon elinkaaren yleiskatsaus
Seuraavat tuotannon elinkaaren vaiheet voivat tapahtua kaikille tilaustyypeille, joita monen tilan tuotannossa voidaan käyttää. Kaikkia ei kuitenkaan esitetä eksplisiittisenä tilauksen tilana.

1.  **Luotu** – Voit luoda tuotanto- tai erätilauksen tai kanbanin manuaalisesti tai määrittää järjestelmän luomaan ne erilaisten kysyntäsignaalien perusteella. Pääsuunnittelu luo tuotanto- tai erätilauksia tai kanbaneja, kun suunnitellut tilaukset vahvistetaan. Muita kysyntäsignaaleja ovat myyntitilaukset tai tarvekohdistetut signaalit muista tuotantotilauksista tai kanbaneista. Kanbaneissa, joissa määrä on kiinteä, kysyntäsignaalit luodaan, kun kanbanit rekisteröidään tyhjiksi.
2.  **Arvioitu** – Voit laskea materiaalin ja resurssien kulutuksen arviot. Arvio luo raaka-aineista varastotapahtumia, joiden tilana on **Tilauksessa**. Pää-, rinnakkais- ja sivutuotteiden vastaanotot luodaan tuotanto- tai erätilauksia arvioitaessa. Jos tuoterakenne sisältää rivejä, joiden tyyppi on **Tarvekohdistuksen tarjonta**, järjestelmä luo ostotilaukset materiaaleista tai alihankkijoille työvaihepalveluista ja tarvekohdistaa ne tuotanto- tai erätilaukseen. Nimikkeet tai tilaukset varataan tuotantotilauksen varausstrategian mukaisesti, ja valmiiden tavaroiden hinta lasketaan parametriasetusten perusteella.
3.  **Ajoitettu** – Voit ajoittaa tuotannon työvaiheiden, yksittäisten töiden tai molempien perusteella.
    -   **Työvaiheiden ajoitus** – Tämä ajoitusmenetelmä antaa karkean pitkän aikavälin suunnitelman. Tämän menetelmän avulla voit määrittää tuotantotilauksille aloitus- ja päättymispäivät. Jos tuotantotilaukset on liitetty reitityksen työvaiheisiin, voit määrittää ne kustannuspaikkaryhmiin.
    -   **Töiden ajoitus** – Tämä ajoitusmenetelmä antaa yksityiskohtaisen suunnitelman. Jokainen työvaihe koostuu yksittäisistä töistä, joille on määritetty päivämäärät, ajat ja operatiiviset resurssit. Jos käytetään rajallista kapasiteettia, työt määritetään operatiivisille resursseille käytettävyyden perusteella. Voit tarkastella ja muuttaa aikataulua Gantt-kaaviossa.
    -   **Kanban-aikataulu** – Kanban-työt ajoitetaan kanban-aikataulun mukaan tai automaattisesti kanban-sääntöjen automaattisen suunnittelukonfiguraation perusteella.

4.  **Vapautettu** – Voit vapauttaa tuotantotilauksen tai erätilauksen, kun ajoitus on valmis ja materiaali voidaan keräillä tai valmistaa. Materiaalin saatavuustarkistuksen avulla tuotannon esimies voi arvioida tuotanto- tai erätilauksissa tarvittavien materiaalien saatavuutta. Voit myös tulostaa tuotantotilausasiakirjoja, esimerkiksi keräilyluettelot, työkortin, reitityskortin ja reititystyön. Kun tuotantotilaus vapautetaan, tilauksen tila muuttuu sen merkiksi, että tuotanto voi alkaa. Varastonhallintaa käytettäessä tuotantotilauksen tai erätilauksen vapauttaminen vapauttaa tuotannon tuoterakennerivit varastonhallintaan. Varastoaallot ja -työ luodaan tämän jälkeen varaston asetusten mukaan.
5.  **Laadittu**/**Keräilty** – Kun kaikki materiaalit ja resurssit on vaiheistettu tuotantopaikassa, tuotannon tuoterakennerivien tai kanban-rivien tilaksi päivittyy **Keräilty**. Tarvekohdistetut toimitustilaukset ja niihin liittyvät varastotyöt suoritetaan yleensä tässä vaiheessa. Kanban-kortit tai työkortit, joita tarvitaan tuotannon edistymisestä raportointiin, on määritettävä ja tulostettava.
6.  **Aloitettu** – Kun tuotantotilaus, erätilaus tai kanban aloitetaan, voit raportoida materiaalien ja resurssien kulutuksesta tilausta kohti. Järjestelmä voidaan määrittää kirjaamaan tilaukseen kohdistettujen materiaalien ja resurssien kulutus, kun tilaus käynnistetään. Tätä kohdistusta kutsutaan nimellä ennakkopoisto tai automaattikulutus. Voit kohdistaa materiaaleja tuotantotilauksiin tai erätilauksiin manuaalisesti luomalla lisää keräysluettelokirjauskansioita. Voit myös manuaalisesti kohdistaa työ- ja muita rutiinikustannuksia tilaukseen. Jos käytät työvaiheiden ajoitusta, voit kohdistaa nämä kustannukset luomalla reitityskorttikirjauskansion. Jos käytät töiden ajoitusta, voit kohdistaa nämä kustannukset luomalla työkorttikirjauskansion. Tuotanto- tai erätilauksia voi aloittaa erissä, jotka sisältävät lopullisen vaaditun määrän. Tuotanto- tai erätilaukseen tai kanbaniin luodut työt voidaan aloittaa ja niistä voidaan raportoida erikseen kirjauskansioiden, tuotannonohjauspäätteen tai kanban-taulujen kautta.
7.  Raportoi edistymisestä /**Valmiit** työt – Raportoi tuotannon edistymisestä työn tai resurssin mukaan käyttämällä tuotannonohjauspäätettä, tuotannon kirjauskansioita, kanban-tauluja tai mobiiliskannausominaisuuksia. Materiaalien ja resurssien kulutus kirjataan ja niihin liittyvien kanbanien, tuotantotilausten ja erätilausten tilaksi voidaan päivittää **Vastaanotettu** tai **Ilmoitettu valmiiksi**. Varaston poispanotyö voidaan luoda varastomäärityksen mukaan.
8.  **Ilmoitettu valmiiksi** (tuotteen vastaanotto) – Kun tuotanto- tai erätilaus ilmoitetaan valmiiksi, valmiiden tavaroiden määrä päivitetään varastoon. Tämä määrä sisältää tärkeimpien rinnakkais- ja sivutuotteiden määrän. Jos käytät keskeneräisten töiden (KET) kirjanpitoa, kirjanpidon kirjauskansio luodaan, jotta KET-tilejä voidaan vähentää ja valmiiden tavaroiden varastoa voidaan lisätä. Kun tuotantotilauksen kustannukset lasketaan, tuotannon toteutuneet kustannukset kirjataan. Jos tuotantoon liittyviä materiaali- ja työkustannuksia ei ole vielä kohdistettu kirjauskansiossa tai ennakkopoiston avulla, ne voidaan automaattisesti kohdistaa jälkipoiston avulla. Jälkipoiston avulla tapahtuvaan kohdistukseen sisältyy varastotapahtumien prosessien jälkivähentäminen. Jos tuotantotilaus on valmis, valitse **Lopeta työ** -valintaruutu, niin jäljellä olevaksi tilaksi muuttuu **Päättynyt**. Muussa tapauksessa kenttä jätetään tyhjäksi, jos haluat sallia tuotettujen lisämäärien raportoinnin.
9.  **Laadunarviointi** – Tuotteen vastaanotto voi käynnistää laatutilausten luonnin testausprosessien sisällön ja tietyille tuotteille määritettyjen laatusääntöjen mukaan. Koska laatutilaus voi päivittää testattujen tuotteiden varastotilan tai erämääritteet, laadunarviointi on monilla aloilla pakollinen prosessi.
10. **Pantu pois** ja **Lähetä tilauksesta** – Tuotteen vastaanoton ja laadunarvioinnin jälkeen valinnainen poispanotyö ohjaa vastaanotetut tuotteet seuraavaan käyttökohteeseen, valmiiden tuotteiden varastoon tai kuljetusalueelle, jos tuotteita lähetetään tilauksesta.
11. **Päättynyt** – Ennen tuotannon lopettamista lasketaan tuotetun määrän toteutuneet kustannukset. Kaikki arvioidut materiaali-, työ- ja yleiskustannukset palautetaan ja korvataan toteutuneilla kustannuksilla. Jos valitset **Lopeta työ** -valintaruudun suorittaessasi kustannuslaskennan, tuotantotilauksen tilaksi tulee **Päättynyt**. Tämä tila estää lisäkustannusten kirjaamisen valmiiseen tuotantotilaukseen.
12. **Kauden sulkeminen** – Jotkin kustannuslaskennan periaatteet, kuten kausittainen keskiarvo, jälkikustannuslaskenta, FIFO tai LIFO, edellyttävät ajoittaisia toimita, jotta varasto tai tilikausi voidaan sulkea. Yleensä järjestelmä yrittää raportoida kaikkien materiaalien ja resurssien kulutuksesta ja varaston sekä hävikin oikaisuista ennen kausien sulkemista. Tämä raportointi tehdään yleensä käyttämällä varaston siirtokirjauskansioita tai oikaisun kirjauskansioita. Tavoitteena on arvioida toimintayksiköiden taloudellista suorituskykyä kullakin kaudella. Joskus kun käytetään pitkäaikaisia tuotantotilauksia, jotka kattavat koko taloudellisen raportointijakson, tuotantokirjauskansioiden avulla voidaan raportoida tuotannon edistymisestä ja resurssien kulutuksesta kauden lopussa.


## <a name="additional-resources"></a>Lisäresurssit

[Tuotannon palaute](production-feedback.md)

[Tuotekonfiguraatiomallien yleiskatsaus](../pim/product-configuration-models.md)

[Lean-valmistuksen yleiskatsaus](lean-manufacturing-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]