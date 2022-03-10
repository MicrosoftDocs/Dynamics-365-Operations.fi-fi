---
title: Määrityksistä poikkeamisten luonti ja käsittely
description: Tässä aiheessa kerrotaan, miten voit hallita määrityksistä poikkeamisia aiemmin luodun laatutilauksen perusteella.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 032f5b712c2be5312524129cd25e655e778f5f44
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580861"
---
# <a name="create-and-process-nonconformances"></a>Määrityksistä poikkeamisten luonti ja käsittely

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kerrotaan, miten voit hallita määrityksistä poikkeamisia aiemmin luodun laatutilauksen perusteella. Määrityksistä poikkeamisen hallinnan hoitaa yleensä laatutyöntekijä. Edellytyksenä laatutilauksen on oltava käytettävissä. (Lisätietoja laatutilauksen luomisesta on kohdassa [Tarkista tavaroiden laatu](inspect-quality-goods.md).)

Ennen kuin käyttäjä voi käsitellä määrityksistä poikkeamisen hyväksynnän, työntekijä on liitettävä niihin **Henkilö**-kentässä **Käyttäjät**-sivulla. Ennen kuin käyttäjä voi käyttää asiakirjan huomautuksia, **Ota tiedoston käsittely käyttöön** -kentän arvoksi on asetettava *Kyllä* käyttäjän asetuksissa.

## <a name="create-a-nonconformance"></a>Luo määrityksistä poikkeaminen

Voit luoda määrityksistä poikkeamisen seuraavasti.

1. Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Määrityksistä poikkeamiset**.
1. Valitse toimintoruudussa **Uusi**.
1. Valitse **Luo määrityksistä poikkeaminen** -valintaikkunan **Ongelman tyyppi** -kentässä ongelman tyyppi, joka löydettiin tarkastusprosessin aikana.
1. Valitse **OK**.

## <a name="approve-or-reject-a-nonconformance"></a>Hyväksy tai hylkää määrityksistä poikkeaminen

Voit hyväksyä tai hylätä määrityksistä poikkeamisen seuraavasti.

1. Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Määrityksistä poikkeamiset**.
1. Etsi ja valitse luettelosta päivitettävä määrityksistä poikkeaminen.

    > [!NOTE]
    > Voit lisätä korjauksen vain hyväksyttyihin määrityksistä poikkeamisiin.

1. Valitse toimintoruudussa **Toiminnot \> Hyväksy määrityksistä poikkeaminen** hyväksyäksesi määrityksistä poikkeamisen tai **Toiminnot \> Hylkää määrityksistä poikkeaminen** hylätäksesi sen. Voit liittää hyväksytyt määrityksistä poikkeamisen [liittyviin toimintoihin](../quality-operations.md). Näin voit kirjata määrityksistä poikkeamisen käsittelyn ja korjauskäsittelyn osana tehtyä työtä.
1. Järjestelmä pyytää vahvistamaan valinnan. Jatka valitsemalla **Kyllä**.

## <a name="add-operations-and-other-details-to-nonconformances"></a>Toimintojen ja muiden tietojen lisääminen määrityksistä poikkeamisiin

Kun olet luonut määrityksistä poikkeamisen, voit alkaa lisätä siihen liittyviä toimintoja ja määrittää näiden toimintojen lisätietoja. Voit lisätä liittyvät toiminnot vain hyväksyttyihin määrityksistä poikkeamisiin.

Perustietojen lisäksi voit lisätä toimintoon seuraavia tietoja:

- **Nimikkeet** – Voit luoda luettelon korjauksen suorittamiseen kulutetuista nimikkeistä. Nimikkeet voivat olla esimerkiksi tuotteita, joita tarvitaan valmiin tuotteen korjausta varten tarvittavien laitteiden tai ainesosien korjaamiseen.
- **Laatukulut** – Voit luoda luettelon kuluista, jotka syntyvät tai laskutetaan ulkoisista lähteistä.
- **Työaikaraportti** – Voit luoda lokin ajasta, jonka kukin työntekijä käyttää toiminnossa.

Muut asetukset ovat valinnaisia. Kunkin nimikkeen, laatukulujen ja aikaraportin kustannukset lasketaan yhteen, ja ne näkyvät toiminnossa. Toiminnon **Kustannus**-kenttää ei voi muokata suoraan.

### <a name="create-an-operation-for-a-nonconformance"></a>Toiminnon luominen määrityksistä poikkeamiselle

Voit luoda toiminnon määrityksistä poikkeamiselle seuraavasti.

1. Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Määrityksistä poikkeamiset**.
1. Etsi ja valitse luettelosta päivitettävä määrityksistä poikkeaminen.

    > [!NOTE]
    > Voit lisätä toimintoja tai päivittää niitä vain hyväksyttyihin määrityksistä poikkeamisiin.

1. Valitse toimintoruudussa **Liittyvät toiminnot**.
1. Valitse **Liittyvät toiminnot** -sivulla toimintoruudussa **Uusi** lisätäksesi rivin ruudukkoon. Määritä sitten uudelle rivillä seuraavat kentät:

    - **Toiminto** – Valitse määrityksistä poikkeamista varten suoritettavan toiminnon koodi.
    - **Syy** – Kirjoita yksityiskohtainen kuvaus, jossa kerrotaan, miksi toiminto on pakollinen.
    - **Myyntitilaus** – Jos valittu toimintokoodi liittyy myyntitilauksen tyyppiin, valitse myyntitilaus, johon linkität toiminnon.
    - **Ostotilaus** – Jos valittu toimintokoodi liittyy ostotilauksen tyyppiin, valitse ostotilaus, johon linkität toiminnon.

1. Sulje sivut.

### <a name="add-items-to-an-operation"></a>Nimikkeiden lisääminen toimintoon

Voit lisätä nimikkeitä toimintoon noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Määrityksistä poikkeamiset**.
1. Etsi ja valitse luettelosta päivitettävä määrityksistä poikkeaminen.

    > [!NOTE]
    > Voit lisätä toimintoja tai päivittää niitä vain hyväksyttyihin määrityksistä poikkeamisiin.

1. Valitse toimintoruudussa **Liittyvät toiminnot**.
1. Valitse **Liittyvät toiminnot** -sivulla toiminto, johon haluat lisätä nimikkeitä.
1. Valitse toimintoruudussa **Nimikkeet**.
1. Valitse **Liittyvät toiminnot** -sivulla toimintoruudussa **Uusi** lisätäksesi rivin ruudukkoon. Määritä sitten uudelle rivillä seuraavat kentät:

    - **Nimiketunnus** – Valitse tuote, joka kulutetaan osana valittua toimintoa.
    - **Määrä** – Kirjoita kulutettava nimikemäärä.

    > [!NOTE]
    > Voit tarkastella nimikkeen kustannusta **Kustannus**-kentässä **Yleiset**-välilehdessä. Siellä näkyvä kustannus tulee **Vapautettu tuote** -sivulla määritettyjen kustannusten perusteella. Kustannusta ei voi päivittää suoraan **Liittyvä toimintonimike**-sivulla. Kaikkien **Liittyvät toimintonimikkeet** -sivulla lisättyjen nimikkeiden kustannus lisätään automaattisesti **Kustannus**-kenttään **Liittyvät toiminnot** -sivulla.

1. Toista edellinen vaihe kullekin lisättävälle nimikkeelle.
1. Sulje sivut.

### <a name="add-quality-charges-to-an-operation"></a>Laatukulujen lisääminen toimintoon

Voit lisätä laatukuluja toimintoon noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Määrityksistä poikkeamiset**.
1. Etsi ja valitse luettelosta päivitettävä määrityksistä poikkeaminen.

    > [!NOTE]
    > Voit lisätä toimintoja tai päivittää niitä vain hyväksyttyihin määrityksistä poikkeamisiin.

1. Valitse toimintoruudussa **Liittyvät toiminnot**.
1. Valitse **Liittyvät toiminnot** -sivulla toiminto, johon haluat lisätä laatukuluja.
1. Valitse toimintoruudussa **Laatukulut**.
1. Valitse **Liittyvät toimintokulut** -sivulla toimintoruudussa **Uusi** lisätäksesi rivin ruudukkoon. Määritä sitten uudelle rivillä seuraavat kentät:

    - **Kulujen koodi** – Valitse lisättävä laatukulu.
    - **Kuvaus** – Anna kulun yksityiskohtainen kuvaus.
    - **Kulujen arvo** – Anna veloitettavan kulun summa.

1. Toista edellinen vaihe kullekin lisättävälle kululle.
1. Sulje sivut.

> [!NOTE]
> **Kulujen arvo** -kentän summa lasketaan automaattisesti kaikkien laatukulujen osalta ja lisätään muihin summiin **Kustannus**-kentässä **Liittyvät toiminnot** -sivulla.

### <a name="create-a-timesheet-on-an-operation"></a>Aikaraportin luominen toimintoa varten

Voit lisätä aikaraportin toimintoon noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Määrityksistä poikkeamiset**.
1. Etsi ja valitse luettelosta päivitettävä määrityksistä poikkeaminen.

    > [!NOTE]
    > Voit lisätä toimintoja tai päivittää niitä vain hyväksyttyihin määrityksistä poikkeamisiin.

1. Valitse toimintoruudussa **Liittyvät toiminnot**.
1. Valitse **Liittyvät toiminnot** -sivulla toiminto, johon haluat lisätä aikaraportin.
1. Valitse toimintoruudussa **Aikaraportti**.
1. Valitse **Liittyvän toiminnon aikaraportit** -sivulla toimintoruudussa **Uusi** lisätäksesi rivin ruudukkoon. Määritä sitten uudelle rivillä seuraavat kentät:

    - **Päivämäärä** – Määritä päivämäärä, jolloin työ on tehty. Oletusarvoisesti tämä kenttä on nykyinen päivämäärä.
    - **Työntekijät** – Valitse työntekijä, joka teki työn. Oletusarvon mukaan tässä kentässä on työntekijä, joka on määritetty nykyiselle käyttäjälle.
    - **Toiminnon tunnit** – Kirjoita valitussa toiminnossa tehtyjen tuntien määrä.
    - **Laskutettu** – Valitse tämä valintaruutu, jos aika on veloitettu laskussa asiakkaalle tai toimittajalle.

    > [!NOTE]
    > Voit tarkastella kustannusta **Kustannus**-kentässä **Yleiset**-välilehdessä. Kustannukset lasketaan käyttämällä **Varastonhallinnan parametrit** -sivulla määrittämääsi hintaa.

1. Toista edellinen vaihe kullekin lisättävälle aikaraportin riville.
1. Sulje sivut.

> [!NOTE]
> **Kustannus**-kentän summa lasketaan kaikkien aikaraportin rivien osalta ja lisätään muihin summiin **Kustannus**-kentässä **Liittyvät toiminnot** -sivulla.

## <a name="add-a-correction-to-a-nonconformance"></a>Korjauksen lisääminen määrityksistä poikkeamiseen

Voit lisätä korjauksen määrityksistä poikkeamiseen seuraavasti:

1. Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Määrityksistä poikkeamiset**.
1. Etsi ja valitse luettelosta päivitettävä määrityksistä poikkeaminen.

    > [!NOTE]
    > Voit lisätä korjauksen vain hyväksyttyihin määrityksistä poikkeamisiin.

1. Valitse toimintoruudussa **Korjaukset**.
1. Valitse **Korjaukset**-sivulla toimintoruudussa **Uusi** lisätäksesi rivin ruudukkoon. Määritä sitten uudelle rivillä seuraavat kentät:

    - **Diagnostiikka** – Valitse diagnostiikkatyyppi, joka määrittää luotavien korjausten tyypin.
    - **Työntekijä** – Valitse henkilö, joka on vastuussa korjauksesta.
    - **Korjausjärjestys** – Valitse vaihtoehto, joka määrittää, miten korjaus priorisoidaan (*pieni*, *normaali* tai *suuri*).
    - **Vaadittu päivämäärä** – Määritä päivämäärä, jolloin korjaustoimintoa pyydettiin.
    - **Suunniteltu päivämäärä** – Syötä päivämäärä, jolloin korjaus on tarkoitus tehdä loppuun.
    - **Lyhytaikainen ratkaisu** – Valitse tämä valintaruutu, jos korjaustoiminto korjaa määrityksistä poikkeamisen vain lyhyen ajan.

1. Sulje sivut.

## <a name="mark-a-correction-as-completed"></a>Korjauksen merkitseminen valmiiksi

Voit merkitä määrityksistä poikkeamisen korjauksen valmiiksi seuraavasti.

1. Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Määrityksistä poikkeamiset**.
1. Etsi ja valitse luettelosta päivitettävä määrityksistä poikkeaminen.

    > [!NOTE]
    > Voit lisätä korjauksen vain hyväksyttyihin määrityksistä poikkeamisiin.

1. Valitse toimintoruudussa **Korjaukset**.
1. Valitse **Korjaukset**-sivun ruudukosta korjaus, jonka haluat merkitä valmiiksi.
1. Valitse toimintoruudussa **Merkitse valmiiksi**.
1. Järjestelmä pyytää vahvistamaan valinnan. Jatka valitsemalla **OK**. **Valmistumispäivämäärä ja -aika** -kentän arvoksi tulee nykyinen päivämäärä ja aika, ja **Valmis**-valintaruutu on valittuna.
1. Sulje sivu.

## <a name="reopen-a-completed-correction"></a>Valmiin korjauksen avaaminen uudelleen

Voit avata valmiin korjauksen uudelleen seuraavasti.

1. Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Määrityksistä poikkeamiset**.
1. Etsi ja valitse luettelosta päivitettävä määrityksistä poikkeaminen.
1. Valitse toimintoruudussa **Korjaukset**.
1. Valitse **Korjaukset**-sivun ruudukosta korjaus, jonka haluat avata uudelleen.
1. Valitse toimintoruudussa **Avaa uudelleen**.
1. Järjestelmä pyytää vahvistamaan valinnan. Jatka valitsemalla **OK**. Arvo poistetaan **Valmistumispäivämäärä ja -aika** -kentästä, ja **Valmis**-valintaruudun valinta poistetaan.
1. Sulje sivu.

Korjaukseen voi nyt tehdä lisämuokkauksia tai päivityksiä. Kun olet valmis, voit merkitä korjauksen valmiiksi uudelleen.

## <a name="close-a-nonconformance"></a>Sulje määrityksistä poikkeaminen

Voit sulkea määrityksistä poikkeamisen seuraavasti.

1. Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Laatutilaukset**.
1. Valitse ruudukosta laatutilaus.
1. Valitse toimintoruudussa **Tiedustelut \> Määrityksistä poikkeamiset**.
1. Valitse **Määrityksistä poikkeamiset** -sivulla ruudukosta kohteena oleva määrityksistä poikkeaminen.
1. Valitse toimintoruudussa **Toiminnot \> Sulje määrityksistä poikkeaminen**.
1. Järjestelmä pyytää vahvistamaan valinnan. Jatka valitsemalla **Kyllä**.
1. Sulje sivut.

## <a name="additional-resources"></a>Lisäresurssit

- [Laadunhallinnan yleiskuvaus](../quality-management-processes.md)
- [Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön](../enable-quality-management.md)
- [Määrityksistä poikkeamisia hyväksyvät työntekijät](../quality-responsible-workers.md)
- [Määrityksistä poikkeamisia koskevat karanteenivyöhykkeet](../quality-quarantine-zones.md)
- [Määrityksistä poikkeamisten diagnostiikkatyypit](../quality-diagnostic-types.md)
- [Määrityksistä poikkeamisten laatukulut](../quality-charges.md)
- [Toiminnot määrityksistä poikkeamisille](../quality-operations.md)
- [Laadunhallinta varastoprosesseja varten](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
