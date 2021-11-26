---
title: Varmuusvaraston kirjauskansion käyttäminen tuotteiden vähimmäiskattavuuden päivittämiseen
description: Tässä aiheessa käsitellään varmuusvaraston kirjauskansion käyttämistä nimikkeiden varmuusvaraston määrän päivittämiseen. Se tehdään laskemalla historiallisiin tapahtumiin perustuvat vähimmäiskattavuusehdotukset.
author: ChristianRytt
ms.date: 10/28/2021
ms.topic: article
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, ReqItemTableSetup, ReqItemTable, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-10-28
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 59e4959898cd961582e1ac1d2285c0c0867ee7af
ms.sourcegitcommit: bc9e75c38e192664cde226ed3a94df5a0b304369
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/10/2021
ms.locfileid: "7790969"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage-for-items"></a>Varmuusvaraston kirjauskansion käyttäminen tuotteiden vähimmäiskattavuuden päivittämiseen

[!include [banner](../../includes/banner.md)]

Varmuusvarasto ilmaisee, kuinka paljon ylimääräisiä nimikkeitä on varastossa, jotta nimikkeen loppuminen varastosta voidaan estää. Varmuusvarastoa käytetään puskurivarastona siltä varalta, että toimittaja ei voi toimittaa koko myyntitilausta vastaavaa määrää pyydettyyn lähetyspäivämäärään mennessä.

Tässä aiheessa käsitellään varmuusvaraston kirjauskansion käyttämistä vähimmäiskattavuuden ehdotusten laskemista historiallisen tapahtumien perusteella ja päivittämistä nimikekattavuuden ehdotusten mukaiseksi.

## <a name="overview-of-minimum-coverage-usage"></a>Vähimmäiskattavuuden käytön yleiskuvaus

Varmuusvarasto määritetään kunkin nimikkeen **Nimikkeen kattavuus** -sivulla. Erilaiset täydennystyypit ilmaistaan erilaisilla kattavuuskoodeilla. (Lisätietoja on kohdassa [Nimikkeiden varmuusvaraston täyttäminen](safety-stock-replenishment.md).) Kaikki kattavuuskoodit käyttävät kuitenkin arvoa, joka on määritetty kunkin nimikkeen **Nimikkeen kattavuus** -sivun **Minimi**-kentässä. **Minimi**-kenttää voi käyttää kahdella tavalla:

- **Minimimäärän käyttö minimin ja maksimin yhteydessä** – Tässä tapauksessa minimimäärää käytetään yhdessä minimi- ja maksimilogiikan kanssa. Sitä käytetään, kun soveltuvan nimikkeen tai kattavuusryhmän **Kattavuuskoodi**-kentän asetuksena on *Min./Maks.* **Minimi**-määrä ilmaisee keskimääräisen päivittäisen käytön kerrottuna nimikkeen läpimenoajalla.
- **Varastosuunnitelman minimimäärä** – Tässä tapauksessa minimimäärää käytetään ilmaisemaan varastosuunnitelma yhdessä kysyntäennusteiden kanssa. Sitä käytetään, kun soveltuvan nimikkeen tai kattavuusryhmän **Kattavuuskoodi**-kentän asetuksena *Kausi* tai *Tarve*. **Minimi**-määrä ilmaisee varastosuunnitelman, joka vastaa toivottua asiakaspalvelutasoa. Tämä auttaa vähentämään varaston loppumisia, osittaisia toimituksia ja toimituksen läpimenoaikoja. Vähimmäismäärä ilmaisee tietyn nimikkeen ennustetarkkuusprosentin. Se ei ilmaise toivottua varastopositiota.

**Minimi**-arvo voidaan määrittää kolmella tavalla:

- manuaalisesti **Nimikkeen kattavuus** -sivulla
- tiedonhallintakeskuksen avulla (*Nimikkeen kattavuus* -tietoyksiköt)
- varmuusvaraston kirjauskansioita käyttämällä tehdyn varmuusvarastolaskelman avulla.

## <a name="calculate-minimum-coverage-based-on-historical-usage"></a>Vähimmäiskattavuuden laskeminen historiallisen käytön perusteella

Varmuusvaraston kirjauskansioita käytetään laskemaan ehdotettu vähimmäismäärä nimikkeen historiallisen käytön perusteella joko minimi- tai maksimikäyttöä tai varastosuunnitelmakäyttöä varten. Historiallinen käyttö ilmaisee kaikki varasto-ottotapahtumat määritettynä ajanjaksona. Nämä varasto-ottotapahtumat sisältävät myyntitilaustapahtumat ja varastonmuutokset. Laskelmat määrittävät myös ehdotetun minimimäärän vaikutuksen varastoarvoon ja varastoarvon muutoksen nykyisiin minimimääriin verrattuna.

Kukin varmuusvaraston kirjauskansion rivi ilmaisee nimikkeen ja sen kattavuusdimensiot. Nämä kirjauskansion rivit luodaan ja näytetään **Varmuusvaraston kirjauskansion rivit** -sivulla (**Pääsuunnittelu \> Pääsuunnittelu \> Suorita \> Varmuusvaraston laskenta**). Liiketoimintaprosessia, jolla ehdotetut vähimmäismäärät lasketaan varmuusvaraston kirjauskansioiden avulla, käsitellä jäljempänä tässä aiheessa.

Suunnittelija laskee varmuusvaraston kirjauskansion avulla valittujen nimikkeiden ehdotetut vähimmäismäärät sen perusteella, mikä oli historiallinen käyttö valittuina ajanjaksoina. Ehdotetut minimit voidaan ohittaa tarvittaessa manuaalisesti, ja ehdotettujen minimien mahdollista vaikutusta varastoarvoon voidaan tarkastella. Kun kirjauskansio kirjataan, liittyvät vähimmäismäärät päivitetään automaattisesti nimikkeen kattavuudessa.

### <a name="create-a-new-safety-stock-journal-name"></a>Uuden varmuusvaraston kirjauskansion nimen luominen

Tällaisen kirjauskansion luominen edellyttää ainakin yhden varmuusvaraston kirjauskansion nimen luontia. Usein käytetään useita kirjauskansion nimiä, sillä näin varmuusvarastolaskelmat voivat erotella.

1. Valitse **Pääsuunnittelu \> Määritys \> Varmuusvaraston kirjauskansion nimet**.
1. Valitse toimintoruudussa **Uusi**.
1. Määritä seuraavat kentät uudella rivillä:

    - **Nimi** – anna kirjauskansiolle lyhyt nimi.
    - **Kuvaus** – anna kirjauskansion kuvaus.
    - **Vain käyttäjäryhmän käytössä** – valitse käyttäjäryhmä, jos haluat rajoittaa nykyisen kirjauskansion nimen kohderyhmää.
    - **Poista rivit kirjauksen jälkeen** – Valitse tämä valintaruutu, jos haluat tyhjentää kirjauskansion rivit oletusarvoisesti kirjauksen jälkeen. Poista valinta, jos haluat säilyttää kaikki kirjatut rivit.

    **Kirjauskansion tyyppi** -kenttä on vain luku -muotoinen, ja sen asetukseksi on valittu valmiiksi *Varmuusvarasto*.

1. Sulje sivu.

### <a name="create-a-safety-stock-journal-and-lines"></a>Varmuusvaraston kirjauskansion ja rivien luominen

Tässä vaiheessa luodaan kirjauskansio ja lisätään siihen automaattisesti rivejä. Kukin rivi määrittää nimikkeen, sen kattavuusdimensiot ja useita laskettuja määritä käyttöhistoriasta. Lasketut määrät sisältävät keskimääräiset varasto-otot nimikkeen läpimenoaikakohtaisesti, kuukausikohtaiset keskimääräiset varasto-otot ja kuukausittainen keskihajonta.

#### <a name="automatically-generate-journal-lines"></a>Kirjauskansion rivien automaattinen luominen

Kirjauskansion rivit voidaan luoda automaattisesti vain, jos näkyvissä olevassa kirjauskansiossa ei ole rivejä.

Kirjauskansion rivit luodaan automaattisesti seuraavasti:

1. Valitse **Pääsuunnittelu \> Pääsuunnittelu \> Suorita \> Varmuusvaraston laskenta**.
1. Valitse toimintoruudussa **Uusi**. Uusi varmuusvaraston kirjauskansio luodaan.
1. Määritä seuraavat kentät **Kirjauskansion otsikkotiedot** -pikavälilehdessä:

    - **Nimi** – valitse, mihin varmuusvaraston kirjauskansioon rivi lisätään.
    - **Kuvaus** – Oletusarvo on valitun kirjauskansion nimen kuvaus. Arvoa voi kuitenkin muokata tarvittaessa.
    - **Poista rivit kirjauksen jälkeen** – Valitse tämä valintaruutu, jos haluat tyhjentää kirjauskansion rivit kirjauksen jälkeen. Poista valinta, jos haluat säilyttää kaikki kirjatut rivit. Tämä asetus peritään valitun kirjauskansion nimestä.

    **Kirjauskansio**-kenttä on vain luku -muotoinen, ja siinä näkyy sen kirjauskansion tunnusnumero, jota ollaan luomassa ja johon rivejä lisätään.

1. Valitse **Kirjauskansion rivit**-pikavälilehden työkalurivillä **Luo rivit**.
1. Määritä **Luo kirjauskansion rivit suunnitelluille varaston vähimmäistasoille** -valintaikkunassa seuraavat kentät:

    - **Päivämäärästä** – valitse sen ajanjakson alkamispäivä, jonka aikaiset varasto-otot on sisällytettävä laskelmaan.
    - **Päivämäärään** – Valitse sen ajanjakson päättymispäivä, jonka aikaiset varasto-otot on sisällytettävä laskelmaan. Alkamis- ja päättymispäivien välissä on oltava vähintään kaksi kuukautta.
    - **Laske vakiopoikkeama** – Laske keskihajonta valitsemalla tässä asetukseksi *Kyllä*. Asetuksena on oltava *Kyllä*, jos **Käytä palvelutasoa** -vaihtoehtoa halutaan käyttää ehdotusta laskettaessa. (Lisätietoja on jäljempänä tässä aiheessa.)

1. **Sisällytettävät tietueet** -pikavälilehdessä voidaan määrittää suodattimet ja rajoitteet, joiden avulla määritetään raporttiin sisällytettävät nimikkeet. (Suodatusperusteena voi olla esimerkiksi **Kattavuusryhmä** -arvo.) Avaa vakiokyselyeditorin valintaikkuna valitsemalla **Suodatus**. Tässä ikkunassa voidaan määrittää valinta- ja lajitteluehdot sekä liitokset. Kentät toimivat samalla tavalla kuin muissakin Microsoft Dynamics 365 Supply Chain Managementin kyselyissä.
1. Valitse **Suorita taustalla** -pikavälilehdessä, suoritetaanko työ erätilassa, ja/tai määritä toistuva aikataulu. Kentät toimivat samalla tavalla kuin muissakin [taustatöissä](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Supply Chain Managementissa.
1. Valitse **OK**. Rivit luodaan dimensioille, joissa on varastotapahtumia.

#### <a name="manually-add-or-remove-journal-lines"></a>Kirjauskansion rivien lisääminen tai poistaminen manuaalisesti

Kirjauskansion rivejä voi lisätä ja/tai poistaa manuaalisesti koska tahansa (joko rivien automaattisen luonnin jälkeen tai sen sijasta). Käytössä on seuraavat **Kirjauskansion rivit** -pikavälilehden työkalurivin painikkeet:

- **Uusi** – Lisää uusi rivi. Anna sitten kussakin sarakkeessa. Tällä tavoin määritetään tuote, jolle uudet minimit lasketaan ja jossa niitä käytetään. Koska ehdotetut minimilaskelmat eivät ole käytettävissä manuaalisesti lisätyissä riveissä, niille ei näytetä uusia **Laskettu vähimmäismäärä** -arvoja. Tämän vuoksi **Uusi vähimmäismäärä** -arvot on annettava manuaalisesti. **Uusi vähimmäismäärä** -arvon mahdollista vaikutusta varastoarvoon ja mahdollista muutosta varastossa nykyiseen määritettyyn minimiin verrattuna voidaan silti tarkastella.
- **Poista** – poista valittu rivi.
- **Poista kirjauskansion rivit** – poista kaikki kirjauskansion rivit.

### <a name="calculate-a-proposal"></a>Ehdotuksen laskeminen

Tässä vaiheessa lasketaan ehdotettu minimi kullekin kirjauskansion riville ja rivin mahdollinen vaikutus varastoarvoon. (Ehdotettu minimi näytetään **Laskettu vähimmäismäärä** -arvona.) Laskelma voidaan tehdä tarvittaessa useita kertoja. Laskelma päivittää kaikille kirjauskansion riveille näytettävän **Laskettu vähimmäismäärä** -arvon.

Näytettävät laskelmat eivät vaikuta kunkin tuotteiden todellisen vähimmäismäärän arvoihin ennen **Kirjaa**-asetuksen valintaa toimintoruudussa. Siinä vaiheessa **Uusi vähimmäismäärä** -arvoja käytetään kussakin tuotteessa.

1. Valitse **Pääsuunnittelu \> Pääsuunnittelu \> Suorita \> Varmuusvaraston laskenta**.
1. Avaa kirjauskansio, jolle ehdotus lasketaan. Vaihtoehtoisesti voit luoda uuden kirjauskansion aiemmin tässä aiheessa kuvatulla tavalla.
1. Valitse **Kirjauskansion rivit**-pikavälilehden työkalurivillä **Laske ehdotus**. (Rivejä ei tarvitse valita.)
1. Määritä **Laske ehdotus varaston vähimmäistasolle** -valintaikkunassa seuraavat kentät:

    - **Käytä keskimääräistä varasto-ottoa läpimenoaikana** – Valitse tämä asetus, kun **Laskettu vähimmäismäärä** -arvot luodaan määritetyn ajankohdan keskimääräisten varasto-ottojen perusteella. Muokkaa sitten tulosta tarvittaessa antamalla arvo **Kerroin**-kentässä. Anna esimerkiksi *1.0*, jos halutaan käyttää tarkkaa laskettua keskiarvoa, tai *1,1*, jos halutaan lisätä 10 prosentin lisäpuskuri.
    - **Käytä palvelutasoa** – Valitse tämä asetus ehdotetun minimin laskemiseen toivotun palvelutason perusteella. Valitse sitten ensisijainen palvelutaso **Palvelutaso**-kentässä.
    - **Läpimenoajan marginaali** – Anna arvo, jolla normaalia läpimenoaikaa pidennetään. (Näin voidaan varata aikaa esimerkiksi hallinnollisia toimia varten.)
    - **Käytä laskettua minimimäärää uutena minimimääränä** – Määritä asetukseksi *Kyllä*, jolloin **Laskettu vähimmäismäärä** -sarakkeen arvot kopioidaan automaattisesti kaikkien rivien **Uusi vähimmäismäärä** -sarakkeisiin, kun laskenta on suoritettu: Jos asetukseksi määritetään *Ei*, **Nykyinen vähimmäismäärä** -arvo kopioidaan kaikkien rivien **Uusi vähimmäismäärä** -sarakkeeseen. **Uusi vähimmäismäärä** -arvoja on sitten muokattava tarvittaessa manuaalisesti.

1. Valitse **Suorita taustalla** -pikavälilehdessä, suoritetaanko työ erätilassa, ja/tai määritä toistuva aikataulu. Kentät toimivat samalla tavalla kuin muissakin [taustatöissä](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Supply Chain Managementissa.
1. Valitse **OK**. Laskelman tulokset näkyvät **Kirjauskansion rivit** -pikavälilehden **Laskettu vähimmäismäärä** -sarakkeessa. Arvot ovat vielä vain ehdotettuja arvoja, joita ei ole käytetty tuotteissa.

### <a name="update-minimum-quantity"></a>Päivitä vähimmäismäärä

Mikä tahansa varmuusvaraston kirjauskansion rivi voidaan valita ja sen **Uusi vähimmäismäärä** -kentän arvo voidaan ohittaa manuaalisesti.

1. Valitse **Pääsuunnittelu \> Pääsuunnittelu \> Suorita \> Varmuusvaraston laskenta**.
1. Avaa muokattava kirjauskansio. Vaihtoehtoisesti voit luoda uuden kirjauskansion aiemmin kuvatulla tavalla.
1. Etsi **Kirjauskansion rivit** -pikavälilehdessä muutettava rivi ja muokkaa sitten **Uusi vähimmäismäärä** -sarakkeen arvoa. **Uusi vähimmäismäärä** -arvo voidaan esimerkiksi määrittää siten, että se vastaa **Laskettu vähimmäismäärä** -arvoa. Jos **Laskettu vähimmäismäärä** on *0* (nolla), voit antaa sopivan tulevan arvon.

### <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>Kirjaa uusi vähimmäismäärä ja vahvista tulos

Uusi vähimmäismäärä kirjataan ja tulos vahvistetaan seuraavasti:

1. Valitse **Pääsuunnittelu \> Pääsuunnittelu \> Suorita \> Varmuusvaraston laskenta**.
1. Avaa kirjauskansio, johon uudet vähimmäismäärät kirjataan. Vaihtoehtoisesti voit luoda uuden kirjauskansion aiemmin kuvatulla tavalla.
1. Valitse toimintoruudussa **Kirjaa**.
1. Määritä **Kirjaa kirjauskansio** -valintaikkunassa **Siirrä kaikki kirjausvirheet uuteen kirjauskansioon** tarvittaessa. Kirjaa kirjauskansio valitsemalla **OK**.
1. Jos rivin **Uusi vähimmäismäärä** -arvo muutettiin **Kirjauskansion rivit** -pikavälilehdessä, muutos voidaan vahvistaa seuraavasti:

    1. Valitse muokatun rivin osalta linkki **Nimiketunnus**-sarakkeessa.
    1. Avaa liittyvän vapautetun tuotteen tietue valitsemalla **Tuotteen tiedot** -valintaikkunassa linkki **Nimiketunnus**-kentässä.
    1. Valitse toimintoruudun **Suunnitelma**-välilehden **Kattavuus**-ryhmässä **Nimikkeen kattavuus**.
    1. Huomaa, että sen toimipaikan ja varaston **Minimi**-arvo, jota muutettiin kirjatun varmuusvaraston kirjauskansion avulla, on nyt päivitetty vastaamaan muokkausta.

## <a name="additional-resources"></a>Lisäresurssit

- [Nimikkeiden varmuusvaraston täyttäminen](safety-stock-replenishment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
