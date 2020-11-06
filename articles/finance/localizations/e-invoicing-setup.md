---
title: Sähköisen laskutuksen lisäosan määrittäminen
description: Tässä aiheessa selitetään, miten sähköisen laskutuksen lisäosa määritetään Microsoft Dynamics 365 Financessa ja Dynamics 365 Supply Chain Managementissa.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 7e631f1bf64b47b5f3e85d4f98c6edafe67d627a
ms.sourcegitcommit: d6250ee5ced43be39e789324a895fd1c07178935
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/19/2020
ms.locfileid: "4039889"
---
# <a name="set-up-the-electronic-invoicing-add-on"></a>Sähköisen laskutuksen lisäosan määrittäminen

[!include [banner](../includes/banner.md)]


Sähköisen laskutuksen lisäosatoiminnon määritys on prosessi, jossa luodaan tarvittavat määritykset RCS (Regulatory Configuration Services) -ympäristön kautta ja julkaistaan tämä määritys sähköisen laskutuksen lisäosapalvelimelle. Määrityksessä voit luoda määritettävissä olevia sääntöjä, joiden avulla sähköisen laskutuksen lisäosa voi käyttää suojattua protokollaa internetissä viestiäkseen ja vaihtaakseen tietoja kolmannen osapuolen yksikön kanssa verkkopaovelujen kautta.

Määritettävyys perustuu sähköisen raportoinnin (ER) muodon määritykseen tapana koota sisältöä, jota lähetetään ja vastaanotetaan digitaalisten tiedostojen kautta. Siinä käytetään myös sellaisten viestintätoimintojen orkestrointiin, joilla lähetetään pyyntöjä ja vastaanotetaan vastauksia kolmannen osapuolen verkkopalveluista ilman tarvetta kirjoittaa koodia.

## <a name="overview"></a>Yleiskuvaus

Sähköisen laskutuksen lisäosatoiminto on sen resurssin yleinen nimi, joka määritetään ja julkaistaan käytettäväksi sähköisen laskutuksen lisäosan palvelimella. Toimintomäärityksessä yhdistyvät muun muassa ER-määrityksen muodot määritettävien vienti- ja tuontitiedostojen luomista varten sekä toimintojen ja toimintokulkujen käyttäminen määritettävien pyyntöjen lähettämisen sääntöjen luomiseen, vastausten tuomiseen sekä vastausten sisältöjen jäsentämiseen.

Seuraavassa kuvassa näkyvät sähköisen laskutuksen lisäosatoiminnon keskeisimmät osat.

![Sähköisen laskutuksen lisäosatoiminnon yleiskatsaus](media/e-Invoicing-services-feature-setup-Overview-e-Invoicing-feature.png)

Laskumuotojen ja toimintokulkujen vaihtelun vuoksi toiminnon määritys voi vaihdella maan tai alueen tai liiketoiminnan vaatimusten mukaan.

## <a name="set-up-the-electronic-invoicing-add-on-feature"></a>Sähköisen laskutuksen lisäosatoiminnon määrittäminen

Määritysprosessi on suoritettava RCS-ympäristössä. Voit luoda uuden sähköisen laskutuksen lisäosatoiminnon noudattamalla seuraavia ohjeita.

1. Kirjaudu RCS-ympäristöön.
2. Valitse **Globalisaatio-ominaisuukset** -työtilan **Toiminnot** -osassa **Sähköisen laskutuksen lisäosa** -ruutu.
3. Valitse **Sähköisen laskutuksen lisäosatoiminnot** sivulla **Tuo** tuodaksesi ER-tietomallin määrityksen yleisestä säilöstä.
4. Valitse **Lisää** luodaksesi sähköisen laskutuksen lisäosatoiminnon. Voit joko luoda toiminnon tyhjästä tai johtaa sen aiemmin luodusta sähköisen laskutuksen lisäosatoiminnosta.

    ![Sähköisen laskutuksen lisäosatoiminnon lisääminen](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature.png)

> [!NOTE]
> Kun luot uuden sähköisen laskutuksen lisäosatoiminnon, sillä on versionumero ja sen oletustilaksi on määritetty **Luonnos**.

### <a name="configurations"></a>Konfiguraatiot

Määritykset sisältävät ER-muodon määritykset, jotka tarvitaan muunnoksiin ja niiden tiedostojen luomiseen, jotka vaihdetaan tiedonsiirrossa kolmannen osapuolen verkkopalveluiden kanssa. Sähköisen laskutuksen lisäosatoiminnolla voi olla niin monta ER-tiedostomuotomääritystä kuin on tarpeen internetpalveluntarjoajan toimittamien integroinnin teknisten määritysten perusteella.

Voit lisätä ER-muotoja sähköisen laskutuksen lisäosatoimintoon noudattamalla seuraavia ohjeita.

1. Valitse **Sähköisen laskutuksen lisäosatoiminnot** -sivun **Määritykset** -välilehdessä **Lisää** lisätäksesi ER-tiedostomuotomäärityksiä sähköisen laskutuksen lisäosatoimintoa varten.

    ![Sähköisen laskutuksen lisäosatoiminnon määritysten lisääminen](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > Kun luot sähköisen laskutuksen lisäosatoiminnon alusta alkaen, sinun on lisättävä kaikki ER-tiedostomuotomääritykset manuaalisesti. Kun johdat sähköisen laskutuksen lisäosatoiminnon aiemmin luodusta toiminnosta, ER-tiedostomuotomääritykset luodaan automaattisesti, koska ne pohjautuvat alkuperäiseen sähköisen laskutuksen lisäosatoimintoon.

2. Valitse **Muokkaa** avataksesi **Muodon suunnittelija** -sivun, jolla voit muokata ER-tiedostomuotomääritystä.

    ![Sähköisen laskutuksen lisäosatoiminnon määritysten muokkaaminen](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > Kun muokkaat muotoa, määritysversion tilaksi määritetään **Luonnos**.

3. Käytä **Muodon suunnittelija** -sivua muuttaaksesi tiedostomuotomääritystä. Lisätietoja on kohdassa [Sähköisten asiakirjojen määritysten luominen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration)

    ![Muodon suunnittelutoiminto -sivu](media/e-Invoicing-services-feature-setup-ER-Format-designer.png)

### <a name="feature-setups"></a>Toimintojen määritykset

Toimintojen määritykset sisältävät kolmannen osapuolen verkkopalvelun kanssa käytävän viestinnän ja suojauksen säännöt. Sähköisen laskutuksen lisäosatoiminnolla voi olla niin monta toimintomääritystä kuin on tarpeen sen liiketoimintasäännön perusteella, jonka haluat toteuttaa.

Voit lisätä toimintomääritykset laskutuksen lisäosatoimintoon noudattamalla seuraavia ohjeita.

1. Valitse **Sähköisen laskutuksen lisäosatoiminnot** -sivun **Määritykset** -välilehdessä **Lisää** lisätäksesi toimintomäärityksiä sähköisen laskutuksen lisäosatoimintoa varten.

    ![Sähköisen laskutuksen lisäosatoiminnon määritysten lisääminen](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Setups.png)

    > [!NOTE]
    > Kun luot sähköisen laskutuksen lisäosatoiminnon alusta alkaen, sinun on lisättävä kaikki tarvittavat toimintomääritykset manuaalisesti. Kun johdat sähköisen laskutuksen lisäosatoiminnon aiemmin luodusta toiminnosta, kaikki toimintomääritykset luodaan automaattisesti, koska ne pohjautuvat alkuperäiseen sähköisen laskutuksen lisäosatoimintoon.

2. Muokkaa toimintoversiomääritystä valitsemalla **Muokkaa**.

    ![Sähköisen laskutuksen lisäosatoiminnon määritysten muokkaaminen](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Setups.png)

3. **Toimintoversion määritykset** -sivulla voit määrittää toimia, soveltuvuussääntöjä ja muuttujia.

    ![Toimet, soveltuvuussäännöt ja muuttujat](media/e-Invoicing-services-feature-setup-View-Actions-Applicability-Rules-Variables.png)

### <a name="actions"></a>Toimenpiteet

Toimet ovat ennalta määritetty luettelo toiminnoista, jotka suoritetaan peräkkäisessä järjestyksessä. Tämä luettelo sisältää yhteenvedon vaiheista, jotka tarvitaan sähköisen laskutuksen lisäosatoiminnon täyttä suorittamista varten. Toimiin voivat kuulua samassa sähköisen laskutuksen lisäosatoiminnossa viestintä molempiin suuntiin (kohdepyynnön lähettäminen) sekä vastauksen vastaanottaminen ja sen sisällön jäsentäminen.

Kukin toimi sisältää ennalta määritetyn luettelon parametreista, joita tarvitaan toimen tarkoituksen täyttämiseen. Lisäparametreja voidaan antaa valinnaisesti.

#### <a name="actions-fasttab"></a>Toimien pikavälilehti

Noudata toista sivun **Toimintoversioiden määritys** -sivun **Toimet** -välilehden **Toimet** -pikavälilehden ohjetta tai niitä molempia:

- Valitse **Uusi** tai **Poista** , jos haluat lisätä uusia toimia tai poistaa aiemmin luotuja toimia.
- Valitsemalla **Ylös** tai **Alas** voit siirtää valittuja toimia ylös- tai alaspäin ruudukossa ja siten muuttaa niiden suoritusjärjestystä. Toimet suoritetaan siinä järjestyksessä, jossa ne ovat ruudukossa alhaalta ylöspäin.

![Toimien hallinta](media/e-Invoicing-services-feature-setup-Manage-Actions.png)

Seuraavassa taulukossa käsitellään **Toimet** -pikavälilehdessä valittavina olevat kentät.

| Kenttä        | kuvaus |
|--------------|-------------|
| Toimenpide       | Esimääritettyjä toimia on kahdeksan.<ul><li><strong>Allekirjoita tiedosto</strong></li><li><strong>FileStoreActionName</strong></li><li><strong>Muunna asiakirja</strong></li><li><strong>Käsittele vastaus</strong></li><li><strong>Kutsu REST-verkkopalvelua</strong></li><li><strong>Kutsu Meksikon PAC-palvelua</strong></li><li><strong>Kutsu Brasilian SEFAZ-palvelua</strong></li><li><strong>Kutsu Italian SDI-palvelua</strong></li></ul> |
| Toiminnon nimi  | Toimen nimi ja suoritusjärjestys. |
| kuvaus  | Toimen kuvaus. |
| Ota uudelleenyritys käyttöön | Valittu valintaruutu ilmaisee, että toimea voidaan yrittää uudelleen, jos edellinen yritys epäonnistuu. |
| Yritä toimintoa uudelleen | Uuden yrityksen yhteydessä se toiminta, josta uusi yritys aloitetaan. Uusi yritys päättyy sitten nykyiseen toimeen (uudelleenyritys mukaan luettuna). Jos uudelleenyrityksiä sisältävillä toimilla on parametrit **Lopetuksen minimi** ja **Lopetuksen maksimi** , määritä uusien yritysten enimmäis- ja vähimmäismäärä. |

#### <a name="parameters-fasttab"></a>Parametrien pikavälilehti

**Parametrit** -pikavälilehdessä on luettelo sen toimen parametreista, joka on valittuna **Toimet** -pikavälilehdessä.

![Parametrien pikavälilehti](media/e-Invoicing-services-feature-setup-View-Actions-Parameters.png)

Seuraavassa taulukossa käsitellään **Parametrit** -pikavälilehdessä valittavina olevat kentät.

| Kenttä       | kuvaus |
|-------------|-------------|
| Nimi        | Esimääritetty parametriluettelo. Katso lisätietoja osasta [Toimikohtainen parametriluettelo](#list-of-parameters-by-action). |
| kuvaus | Parametrin kuvaus. |
| Arvo       | Parametrin arvo. |

#### <a name="list-of-parameters-by-action"></a>Toimikohtainen parametriluettelo

Käytettävissä olevat parametrit vaihtelevat **Toimet** -pikavälilehdessä valitun toimen mukaan.

###### <a name="action-sign-document"></a>Toimi: Allekirjoita tiedosto

| Parametri                             | kuvaus |
|---------------------------------------|-------------|
| Syötetiedosto                            | Tuleva XML-asiakirjatiedosto, joka on allekirjoitettava sähköisellä allekirjoituksella. |
| Sertifikaatin nimi                      | Tallennettuna olevan sertifikaatin nimi. |
| Allekirjoitustyyppi                        | Käytettävän allekirjoituksen tyyppi. |
| Allekirjoitusmenetelmän nimi                 | Sähköisen allekirjoituksen luomisessa käytettävän allekirjoitusmenetelmän nimi. |
| Tiivistysmenetelmän nimi                    | Tiivistemenetelmä, jota käytetään tiivistemerkkijonon luomiseen digitaalisessa allekirjoituksessa. |
| Kanonisointimenetelmän nimi          | Kanonisointimenetelmä, jota käytetään allekirjoitustiivisteen laskemiseen. |
| Viitemääritteen nimi              | Määritteen nimi, joka ilmaisee, minne viitetunnus pitäisi lisätä allekirjoituselementissä. |
| Allekirjoitettavan elementin nimi               | Asiakirjan sen XML-elementin nimi, joka on allekirjoitettava sähköisellä allekirjoituksella. Jos mitään elementtiä ei ole määritetty, allekirjoitetaan asiakirjan juuri. |
| Allekirjoitukseen lisättävän elementin nimi   | Sen XML-elementin nimi, johon luotu digitaalinen allekirjoitus pitäisi lisätä. Jos mitään elementtiä ei ole määritetty, allekirjoitus lisätään asiakirjan juureen. |
| XLST-tiedosto, joka sisältää tiivistemuunnoksen       | XSLT (Extensible Stylesheet Language Transformations) -tiedosto, joka sisältää tiivistemuunnoksen säännöt sähköisen allekirjoituksen tiivistemerkkijonon luomiselle. |
| Polku tiivistemerkkijonon lisäämistä varten          | Polku kohdassa **\<elementName\>.\<Attribute.Path\>** Sen sijainnin muoto, johon luotu tiivistemerkkijono on lisättävä. |
| Sertifikaattinumeron sijainti           | Sen elementin ja määritteen nimi, johon sertifikaattinumero sijoitetaan. |
| Sertifikaattitietojen sijainti          | Sen elementin ja määritteen nimi, johon sertifikaattitiedot (base64) on lisättävä. |
| Sertifikaattinumero on ASCII-muodossa | Arvo, joka määrittää, koodataanko sertifikaatin numero ASCII-muodossa. |

###### <a name="action-filestoreactionname"></a>Toimi: FileStoreActionName

| Parametri  | kuvaus |
|------------|-------------|
| Syötetiedosto | Syötetiedosto, joka tallennetaan. |

###### <a name="action-transform-document"></a>Toimi: Muunna tiedosto

| Parametri                       | kuvaus |
|---------------------------------|-------------|
| Syötetiedosto                      | Lähdetiedosto, joka sisältää tiedostot, jotka on suoritettava toimessa. |
| Siirtosuunta                       | Arvo, joka ilmaisee, käytetäänkö tuontimuotoa vai vientimuotoa. |
| Konfiguraation tunnus                | Suoritettava muoto. |
| Määritysten versio           | Jos määritysversio on määritetty, käytetään viimeisintä versiota. |
| Määrityksen integrointikohta | Lähdetiedosto, joka sisältää tiedot raportoinnin suorituspalvelua varten. |

###### <a name="action-process-response"></a>Toiminto: Käsittele vastaus

| Parametri                    | kuvaus |
|------------------------------|-------------|
| Syötetiedosto                   | Analysoitava vastaus. |
| Raportointikonfiguraatioluettelo | Määritysluettelo, jota käytetään vastausten jäsentämiseen. |

###### <a name="action-call-rest-web-service"></a>Soitmi: Kutsu REST-verkkopalvelua

| Parametri                   | kuvaus |
|-----------------------------|-------------|
| Internet-palvelun URL             | URL-osoite, johon pyynnöt lähetetään. |
| Verkkopyynnön aikakatkaisu         | Enimmäisaika (millisekunteina), joka odotetaan verkkopalvelun vastausta. |
| Pyyntötoiminnon tyyppi      | HTTP-pyyntötoiminnon tyyppi (kuten **HAE** , **KIRJAA** tai **POISTA** ). |
| Sertifikaattien nimet           | Sertifikaattien nimet. |
| Vastaustekstin koodaus      | HTTP-vastaustekstin odotettu koodaus, jotta sen koodaus voidaan purkaa oikein. |
| HTTP-pyynnön sisältötyyppi   | HTTP-pyynnön sisältötyypin otsikkosyöte. |
| HTTP-pyynnön sisältöteksti   | HTTP-pyynnön teksti. (Teksti voi olla tyhjä.) |
| HTTP-parametrikyselyn arvot | Parametrikyselyn arvoit, joita käytetään URL-osoitteen täyttämiseen muuttuvilla parametreilla. |
| Pyydä reititys               | HTTP-pyynnön reitityspolku. Muuttuvat parametrit voi kirjoittaa **\{paramName\}** -merkintään. Esimerkki: **"api/{id}/submit"**. |
| Reititysparametriluettelo        | Muuttujien reititykseen lisäämiseen käytettävät reititysparametrit avainarvomerkintänä. |
| Mukautetut HTTP-otsikot         | Mukautetut HTTP-otsikot, jotka lisätään pyyntöön. |
| HTTP-pyynnön evästeet        | Luettelo avainarvomerkinnän muotoisista evästeitä, jotka lisätään HTTP-evästeiden otsikkopyyntöön. |
| Suojausprotokolla           | Suojausprotokolla, jota käytetään HTTP-pyynnöissä palvelimen kanssa viestimiseen. (Oletusarvoisesti käytetään suojausprotokollaa Transport Layer Security \[TLS\] 1.2.) |

###### <a name="action-call-mexican-pac-service"></a>Soitmi: Kutsu Meksikon PAC-palvelua

| Parametri                | kuvaus |
|--------------------------|-------------|
| Syötetiedosto               | Tiedosto, joka sisältää XML-tietoja, jotka lähetetään verkkopalvelulle menetelmäsyöteparametrina. |
| URL-osoite              | Verkkopalvelun osoite (päätepiste). |
| Verkkomenetelmän (toimi) nimi | Suoritettavan verkkomenetelmän (toimen) nimi. |
| Todistukset             | Varmenneketju, jota vaaditaan verkkopalvelun asiakasohjelman todentamiseen. Asiakasvarmenteen pitäisi olla ketjun viimeinen varmenne. Juuri- ja välivarmenteiden pitäisi tulla ensin. |
| Verkkopyynnön aikakatkaisu      | Enimmäisaika (millisekunteina), joka odotetaan verkkopalvelun vastausta. |
| Uudelleenyritysten aikaväli           | Verkkopalvelun kutsumisen ja vastauksen saamisen yritysten välinen aika. Jos aik väliä ei määritetä, muita uudelleenyrityksiä ei tehdä, kun ensimmäinen kutsu epäonnistuu. |
| Uudelleenyrityslaskuri              | Enimmäismäärä uudelleenyrityksiä verkkopalvelun kutsumiselle ja siltä vastauksen saamiselle. |
| Yritä uudelleen aikaan               | Enimmäisaika (millisekunteina), jonka kutsujen uudelleenyritykset voivat jatkua. |
| Lopetuksen minimi         | Pienin lopetusarvo uusien yritysten aikavälien eksponentiaaliselle laskennalle. |
| Lopetuksen maksimi         | Suurin lopetusarvo uusien yritysten aikavälien eksponentiaaliselle laskennalle. |
| Suojausprotokolla        | Suojausprotokolla, jota käytetään HTTP-pyynnöissä palvelimen kanssa viestimiseen. (Oletusarvoisesti käytetään suojausta TLS 1.2.) |

###### <a name="action-call-brazilian-sefaz-service"></a>Toimi: Kutsu Brasilian SEFAZ-palvelua

| Parametri                | kuvaus |
|--------------------------|-------------|
| Syötetiedosto               | Tiedosto, joka sisältää XML-tietoja, jotka lähetetään verkkopalvelulle menetelmäsyöteparametrina. |
| URL-osoite              | Verkkopalvelun osoite (päätepiste). |
| Verkkomenetelmän (toimi) nimi | Suoritettavan verkkomenetelmän (toimen) nimi. |
| Todistukset             | Varmenneketju, jota vaaditaan verkkopalvelun asiakasohjelman todentamiseen. Asiakasvarmenteen pitäisi olla ketjun viimeinen varmenne. Juuri- ja välivarmenteiden pitäisi tulla ensin. |
| Verkkopyynnön aikakatkaisu      | Enimmäisaika (millisekunteina), joka odotetaan verkkopalvelun vastausta. |
| Uudelleenyritysten aikaväli           | Verkkopalvelun kutsumisen ja vastauksen saamisen yritysten välinen aika. Jos aik väliä ei määritetä, muita uudelleenyrityksiä ei tehdä, kun ensimmäinen kutsu epäonnistuu. |
| Uudelleenyrityslaskuri              | Enimmäismäärä uudelleenyrityksiä verkkopalvelun kutsumiselle ja siltä vastauksen saamiselle. |
| Yritä uudelleen aikaan               | Enimmäisaika (millisekunteina), jonka kutsujen uudelleenyritykset voivat jatkua. |
| Lopetuksen minimi         | Pienin lopetusarvo uusien yritysten aikavälien eksponentiaaliselle laskennalle. |
| Lopetuksen maksimi         | Suurin lopetusarvo uusien yritysten aikavälien eksponentiaaliselle laskennalle. |
| Suojausprotokolla        | Suojausprotokolla, jota käytetään HTTP-pyynnöissä palvelimen kanssa viestimiseen. (Oletusarvoisesti käytetään suojausta TLS 1.2.) |

###### <a name="action-call-italian-sdi-service"></a>Toimi: Kutsu Italian SDI-palvelua

| Parametri                | kuvaus |
|--------------------------|-------------|
| Syötetiedosto               | Tiedosto, joka sisältää XML-tietoja, jotka lähetetään verkkopalvelulle menetelmäsyöteparametrina. |
| URL-osoite              | Verkkopalvelun osoite (päätepiste). |
| Verkkomenetelmän (toimi) nimi | Suoritettavan verkkomenetelmän (toimen) nimi. |
| Todistukset             | Varmenneketju, jota vaaditaan verkkopalvelun asiakasohjelman todentamiseen. Asiakasvarmenteen pitäisi olla ketjun viimeinen varmenne. Juuri- ja välivarmenteiden pitäisi tulla ensin. |
| Verkkopyynnön aikakatkaisu      | Enimmäisaika (millisekunteina), joka odotetaan verkkopalvelun vastausta. |
| Uudelleenyritysten aikaväli           | Verkkopalvelun kutsumisen ja vastauksen saamisen yritysten välinen aika. Jos aik väliä ei määritetä, muita uudelleenyrityksiä ei tehdä, kun ensimmäinen kutsu epäonnistuu. |
| Uudelleenyrityslaskuri              | Enimmäismäärä uudelleenyrityksiä verkkopalvelun kutsumiselle ja siltä vastauksen saamiselle. |
| Yritä uudelleen aikaan               | Enimmäisaika (millisekunteina), jonka kutsujen uudelleenyritykset voivat jatkua. |
| Lopetuksen minimi         | Pienin lopetusarvo uusien yritysten aikavälien eksponentiaaliselle laskennalle. |
| Lopetuksen maksimi         | Suurin lopetusarvo uusien yritysten aikavälien eksponentiaaliselle laskennalle. |
| Suojausprotokolla        | Suojausprotokolla, jota käytetään HTTP-pyynnöissä palvelimen kanssa viestimiseen. (Oletusarvoisesti käytetään suojausta TLS 1.2.) |

### <a name="applicability-rules"></a>Soveltuvuussäännöt

Soveltuvuussääntöjen avulla voit luoda loogisia sääntöjä, jotka määräävät toimintomäärityksen käyttökontekstin. Näin ollen käsittelyyn lähetetyn liiketoimintatiedoston kontekstin yhteensovituksen ja soveltuvuussäännön ehtojen mukaan määräytyy, mitä sähköisen laskutuksen lisäosatoimintoa käytetään kyseisen lähetyksen käsittelemiseen.

#### <a name="set-up-applicability-rules"></a>Soveltuvuussääntöjen määrittäminen

1. Valitse **Toimintoversion määritys** -sivun **Soveltuvuussäännöt** -välilehdessä **Uusi** lisätäksesi soveltuvuussäännön.

    ![Soveltuvuussääntöjen hallinta](media/e-Invoicing-services-feature-setup-Manage-Actions-Applicability-rules.png)

2. Valitse ruudukosta lausekkeet, jotka ryhmitellään.
3. Valitse **Ryhmittele lauseke**.

    ![Lausekkeiden ryhmittely](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-clause.png)

    Kun lausekkeita ryhmitellään, ruudukkoon lisästään uusi sarake. Tämä sarake määrittää ryhmiteltyjen lausekkeiden loogisen operaattorin.

    ![Ryhmiteltyjen lausekkeiden looginen operaattori](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-criterias.png)

Voit purkaa lausekkeiden ryhmittelyn valitsemalla halutut lausekkeet ja valitsemalla sitten **Poista lausekkeen ryhmittely**.

![Lausekkeiden ryhmittelyn poisto](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-UnGroup-criterias.png)

> [!NOTE]
> Kun purat lausekkeen ryhmittelyn, aloita aina sisimmästä ryhmittelytasosta.

Seuraavassa taulukossa käsitellään **Soveltuvuussäännöt** -välilehdessä valittavina olevat kentät.

| Kenttä         | kuvaus |
|---------------|-------------|
| Ja/tai        | Looginen operaattori. |
| Kenttä         | Kenttä, jota käytetään säännön rakentamiseen. |
| Operaattorin tyyppi | Operaattorin tyyppi.<ul><li>Yhtä suuri</li><li>Ei sama kuin</li><li>Suurempi kuin / pienempi kuin</li><li>suurempi tai yhtä suuri kuin / pienempi tai yhtä suuri kuin</li><li>Sisältää</li><li>Aloitus</li></ul> |
| Arvo         | Säännön kriteeri. |

### <a name="variables"></a>Muuttujat

Voit luoda muuttujia ja käyttää niitä tietyn toimen parametrin syötearvona. Niiden avulla voi myös vaihtaa sähköisen laskutuksen lisäosapalvelujen ja asiakasohjelman välillä tietoja, jotka ovat tulosta tietyn toimen suorittamisesta osana lähetysten työnkulkua.

#### <a name="set-up-variables"></a>Määritä muuttujat

- Voit hallita muuttujia valitsemalla **Toimintoversion määritys** -sivun **Muuttujat** -välilehdessä **Uusi** tai **Poista**.

    ![Muuttujien hallinta](media/e-Invoicing-services-feature-setup-Manage-Variables.png)

Seuraavassa taulukossa käsitellään **Muuttujat** -välilehdessä valittavina olevat kentät.

| Kenttä       | kuvaus |
|-------------|-------------|
| Nimi        | Muuttujan nimi. |
| kuvaus | Muuttujan lyhyt kuvaus. |
| Laji        | Muuttujan tyyppi:<ul><li><strong>Vakio</strong> – Muuttujan sisältö on kiinteä.</li><li><strong>Asiakkaalta</strong> – Muuttujan sisältö hankitaan Microsoft Dynamics 365 -asiakkaalta lähetysprosessin suorittamisen aikana.</li><li><strong>Asiakkaalle</strong> – Microsoft Dynamics 365 -asiakas antaa muuttujan sisällön käyttöön lähetysprosessin suorittamisen aikana.</li></ul> |
| Tietotyyppi   | Muuttujan tietolaji:<ul><li>Boolen arvo</li><li>Päivämäärä</li><li>Numero</li><li>UUID</li><li>Merkkijono</li><li>Tiedosto</li></ul> |
| Arvo       | Muuttujan arvo tai sen toimen nimi, joka määrittää muuttujan arvon. |

### <a name="validate-the-feature-setup"></a>Toimintomäärityksen vahvistaminen

- Voit vahvistaa version määrityksen valitsemalla **Toimintoversion määritys** -sivun toimintoruudussa **Vahvista**.

   ![Vahvistuspainikkeen valitseminen](media/e-Invoicing-services-feature-setup-Select-Validate-Button.png)

Vahvistus tarkistaa koko määrityksen yhdenmukaisuuden. Jos esimerkiksi toimen tietty parametri on pakollinen, mutta sen arvo pysyy tyhjänä, vahvistus havaitsee tämän ristiriidan ja näyttöön tulee varoitus.

## <a name="environments"></a>Ympäristöt

Sähköisen laskutuksen lisäosaympäristö on liitettävä sähköisen laskutuksen lisäosatoimintoon ja otettava käyttöön. Sähköisen laskutuksen lisäosaympäristöt on luotava ja julkaistava etukäteen määrittämällä globalisointitoimintoja organisaation RCS-tilissä.

Näiden ohjeiden avulla voit ottaa käyttöön sähköisen laskutuksen lisäosaympäristön sähköisen laskutuksen lisäosatoimintoa varten.

1. Valitse **Sähköisen laskutuksen lisäosatoiminnot** -sivun **Ympäristöt** -välilehdessä **Ota käyttöön** lisätäksesi sähköisen laskutuksen lisäosaympäristön.
2. Syötä **Voimaantulo** -kenttään päivämäärä, jona uusi ympäristö otetaan käyttöön.

![Sähköisen laskutuksen lisäosaympäristön käyttöönotto](media/e-Invoicing-services-feature-setup-Select-Enable-e-Invoicing-feature-Environment.png)

## <a name="organizations"></a>Organisaatiot

Sähköinen lisäosatoiminto voidaan jakaa useille organisaatioille.

- Valitse **Sähköisen laskutuksen lisäosatoiminnot** -sivun **Organisaatiot** -välilehdellä **Jaa seuraavan kanssa** lisätäksesi organisaation, jolle haluat jakaa sähköisen laskutuksen lisäosatoiminnon.

Voit lopettaa sähköisen laskutuksen lisäosatoiminnon jakamisen organisaatiolle valitsemalla **Lopeta jakaminen**.

## <a name="versions"></a>Versiot

Versiot auttavat sähköisen laskutuksen lisäosatoiminnon elinkaaren hallinnassa siten, että ne hallitsevat sen tilaa. Voit luoda uuden version aiemmin luodusta sähköisen laskutuksen lisäosatoiminnosta tai, kun kaikki sähköisen laskutuksen lisäosatoiminnon määritykset on suoritettu, voit muuttaa toiminnon tilaksi **Valmis** ja sitten **Julkaise**.

### <a name="create-a-new-version-of-an-existing-electronic-invoicing-add-on-feature"></a>Luo uusi versio olemassa olevasta sähköisen laskutuksen lisäosatoiminnosta

1. Valitse **Sähköisen laskutuksen lisäosatoiminnot** -sivun vasemmassa ruudukossa Sähköisen laskutuksen lisäosatoiminto.
2. Valitse **Versiot** -välilehdessä **Uusi** lisätäksesi uuden version sähköisen laskutuksen lisäosatoiminnosta.

### <a name="change-the-status-of-the-electronic-invoicing-add-on-feature"></a>Sähköisen laskutuksen lisäosatoiminnon tilan muuttaminen

Voit hallita laskutuksen lisäosatoimintoa noudattamalla seuraavia ohjeita.

1. Valitse **Sähköisen laskutuksen lisäosatoiminnot** -sivun vasemmassa ruudukossa Sähköisen laskutuksen lisäosatoiminto.
2. Valitse **Versiot** -välilehdessä **Muuta tilaa** ja muuta tilan **Luonnos** tilalle tila **Valmis**.
3. Järjestelmä pyytää vahvistamaan, että haluat viimeistellä sähköisen laskutuksen lisäosatoiminnon ja kaikki sen komponentit. Vahvista toimi valitsemalla **Kyllä** tai peru se valitsemalla **Ei**.

    > [!NOTE]
    > Kun valitset **Kyllä** , sähköisen laskutuksen lisäosatoiminnon komponentteja olevien määritysversioiden tila muuttuu automaattisesti arvosta **Luonnos** arvoksi **Valmis**.

4. Valitse **Muuta tilaa** ja muuta tila sitten tilasta **Valmis** tilaan **Julkaise**.
5. Järjestelmä pyytää vahvistamaan, että haluat julkaista sähköisen laskutuksen lisäosatoiminnon ja kaikki sen komponentit yleiseen säilöön. Vahvista toimi valitsemalla **Kyllä** tai peru se valitsemalla **Ei**.

    > [!NOTE]
    > Kun valitset **Kyllä** , määritysversioiden tila muutetaan automaattisesti tilasta **Valmis** tilaan **Jaettu**.
