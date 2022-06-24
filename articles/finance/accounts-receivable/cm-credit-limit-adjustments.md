---
title: Luottorajan oikaisut
description: Tässä artikkelissa käsitellään luottorajan oikaisujen määrittämistä ja lisäämistä.
author: JodiChristiansen
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fa4721be1e213afbaaeaa475be2697c8e55426a3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891722"
---
# <a name="credit-limit-adjustments"></a>Luottorajan oikaisut 

[!include [banner](../includes/banner.md)]

Luottorajaoikaisujen avulla luottopäälliköt voivat päivittää yhden asiakkaan, asiakasryhmän tai kaikkien asiakkaiden luottorajat ja vanhentumispäivät käyttämällä kirjausprosessia. Voit lisätä luottorajan oikaisumerkintöjä ja päivittää niillä asiakkaita ja asiakkaiden luottoryhmiä. Voit käyttää niitä myös automaattisten luottorajojen laskentaan. Merkintöjä voi sitten tarkistaa, lähettää hyväksyttäväksi työnkulun avulla ja kirjata asiakkaan tileille.

## <a name="set-up-credit-limit-adjustments"></a>Luottorajan oikaisujen määrittäminen

Voit luoda merkintöjä **Luottorajan oikaisu** -kirjauskansiossa **Luottorajan oikaisu** -sivulla (**Luotonhallinta \> Luottorajaoikaisut \> Luottorajaoikaisut**).

1. Valitse **Uusi**. Luotavassa uudessa merkintäryhmässä on luottarajan oikaisunumero.
2. Valitse luottorajan oikaisutyyppi:

    - Voit muuttaa asiakkaan luottorajaa valitsemalla **Luottoraja**.
    - Voit luoda väliaikaisen luottorajan valitsemalla **Väliaikainen luottoraja** sen sijaan, että muuttaisit asiakkaan nykyistä luottorajaa. Väliaikaiset luottorajat ohittavat asiakkaan määritetyn kauden luottorajan. Kun tämä kausi päättyy, asiakkaan luottoraja otetaan taas käyttöön.
3. Anna kuvaus. 

Jos **Kirjattu**-valintaruutu valitaan, luottorajoja on käytetty. **Hyväksynnän tila** -kenttä ilmaisee kirjauskansion työnkulun tilan. Työnkulku on valinnainen.

### <a name="add-credit-limit-adjustments"></a>Luottorajan oikaisujen lisääminen

Luottorajan oikaisut voi lisätä manuaalisesti valitsemalla **Rivit** ja toimimalla sitten seuraavien ohjeiden mukaisesti.

1. Jos haluat lisätä asiakkaan luottorajan oikaisuja, käytä **Asiakkaan oikaisut** -valikkoa. Jos haluat lisätä asiakkaan luottoryhmän luottorajan, valitse **Asiakkaan luottoryhmän oikaisut**.
2. Anna sen laskun asiakastili, joka on päivitettävä uudella luottorajalla. Jos valitsit **Asiakkaan luottoryhmän oikaisut** vaiheessa 1, anna asiakkaan luottoryhmä. Et voi antaa samalla kirjauskansioriville sekä asiakkaan tiliä että asiakkaan luottoryhmän tunnusta.

    Nykyinen luottoraja ja nimi tulevat automaattisesti näkyviin.

3. Anna uusi luottoraja, joka korvaa nykyisen luottorajan luottorajamerkintää kirjattaessa.
4. Anna päivämäärä, joka määrittää asiakkaan luottorajan uuden vanhentumispäivän. Luottorajan oikaisua luotaessa on annettava luottorajan vanhentumispäivä.

**Hyväksynnän tila** -kenttä ilmaisee kirjauskansiorivin työnkulun tilan.

Jos haluat, että luottorajan oikaisut luodaan automaattisesti, voit käyttää toimintoruudun **Luo**-valikkoa.
 
### <a name="add-temporary-credit-limit-adjustments"></a>Väliaikaisen luottorajan oikaisujen lisääminen

Väliaikaiset luottorajan oikaisut voidaan lisätä manuaalisesti valitsemalla suorittamalla seuraavat vaiheet kirjauskansion riveillä.

1. Jos haluat lisätä asiakkaan luottorajan oikaisuja, käytä **Asiakkaan oikaisut** -valikkoa. Jos haluat lisätä asiakkaan luottoryhmän luottorajan, valitse **Asiakkaan luottoryhmän oikaisut**.
2. Anna sen laskun asiakastili, joka on päivitettävä uudella luottorajalla. Jos valitsit **Asiakkaan luottoryhmän oikaisut** vaiheessa 1, anna asiakkaan luottoryhmä. Et voi antaa samalla kirjauskansioriville sekä asiakkaan tiliä että asiakkaan luottoryhmän tunnusta.

    Jos aktiivinen tai väliaikainen luottoraja on jo luotu aiemmin, kunkin väliaikaisen luottorajan kohdalla näkyy nykyinen väliaikainen luottoraja ja päivämääräväli. Nimi tulee näkyviin automaattisesti.

3. Anna nykyisen luottorajan korvaa uusi luottoraja.
4. Määritä **Uusi päivämäärästä**- ja **Uusi päivämääriin** -kenttiin jakso, jolloin luottorajan lisäasetukset ovat voimassa. Luottorajan oikaisukirjauskansiota luotaessa on annettava luottorajan vanhentumispäivät.

**Hyväksynnän tila** -kenttä ilmaisee kirjauskansiorivin työnkulun tilan.

## <a name="generate-credit-limit-adjustments"></a>Luottorajan oikaisujen luominen

Luottorajoja voi oikaista myös automaattisesti. Valitse toimintoruudussa **Luo** ja valitse sitten jokin seuraavista vaihtoehdoista:

- Aiemmin luodusta asiakkaasta
- Aiemmin luodusta asiakkaan luottoryhmästä
- Automaattiset luottorajat

### <a name="from-existing-customer"></a>Aiemmin luodusta asiakkaasta

Voit luoda kirjauskansion rivejä aiemmin luoduista asiakkaista. Kun valitset **Luo \> Aiemmin luodusta asiakkaasta**, valintaikkuna avautuu. Voit määrittää tässä valintaikkunassa kriteerit asiakkaiden valitsemiseen ja uusien rajojen laskemiseen.

1. Anna oikaisuarvo, jonka suuruinen summa lisätään luottorajaan tai vähennetään siitä. Anna negatiivinen arvo, jolla pienennetään nykyistä luottorajaa, tai positiivinen arvo, jolla rajaa suurennetaan.
2. Valitse **Arvon tyyppi** -kentässä, miten vaiheessa 1 annetun arvon avulla lasketaan uusi luottoraja:

    - Valitse **Kiinteä arvo**, jos luottorajaa muutetaan summalla.
    - Valitse **Prosenttiosuus**, jos luottorajaa muutetaan prosenttiosuudella.

3. Anna arvo, jolla laskettu luottoraja pyöristetään. Anna esimerkiksi **10,00**, jolloin luottoraja pyöristetään lähimpään 10,00 valuuttayksikköön.
4. Määritä **Pyöristystapa**-kentässä pyöristetäänkö jäljellä oleva summa ylös- vai alaspäin.
5. Valitse päivämäärien oikaisutapa.

    - Jos valitset **Absoluuttinen**, voit antaa päivämäärät, jotka määrittävät luottorajojen päivämäärävälin.
    - Jos valitset **Suhteellinen**, voit antaa päivämääräalueen siirtymäajan. Luottorajan nykyistä päivämääräaluetta oikaistaan siirtymällä.

6. Voit suodattaa **Sisällytettävät tietueet** -pikavälilehdessä sisällytettävien asiakkaiden luetteloa. Jos suodattimia ei sisällytetä, luottorajamerkinnät luodaan kaikille asiakkaille.
7. Luo luottorajan oikaisumerkinnät valitsemalla **OK**.

### <a name="from-existing-customer-credit-group"></a>Aiemmin luodusta asiakkaan luottoryhmästä

Voit luoda kirjauskansion rivejä aiemmin luoduista asiakkaan luottoryhmistä. Kun valitset **Luo \> Aiemmin luodusta asiakkaan luottoryhmästä**, valintaikkuna avautuu. Voit määrittää tässä valintaikkunassa kriteerit asiakkaan luottoryhmien valitsemiseen ja uusien rajojen laskemiseen. Kriteerit ovat samat, joita käytettiin kirjauskansion rivien luomiseen aiemmin luoduista asiakkaista. Katso ohjeet edellisestä osasta.

### <a name="automatic-credit-limits"></a>Automaattiset luottorajat

Voit luoda automaattisia luottorajoja määrittämään ja päivittämään asiakkaan luottorajoja. Automaattiset luottorajat luodaan riskiryhmälle, ja ne perustuvat tiettyihin pisteytysryhmissä käytettyihin arvoihin. Näitä automaattisia luottorajoja voi käyttää luottorajamerkintöjen luomiseen. Jos asiakas on määritetty tiettyyn riskiryhmään ja asiakkaan luottotiedot vastaavat automaattisen luottorajan kriteerejä, luottorajan oikaisumerkintä luodaan.

#### <a name="create-automatic-credit-limits"></a>Automaattisten luottorajojen luominen

Automaattisia luottorajoja luodaan käyttämällä luottorajan oikaisuja. Kun valitset **Luo \> Automaattiset luottorajat**, voit määrittää avautuvassa valintaikkunassa vanhentumispäivän uusille luottorajoille. Nämä luottorajat luodaan niiden riskiryhmien perusteella, joihin asiakkaat on määritetty. Kun olet valmis, luo luottorajan oikaisurivit valitsemalla **OK**.

### <a name="post-adjustments"></a>Oikaisujen kirjaaminen

Kun olet luonut luottorajan oikaisurivit, voit kirjata merkinnät ja päivittää asiakkaan luottorajat toimintoruudun **Kirjaa**-painikkeella. Jos olet kuitenkin määrittänyt työnkulun, kirjauskansio on lähetettävä hyväksyttäväksi valitsemalla toimintoruudussa **Työnkulku \> Lähetä**.

### <a name="credit-limit-adjustments-workflows"></a>Luottorajan oikaisujen työnkulut

**Luottorajan oikaisut** -työnkulkujen avulla voi lähettää luottorajan oikaisut työnkulun hyväksyntäprosessiin. Voit luoda kaksi työnkulkua **Luotonhallinnan työnkulku** -sivulla (**Luotonhallinta \> Asetukset \> Luotonhallinnan työnkulku**):

- **Luottorajan oikaisut** – tätä työnkulkua käytetään merkintöjen hyväksymiseen otsikkotasolla.
- **Luottorajan oikaisurivi** – tätä työnkulkua käytetään oikaisumerkintöjen hyväksymiseen siten, että eri henkilöt voivat hyväksyä merkinnät työnkulun kriteerien perusteella.

> [!NOTE]
> **Luottorajan oikaisut** -työnkulkua luotaessa työnkulku määritetään siten, että oikaisut kirjataan automaattisesti sen jälkeen, kun rivit on hyväksytty. Työnkulkuun tarvitsee sisällyttää vain **Kirjaa kirjauskansio automaattisesti** -tehtävä.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
