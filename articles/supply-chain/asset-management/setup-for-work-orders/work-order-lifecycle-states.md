---
title: Työtilauksen elinkaaren tilat
description: Tässä artikkelissa selitetään työtilausten elinkaaren tilat käyttöomaisuuden hallinnassa.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderLifecycleState, EntAssetWorkOrderLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9c6a7c204370542353e9b629b78091972f8ce9a1
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017084"
---
# <a name="work-order-lifecycle-states"></a>Työtilauksen elinkaaren tilat


[!include [banner](../../includes/banner.md)]

 

Työtilauksen elinkaaritilat määrittävät tilat, joita työtilaus voi käydä läpi. Esimerkkejä ovat **Luotu**, **Ajoitettu**, **Käsittelyssä** ja **Päättynyt**. Työtilauksen elinkaaritilat voidaan päivittää manuaalisesti työtilaukseen tai ne voidaan päivittää automaattisesti (esimerkiksi työtilausten ajoituksessa).

Työtilausten vaatimat elinkaaritilat on liitettävä vastaviin projektivaiheisiin **Projektinhallinnan ja kirjanpidon parametrit** -sivulla (**Projektinhallinta ja kirjanpito** \> **Projektinhallinnan ja kirjanpidon parametrit**). Ensin määritetään projektin vaiheet kohdassa Projektinhallinta ja kirjanpito. Tämän jälkeen määrität työtilausten elinkaaritilat ja työtilausten elinkaarimallit käyttöomaisuuden hallinnassa.

Seuraavassa taulukossa on kuvattu vaihtoehdot **Työtilaus**- ja **Ajoita**-osissa **Yleiset**-välilehdessä **Työtilauksen elinkaaren tila** -sivulla (**Resurssien hallinta** \> **Asetukset** \> **Työtilaukset** \> **Elinkaaren tilat**).

![Työtilauksen elinkaaren tila -sivu.](media/09-setup-for-work-orders.png)

| Vaihtoehdon nimi                   | kuvaus |
|-------------------------------|-------------|
| Käytössä                        | Määritä asetukseksi **Kyllä**, jos työtilauksen on oltava aktiivinen tässä elinkaaritilassa. |
| Lisää rivi                      | Määritä asetukseksi **Kyllä**, jos työtilauksen töitä voidaan lisätä tässä elinkaaritilassa olevaan työtilaukseen. |
| Poista                        | Määritä asetukseksi **Kyllä**, jos työtilaus voidaan poistaa tässä elinkaaritilassa. |
| Poista rivi                   | Määritä asetukseksi **Kyllä**, jos työtilauksen töitä voidaan poistaa tässä elinkaaritilassa olevasta työtilauksesta. |
| Salli ajoitus              | Määritä asetukseksi **Kyllä**, jos työtilaus voidaan ajoittaa tässä elinkaaritilassa. |
| Aseta toteutunut aloitus              | Määritä asetukseksi **Kyllä**, jos käyttäjää kehotetaan valitsemaan todellinen alkamispäivämäärä ja -aika työtilaukselle, kun se päivitetään tähän elinkaaritilaan. |
| Aseta toteutunut lopetus                | Määritä asetukseksi **Kyllä**, jos käyttäjää kehotetaan valitsemaan todellinen lopetuspäivämäärä ja -aika työtilaukselle, kun se päivitetään tähän elinkaaritilaan. |
| Kirjaa kirjauskansiot                 | Määritä asetukseksi **Kyllä**, jos työtilauksen kirjauskansiot pitäisi automaattisesti krjata, kun työtilaus päivitetään tähän elinkaaritilaan. Jos kirjauskansion kirjauksen aikana tapahtuu virhe, näkyviin tulee sanoma ja työtilauksen elinkaaritilan päivitys peruutetaan. Voit tarkastella työtilauksen kirjauskansiorivejä valitsemalla **Resurssien hallinta** \> **Työtilaukset** \> **Kaikki työtilaukset**, **Aktiiviset työtilaukset** tai **Omat aktiiviset työtilaukset**. Valitse työtilaus luettelosta ja valitse lopuksi **Kirjauskansiot**. Tämän automaattisen työtilauksen kirjauskansion kirjaamisen määrittäminen tietyssä elinkaaritilassa on sama asia kuin silloin, kun valitset **Työtilauksen kirjauskansiot** -sivulla **Kirjaa kirjauskansiot**.<p>**Huomautus:** Jos määrität tämän asetuksen arvoksi **Kyllä**, kirjauskansiot kirjataan automaattisesti, jos hyväksymisen työnkulkua ei ole määritetty. Jos yrityksessä käytetään kirjauskansion hyväksymisasetuksia, jotka on määritetty **Kirjauskansion hyväksyminen** -sivulla (**Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Kirjauskansiot**\> **Kirjauskansion hyväksyminen**), esimiehen tai virkailijan on tarkistettava kulutusrekisteröinnit ja kirjattava ne.</p> |
| Ylläpidon tarkistuslistan käsittely | Määritä asetukseksi **Kyllä**, jos kaikki liitetyt ylläpidon tarkistuslistat tulisi käsitellä, kun työtilaus päivitetään tähän elinkaaritilaan. Osana tätä käsittelyä huoltotarkistusluetteloon tehdyt mahdolliset vastarekisteröinnit kirjataan ja koko huollon tarkistusluettelon tulokset arvioidaan. Huollon tarkistusluettelon rivit, joissa on **hyväksytty** ja **hylätty**-tuloksia, arvioidaan ja jos vähintään yksi rivi ei ole hyväksytty, koko huollon tarkistusluettelo merkitään käyttöomaisuuden hallinnassa arvolla **Hylätty**. |
| Valm.                         | Määritä tämän vaihtoehdon arvoksi **Kyllä**, jos työtilauksen työaikataulun tilaksi päivitetään **Valmis** kaikille työtilaukselle luoduille työtilaustöille automaattisesti, kun työtilaus päivitetään tähän elinkaaritilaan. |
| Alku                         | Määritä tämän vaihtoehdon arvoksi **Kyllä**, jos työtilauksen työaikataulun tilaksi päivitetään **Aloitettu** kaikille työtilaukselle luoduille työtilaustöille automaattisesti, kun työtilaus päivitetään tähän elinkaaritilaan. |
| Loppu                           | Määritä tämän vaihtoehdon arvoksi **Kyllä**, jos työtilauksen työaikataulun tilaksi päivitetään **Päättynyt** kaikille työtilaukselle luoduille työtilaustöille automaattisesti, kun työtilaus päivitetään tähän elinkaaritilaan. |
| Poista aikataulutetut rivit         | Määritä tämän vaihtoehdon arvoksi **Kyllä**, jos kaikki työtilaukselle luotujen työtilaustöiden ajoitus, joka on jo ajoitettu, tulisi poistaa, kun työtilaus päivitetään tähän elinkaaritilaan. Toisin sanoen käyttöomaisuuserän kunnossapitotyöntekijä, työkalut ja kapasiteettivaraukset poistetaan. Voit esimerkiksi määrittää tämän asetuksen arvoksi **kyllä** työtilauksen elinkaaritilassa, jonka nimi **Arvioitu**. Tämän jälkeen, kun työtilaus palautetaan takaisin tähän elinkaaritilaan, koska uudelleenajoitus on tarpeen, ajoitus voidaan poistaa kyseisestä työtilauksesta. |

## <a name="set-up-project-stages-and-work-order-lifecycle-states"></a>Projektin vaiheiden ja työtilausten elinkaaritilojen määrittäminen

1. Valitse **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Projektinhallinnan ja kirjanpidon parametrit**.
2. Valitse **Projektin vaihe** -välilehdessä kussakin vaiheessa, jota haluat käyttää, jokaisen työtilauksiin vaadittavan projektityypin valintaruutu. Projektityypit määrittävät sallitut taloustehtävät. Taloudellisia tehtäviä ovat esimerkiksi ennusteen luominen, arvioiden luominen ja alkusaldojen luominen.

    > [!IMPORTANT]
    > Jos projektityypille ei ole valittu projektivaihetta, mutta projektin vaihetta käytetään työtilauksen elinkaaritilassa, työtilauksen projekteja ei päivitetä asianmukaisella tavalla.

3. Sulje **Projektinhallinnan ja kirjanpidon parametrit** -sivu.
4. Valitse **Resurssien hallinta** \> **Asetukset** \> **Työtilaukset** \> **Elinkaaren tilat**.
5. Luo uusi työtilauksen elinkaaren tila valitsemalla **Uusi**.
6. Kirjoita **Elinkaaren tila** -kenttään elinkaaren tilan tunnus.
7. Anna nimi **Nimi**-kenttään.

    **Tiedot**-pikavälilehden **Elinkaarimallit**-kentässä näkyy niiden työtilausten elinkaarimallien määrä, jotka käyttävät tätä elinkaaritilaa.

8. Valitse **Yleiset**-pikavälilehden **Työtilaus**-osassa toiminnot, jotka ovat käytettävissä tässä elinkaaritilassa, määrittämällä asianmukaisten asetusten arvoksi **Kyllä**. Asetusten kuvaukset ovat tässä artikkelissa edellä esitetyssä taulukossa.
9. Valitse **Projekti**-osan **Vaihe**-kentästä projektin vaihe, joka liittyy tähän elinkaaritilaan.
10. Määritä **Projekti**-osassa **Sulje tehtävät** -asetukseksi **Kyllä**, jos kuhunkin työtilaustyöhön liittyvät projektitehtävät suljetaan automaattisesti, kun työtilaus on tässä elinkaaritilassa.

    > [!NOTE]
    > Voit etsiä työtilaustyöhön liittyvän projektitehtävän numeron valitsemalla **Resurssien hallinta** \> **Työtilaukset** \> **Kaikki työtilaukset**, **Aktiiviset työtilaukset** tai **Omat aktiiviset työtilaukset**. Avaa työtilaus ja valitse sitten työtilauksen työ. Tehtävän numero näkyy **Rivin tiedot** -pikavälilehden **Yleiset**-välilehden **Projekti**-osan **Tehtävän numero**-kentässä.

11. Määritä **Ennuste**-osassa **Kopioi tuntiennuste**-, **Kopioi nimike-ennuste**- ja/tai **Kopioi kuluennuste** -asetukseksi **Kyllä**, jos työtilauksen projektiennusteet tulisi kopioida automaattisesti työtilauksen kirjauskansioihin, kun työtilaus on tässä elinkaaritilassa.
12. Määritä **Ajoita**-osassa jokin vaihtoehdoista arvoksi **Kyllä**, jos työtilauksen töiden ajoituksen tila tulisi päivittää, kun työtilaus on tässä elinkaaritilassa. Lisätietoja **Valmis**- **Aloitus**-, **Loppu**- ja **Poista ajoitusrivit** -asetuksista on aiemmin tässä artikkelissa olevassa taulukossa.

    > [!NOTE]
    > Voit tarkastella työtilaustyöhön liittyviä ajoitusrivejä valitsemalla **Resurssien hallinta** \> **Työtilaukset** \> **Kaikki työtilaukset**, **Kaikki työtilaukset** tai **Omat aktiiviset työtilaukset**. Avaa työtilaus, valitse työtilauksen työ **Työtilauksen työ**-pikavälilehdessä ja tarkastele liittyviä tietoja **Rivin tiedot** -pikavälilehdessä. **Ajoitus**-välilehden **Tila**-kentässä näkyy työtilaustyön tila. **Tila** -kentän arvoksi voidaan määrittää seuraavat arvot: **Ajoitettu**, **valmis**, **aloitettu**, **pysäytetty** ja **päättynyt.**

13. Valitse **Ylläpitopyynnöt**-osan **Elinkaaren tila** -kentässä ylläpitopyynnön elinkaaritila, johon liittyvät kunnossapitopyynnöt päivitetään. Tämä päivitys tapahtuu automaattisesti. Se voidaan tehdä vain, jos ylläpitopyynnön elinkaarimallissa on valittu ylläpitopyynnön elinkaaritila, jota käytetään kunnossapitopyynnössä.
14. Määritä **Resurssi**-osassa **Päivitä resurssirakenne** -asetukseksi **Kyllä**, jos kaikki työtilauksessa käytettävät nimikkeet tulisi automaattisesti päivittää **Resurssirakenne**-sivulla, kun työtilaus päivitetään tähän elinkaaritilaan. Tämä asetus voi olla merkityksellinen, jos esimerkiksi työtilauksen elinkaaren tila määrittää työtilauksen valmiiksi tai päättyneeksi.
15. Määritä **Työtilauspooli** -osassa **Poista pooliviittaus** -asetukseksi **Kyllä**, jos tässä elinkaaritilassa olevat työtilaukset poistetaan automaattisesti työtilauspooleista.
16. Valitse **Vahvista**-pikavälilehdessä tässä elinkaaritilassa aktivoitavat vahvistustyypit määrittämällä asianmukaiset asetukset arvoon **Kyllä**. Valitse kunkin valitsemasi vahvistustyypin **Tyyppi**-kentässä sanomatyyppi, joka näytetään, jos vahvistustyyppiin liittyviä pakollisia kenttiä ei ole vahvistettu. Jos valitset **Virhe**, työtilauksen eli kaaritilan päivitys peruutetaan, kunnes siihen liittyvät pakolliset kentät on päivitetty työtilauksessa.

    - Asetukset **Ylläpidon käyttökatko**, **Ylläpidon tarkistuslista**, **Vian oire**, **Vian syy** ja **Vian korjaus** liittyvät asetuksiin **Työtilaustyypit**-sivun **Pakollinen**-osassa (**Resurssien hallinta** \> **Asetukset** \> **Työtilaukset** \> **työtilaustyypit**). Jotta nämä vahvistukset voidaan aktivoida, niihin liittyvien asetusten on myös oltava arvossa **Kyllä** työtilauksessa käytettävän työtilaustyypin osalta.
    - Jos **Ylläpidon tarkistuslista** -asetukseksi on määritetty **Kyllä** elinkaaren tilassa, johon työtilaus päivitetään, oikeellisuustarkistus tehdään sen tarkistamiseksi, että huollon tarkistusluettelon rivit, jotka on merkitty arvolla **Pakollinen**, on rekisteröity joko merkillä **Tarkistettu** tai **Ei käytettävissä**. Jos kumpaakaan näistä rekisteröinneistä ei ole tehty pakollisilla riveillä, näytetään tieto-, virhe-tai varoitussanoma, kun työtilaus päivitetään tähän elinkaaritilaan.
    - Jos Sidottu kustannus -vaihtoehdon arvoksi on **asetettu** **Kyllä** sen elinkaaritilan osalta, johon työtilaus päivitetään, sidottujen kustannusten kokonaissumma (eli kokonaiskulujen kokonaissumma, jonka oikeushenkilö on sitoutunut maksamaan) lasketaan kullekin työtilaustyölle. Näkyviin tulee sanoma, jos sidotun kustannuksen summa on suurempi kuin 0 (nolla). Voit valita kustannussitoumusten tyypit **Kustannussitoumukset**-pikavälilehdessä **Kustannusseuranta**-välilehdessä **Projektinhallinnan ja kirjanpidon parametrit** -sivulla (**Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Projektinhallinnan ja kirjanpidon parametrit**).
    - Jos **Ylläpidon käyttökatko** -asetukseksi on määritetty **Kyllä** elinkaaren tilalle, johon työtilaus on päivitetty, kunnossapitoseisokkien oikeellisuustarkistus tehdään työtilaukseen liittyvälle resurssille. Jos kunnossapitoseisokkimerkintä on tehty, mutta ei ole **Päättynyt**-rekisteröintiä, näkyviin tulee sanoma, kun työtilaus päivitetään tähän elinkaaritilaan.
    - Jos projektin vakioasetukset eivät sisällä kaikkia käyttöomaisuuden hallinnan asetuksiin liittyviä vaiheita, voit määrittää käyttäjän määrittämiä projektin vaiheita  **Projektinhallinnan ja kirjanpidon parametrit** -sivun **Projektin vaiheet**-välilehdessä. Seuraavassa kuvassa näkyy **Projektinhallinnan ja kirjanpidon parametrit** -sivun **Projektin vaihe** -välilehti.

    ![Eri projektityyppien projektivaiheiden määrityssivu.](media/10-setup-for-work-orders.png)

> [!NOTE]
> Jos työtilauksen elinkaaritila johon päivitetään on ei-aktiivinen, työtilaukseen liittyvät kirjauskansiot, joita ei vielä ole kirjattu, poistetaan automaattisesti. Tämä toiminto auttaa takaamaan käyttämättömien tietojen automaattisen tyhjennyksen. (Elinkaari tila ei ole käytössä, **Aktiivinen**-asetukseksi on määritetty **Ei** **Yleiset** pikavälilehdessä **Työtilauksen elinkaaren tila** -sivulla.)
>
> Jos kuitenkin määrität työtilauksen manuaalisesti ei-aktiiviseksi, työtilaukseen liittyvät kirjauskansioita, joita ei vielä ole kirjattu, **ei** poisteta automaattisesti. (Jos haluat työtilauksen passiiviseen tilaan manuaalisesti, valitse **Resurssien hallinta** \> **Työtilaukset** \> **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**. Avaa työtilaus ja siirry **Otsikko**-näkymään. Valitse **Yleiset**-pikavälilehdessä **Muokkaa** ja määritä sitten **Aktiivinen**-asetukseksi **Ei**.)

## <a name="relations-among-work-order-lifecycle-models-work-order-types-and-work-order-lifecycle-states"></a>Työtilaustyyppien, työtilauksen elinkaaritilojen ja työtilauksen elinkaarimallien väliset suhteet

Elinkaarimallit viittaavat työnkulkuihin, ja elinkaaritilat valitaan elinkaarimallissa peräkkäisessä järjestyksessä. Elinkaarimallit määritetään työtilaustyypeille. Työtilaustyypit määräävät työnkulkujen ja työprosessien koon tai laajuuden. Esimerkiksi **Ylläpito**, joka on vakiotyötilaustyyppi, voi liittyä työtilauksen elinkaarimalliin, jossa on useita elinkaaritiloja. Sen sijaan sinulla voi olla työtilaustyyppi **Korjaava**, jota käytetään työtilauksissa, joita ei ole ajoitettu, tai työtilauksille, joiden työ on päättynyt, ennen kuin työtilaus on tehty (kiireellisen tilanteen vuoksi). Tämä työtilaustyyppi voi liittyä työtilauksen elinkaarimalliin, jossa on vain muutamia elinkaaritiloja.

Tyyppien käyttämisen syy on se, että kun tyyppi on määritetty esimerkiksi työtilaukselle tai resurssille, siihen liittyvät työprosessit (elinkaaritilat) määritetään automaattisesti. Lisätietoja työtilaustyyppien määrittämisestä on kohdassa [Työtilaustyypit](../setup-for-work-orders/work-order-types.md).

> [!NOTE]
> Elinkaaritilat, elinkaarimallit ja -tyypit koskevat työtilausten lisäksi toiminnallisia sijainteja, resursseja ja ylläpitopyyntöjä.

Seuraavassa kuvassa näkyy työtilaustyyppien, elinkaarimallien ja elinkaaritilojen välinen suhde.

![Työtilauksen tyyppisivu verrattuna työtilauksen elinkaarimallisivuun.](media/11-setup-for-work-orders.png)

## <a name="work-order-lifecycle-models"></a>Työtilausten elinkaarimallit

Kun olet luonut työtilauksille tarvittavat elinkaaritilat, ne voidaan jakaa työtilauksen elinkaarimalleihin. Luo vähintään yksi vakioelinkaarimalli.

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Työtilaukset** \> **Elinkaarimallit**.
2. Luo uusi työtilauksen elinkaarimalli valitsemalla **Uusi**.
3. Kirjoita **Elinkaarimalli** -kenttään elinkaarimallin tunnus.
4. Anna nimi **Nimi**-kenttään.

    **Tiedot**-välilehden **Elinkaaren tilat**-kentässä näkyy niiden elinkaaren tilojen määrä, jotka on valittu tässä elinkaarimallissa. **Työtilaustyypit**-kentässä näkyy tätä elinkaarimallia käyttävien työtilausyyppien määrä.

5. Valitse **Elinkaaren tilat** -pikavälilehdessä ne elinkaaren tilat, jotka sisällytetään elinkaarimalliin.

    - Jos haluat sisällyttää elinkaaren tilan elinkaarimalliin, valitse se **Jäljellä olevat elinkaaren tilat** -osiosta ja valitse sitten oikealle osoittava nuolipainike ![Oikea nuoli.](media/12-setup-for-work-orders.png) siirtääksesi sen **Valitut elinkaaren tilat** -osioon.
    - Jos haluat lisätä kaikki käytettävissä olevat elinkaaritilat elinkaarimalliin, valitse **Valitse kaikki käytettävissä olevat vaiheet** -painike ![Valitse kaikki käytettävissä olevat vaiheet.](media/13-setup-for-work-orders.png). Kaikki elinkaaritilat siirretään **Valitut elinkaaren tilat** -osioon.
    - Jos haluat poistaa elinkaaren tilan elinkaarimallista, valitse se **Valitut elinkaaren tilat** -osiosta ja valitse sitten vasemmalle osoittava nuolipainike ![Vasen nuoli.](media/14-setup-for-work-orders.png) siirtääksesi sen **Jäljellä olevat elinkaaren tilat** -osioon.

6. Valitse **Elinkaaren tilan päivitykset** määrittääksesi, mitkä elinkaaren tilat voivat seurata valittua elinkaaren tilaa.
7. Valitse **Päivitykset**-pikavälilehden **Ajoitettu-tila**-kentästä elinkaaritila, joka on aina valittava työtilaukselle, jonka työtilauksen ajoitus on tehty, riippumatta siitä, mikä on työtileuksen edellinen elinkaaren tila.
8. Valitse **Ajoittamattoman elinkaaren tila** -kentässä elinkaaritila, joka on aina valittava työtilaukselle, jos työtilauksen ajoittaminen poistetaan.
9. Tallenna työtilauksen elinkaarimalli.

![Työtilausten elinkaarimallit -sivu.](media/15-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]