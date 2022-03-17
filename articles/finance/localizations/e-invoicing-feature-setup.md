---
title: Ominaisuusmääritysten käyttäminen
description: Tässä aiheessa selitetään, miten sähköisen laskutuksen ominaisuudet määritetään.
author: dkalyuzh
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 41ffc9c7009291a55392e50c5e490d3288d122bc
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371622"
---
# <a name="work-with-feature-setups"></a>Ominaisuusmääritysten käyttäminen

[!include [banner](../includes/banner.md)]

Voit määrittää sähköisten tiedostojen luonnin ja muut käsittelyvaiheet (esimerkiksi tiedostojen digitaalisten allekirjoitusten, lähettämisen valtion Internet-palveluun ja vastauksen vastaanottamisen tai niiden tallentamisen), määrittää käsittelyputken, käytettävyyssäännöt ja muuttujat sähköisen laskutuksen ominaisuuksille.

Asetustiedot yhdistetään *toiminnon asetus*-malliin, ja ne voidaan luoda, poistaa ja muuttaa. Myös sähköisen laskutuksen ominaisuuksien valmiiden versioiden tietoja voi tarkastella.

Voit luoda niin monta toimintoasetusta kuin sähköisten tiedostojen luomista, käsittelyä ja vastaanottamista varten tarvitaan erilaisia skenaarioita. Vaikka näillä toimintojen asetuskohteilla on itsenäiset käsittelytoiminnot ja ehdot suoritusta varten, ne luodaan osana yhtä sähköistä laskutusominaisuutta ja perivät sen elinkaaren ja käyttöönottoprosessin.

## <a name="add-a-feature-setup"></a>Toimintoasetuksen lisääminen

1. Kirjaudu sisään Regulatory Configuration Service (RCS) -tilillesi.
2. Valitse **Globalisaatio-ominaisuus** -työtilan **Toiminnot**-osassa **Sähköinen laskutus** -ruutu.
3. Valitse **Sähköisen laskutuksen ominaisuudet** -sivulla, että sähköisen laskutuksen versio, jonka tila on **Luonnos**.
4. Valitse **Määritykset**-välilehdessä **Lisää**.
5. Valitse avattavan **Toimintoasetusten luonti** -valintaikkunan **Uusi** kenttäryhmässä jokin seuraavista vaihtoehdoista:
 
    - **Mukautetut asetukset** – Voit luoda uusia toimintoasetuksia, joissa on tyhjät kanavat, tyhjä käsittelyputken luettelo, tyhjä osa käytettävyyssääntöjä varten ja oletusmuuttujajoukko asetustyypin mukaan.
    - **Ominaisuuksien asetuksista** – Luo kopio toisen ominaisuuden asetuksista nykyisen sähköisen laskutustoiminnon käyttöalueen mukaan.

6. Jos olet valinnut edellisen vaiheen **Mukautetut asetukset** -vaihtoehdon, kirjoita toiminnon asetuskohteen nimi ja kuvaus ja valitse sitten **Asetustyyppi**-kenttäryhmästä jokin seuraavista vaihtoehdoista:

    - **Käsittelyputki** – Valitsemalla tämän vaihtoehdon voit luoda ja käsitellä lähteviä sähköisiä tiedostoja. Järjestelmä luo tätä asetustyyppiä varten tyhjän käsittelyputkiluettelon, tyhjän osan käytettävyyssääntöjä varten sekä muuttujien oletusjoukon. Et voi käyttää saapuvien sähköisten tiedostojen kanavia.
    - **Tietokanava** – Valitsemalla tämän vaihtoehdon voit määrittää prosessin, joka vastaanottaa saapuvia sähköisiä asiakirjoja määritetyistä kanavista ja siirtää ne suoraan Microsoft Dynamics 365 Financeen tai Dynamics 365 Supply Chain Managementiin ilman lisätoimintoja. Järjestelmä luo tätä asetustyyppiä varten tietokanavien esimääritetyn parametriluettelon, tyhjän osan käytettävyyssääntöjä varten sekä oletusmuuttujien joukon. Et voi lisätä mitään toimintoja käsittelyputkeen.
    - **Tietokanava ja käsittelyputki** – Tämä asetustyyppi muistuttaa **Tietokanava**-asetustyyppiä. Ennen kuin saapuva sähköinen asiakirja välitetään Financeen tai Supply Chain Managementiin, voit kuitenkin määrittää käsittelyputkeen lisätoimintoja.

7. Jos olet valinnut **Tietokanava**- tai **Tietokanavan ja käsittelyputki** -vaihtoehdon viimeisessä vaiheessa, valitse **Valitse tietokanava** -kentästä kanava, jonka kanssa haluat integroida.
8. Valitse **Luo**.

Kun toiminnon asetukset on luotu, voit konfiguroida sen valitsemalla **Muokkaa**.

## <a name="edit-a-feature-setup"></a>Toimintoasetuksen muokkaaminen

Toimintoasetusten tyypin mukaan voit konfiguroida lähtevien sähköisten tiedostojen muodostamisprosessin ja niiden lähettämisen ulkoisiin kanaviin tai saapuvien asiakirjojen vastaanottamisen ja siirtämisen Finance- tai Supply Chain Management -sovellukseesi.

### <a name="data-channel"></a>Tietokanava

*Tietokanava* vie sähköisen tiedoston ja käsittelee sen tai siirtää sen suoraan Financeen tai Supply Chain Managementiin. Tämä vaihtoehto ei ole käytettävissä **Käsittelyputki**-tyypin ominaisuusasetuksissa.

Voit määrittää tietokanavan kirjoittamalla kanavan nimen. Määritä sitten parametrit valitun kanavatyypin perusteella. Tietokanavan tunnuksen on viitattava muuttujaan, joka on luotu erityisesti tietokanavan yksilöimiseksi. Sitä käytetään viitteenä Financessa ja Supply Chain Managementissa.

Määritä **Liitteiden suodatin** -välilehdessä suodattimet, jotka noutavat tietyt tiedostot kanavasta. Voit luoda useita rivejä, jos odotat, että tiedostoilla on eri tiedostonimitunnisteita tai jos tiedostot on käsiteltävä eri tavalla tiedostonimen mukaan. Pääparametrit ovat seuraavat:

- **Nimi** – Kirjoita sen tiedoston nimi, johon järjestelmä viittaa käsittelyn aikana. Finance- ja Supply Chain Management -sovelluksessa tiedostot näkyvät lähetyslokissa.
- **Suodata** – Määritä suodatin tiedostojen valintaa varten.
- **Valinnainen** – Jos tämän valintaruudun valinta on tyhjä, tiedosto on pakollinen. Tässä tapauksessa järjestelmä näyttää virhesanoman, jos kanavat eivät sisällä suodatinta vastaavia tiedostoja. Tämä parametri koskee sähköposteja.

Jos kanava on postilaatikko ja saapuva sähköposti sisältää useita liitteitä, voit määrittää sääntöjä, jotka määrittävät, miten palvelu käsittelee liitteet. Palvelu voi ottaa kunkin liitteen huomioon erillisenä sähköisenä laskuna tai se voi käsitellä yhtä liitettä päälaskuna ja kaikkia muita liitteitä lisäyksinä.

### <a name="processing-pipeline"></a>Käsitellään jaksoa

*Käsittelyputki* on joukko *toimintoja*, jotka suoritetaan peräkkäin, kunnes ne on suoritettu onnistuneesti loppuun. Käsittelyputken avulla voit määrittää sähköisten tiedostojen luomisprosessin ja suorittaa muita vaiheita (kuten allekirjoittaa tiedostoja digitaalisesti, lähettää ne ulkoisiin Internet-palveluihin, jäsentää vastauksen sekä vastaanottaa ja käsitellä saapuvia tiedostoja).

Toimenpiteiden luettelo on esimääritetty. **Uusi**- ja **Poista**-painikkeilla voit määrittää toimenpiteiden yhdistelmän, joka loogisesti määrittää asiakirjojen lähetys- ja vastaanottoprosessit.

Toimintojen järjestys on erittäin tärkeä. Voit säätää järjestystä **Ylös**- ja **Alas**-painikkeilla.

Jokaisella toiminnolla on parametrijoukko, jonka voit konfiguroida tai muuttaa. Tietty parametrijoukko riippuu toimenpiteen tyypistä.

- **Toiminto** – Valitse toiminnon tyyppi.
- **Toiminnon nimi** – Anna toiminnon nimi. Tämä nimi näkyy lähetyslokissa ja viesteissä Finance- ja Supply Chain Management -sovelluksissa.
- **Kuvaus** – Anna lisätietoja prosessin toimenpiteen tarkoituksesta.
- **Ota uudelleenyritys käyttöön** – Jos valitset tämän valintaruudun, voit valita toimenpiteen **Uudelleenyritä toimintoa** -kentästä ja määrittää lisäparametreja **Uudelleenyritysparametrit**-välilehdessä.

    Uudelleenyritystoimintojen avulla voit konfiguroida palvelun toiminnan, jos tiettyä toimintoa ei voi suorittaa. Jos esimerkiksi ulkoinen Internet-palvelu, jonne yrität muodostaa yhteyden, ei vastaa, voit määrittää, kuinka monta kertaa järjestelmä yrittää muodostaa yhteyden uudelleen, millä aikavälillä ja mistä käsittelyputken toiminnosta.

- **Vie tulokset** – Voit valita tämän valintaruudun käsittelyputken *yhdelle* toiminnolle. Sähköinen tiedosto, jonka toimenpide tuottaa Finance- tai Supply Chain Management -sovelluksessa, voidaan tämän jälkeen viedä **Sähköisten tiedostojen lähetysloki** -sivulta.

### <a name="applicability-rules"></a>Soveltuvuussäännöt

*Käytettävyyssäännöt* ovat määritettäviä lausekkeita, jotka antavat kontekstin suoritettaville sähköisen laskutuksen ominaisuuksille sähköisen laskutuksen ominaisuusjoukon avulla.
Kun Financesta tai Supply Chain Managementista lähetetään liiketoiminta-asiakirja sähköiseen laskutukseen, liiketoiminta-asiakirjassa ei ole täsmällistä viitettä, jonka avulla sähköinen laskutustoiminto voi kutsua tiettyä sähköisen laskutustoiminnon versiota ja tiettyä toimintoasetusta lähetyksen käsittelemiseksi. Kun liiketoiminta-asiakirja on kuitenkin konfiguroitu oikein, se sisältää tarvittavat elementit, joiden avulla sähköinen laskutus voi ratkaista, minkä sähköisen laskutuksen ominaisuuden version ja käsittelyputken on oltava valittuna ja suoritettavana.

Sovellettavuussääntöjen avulla sähköinen laskutuspalvelu voi etsiä lähetyksen suorittamisessa käytettävät tarkat sähköiset laskutusominaisuudet. Jotta oikeat toiminnot voidaan löytää, lähetetyn liiketoiminta-asiakirjan **Konteksti**-kentät on täsmäytetty käytettävyyssääntöjen lausekkeiden kanssa.

Voit käyttää käytettävyyssääntöjä seuraavasti:

- Valitse **Uusi**, kun haluat lisätä uuden lausekkeen käytettävyyssääntöjoukkoon.
- Poista lauseke valitsemalla **Poista**.
- Valitse useita tietueita ja luo kohteiden tai loogisten lauseiden yhdistelmä **Ryhmittele**- tai **Pura ryhmittely** -painikkeen avulla. Valitse esimerkiksi rivit, jotka haluat ryhmitellä, ja valitse **Ryhmittele lauseke**. Kun lausekkeita ryhmitellään, ruudukkoon lisästään uusi sarake. Tämä sarake määrittää ryhmiteltyjen lausekkeiden loogisen operaattorin. Tuetaan seuraavia operaattorityyppejä:

    - Equal
    - Not equal
    - Suurempi kuin / pienempi kuin
    - suurempi tai yhtä suuri kuin / pienempi tai yhtä suuri kuin
    - Contains
    - Aloitus

    > [!NOTE]
    > Kun purat lausekkeen ryhmittelyn, aloita aina sisimmästä ryhmittelytasosta.

### <a name="variables"></a>Muuttujat

*Muuttujat* ovat joustavampia määrittäessäsi käsittelyputkea ja tietojen kulkua toimenpiteiden välillä. Joissakin toimenpideparametreissa voi viitata muuttujaan tietojen tai sähköisten tiedostojen väliaikaisesti tallentamista varten. Joidenkin muuttujien avulla voidaan siirtää tietoja Finance- ja Supply Chain Management -sovelluksen ja sähköisen laskutuspalvelun välillä.

Järjestelmä luo oletusarvoisesti joitakin muuttujia. Esimerkiksi **BusinessDocumentDataModel**-muuttuja sisältää JavaScript Object Notation (JSON) -muotoisia liiketoimintatietoja, jotka lähetysprosessin aikana tulevat liitetyn sovelluksen kutsusta.

Käytettävissä ovat seuraavat muuttujatyypit:

- **Vakio** – säilö, johon tallennetaan putken toimenpiteiden käsittelyssä käytettävät tilapäiset tiedot.
- **Asiakkaalta** – Muuttujan sisältö hankitaan Dynamics 365 -asiakkaalta lähetysprosessin suorittamisen aikana.
- **Asiakkaalle** – Dynamics 365 -asiakas antaa muuttujan sisällön käyttöön lähetysprosessin suorittamisen aikana.
- **Tietotyyppi** – Valitse muuttujaan tallennettujen tietojen tietotyyppi.

### <a name="parameters"></a>Parametrit

**Poista liiketoimintatietojen poistaminen käytöstä** -valintaa käytetään optimoimaan Finance- tai Supply Chain Management -sovelluksesta tulevien liiketoimintatietojen työkuorman rakenteen sähköisten tiedostojen lähettämisen aikana. Optimointi helpottaa sähköisen laskutuspalveluun menevien tietojen vähentämistä, jotta tietoja voidaan muuttaa edelleen vaadituksi sähköiseksi tiedostoksi. Oletusarvo on **Ei**.

- **Kyllä** – Finance tai Supply Chain Management lähettää **Laskumalli**- tai **Kirjanpitomalli** (Brasilia) -rakenteen JSON-tiedoston, joka määritetään **Sähköinen raportointi** -moduulissa. Kaikkiin mallin elementteihin täytetään sovelluksen puolelta liiketoimintatiedot lopullisesta sähköisen tiedoston rakenteesta riippumatta. Mallit sisältävät yleensä enemmän liiketoimintatietoja kuin kohdetiedostorakenne vaatii, ja näiden tietojen luomiseen sovelluksessa voi kulua enemmän aikaa. **Kyllä**-arvo on pakollinen niissä harvinaisissa tapauksissa, joissa haluat luoda erilaisia tulostiedostoja yhdessä sähköisessä laskutusominaisuudessa ja ominaisuusasetuksessa. **Kyllä**-arvo on hyödyllinen, kun teet vianmääritystä skenaarioille, sähköisten tiedostojen rakenteelle ja liiketoimintatietojen täydellisyydelle.
- **Ei** – Finance tai Supply Chain Management kutsuu ensimmäiseksi palvelua ilman liiketoimintatietoja. Tämän kutsun tarkoituksena on saada tietoja sähköisen raportoinnin (ER) konfiguroinnista, jota käytetään sähköisen tiedoston muuntamisessa käsittelyputkessa. Nämä tiedot palautetaan sovellukseen, joka määrittää niiden avulla niiden liiketoimintatietojen osajoukon, jotka tulee sisällyttää **Laskumalli**- tai **Kirjanpitomalli** (Brasilia) -rakenteen JSON-tiedostoon. **Ei**-arvo tälle asetukselle vähentää sovelluksen palveluun lähettämien liiketoimintatietojen määrää, koska sovellus voi lähettää vain ne liiketoimintatiedot, joita sähköisten tiedostojen luominen edellyttää.

### <a name="validate-a-feature-setup"></a>Toimintomäärityksen vahvistaminen

Voit suorittaa vahvistuksen tarkistaaksesi koko määrityksen yhdenmukaisuuden. Jos esimerkiksi toimen pakollinen parametri on jätetty tyhjäksi, vahvistus havaitsee tämän ristiriidan ja näyttöön tulee varoitusviesti.

- Valitse **Toimintoversion määritys** -sivun toimintoruudussa **Vahvista**.

## <a name="delete-a-feature-setup"></a>Toimintomäärityksen poistaminen

1. Valitse **Sähköisen laskutuksen ominaisuudet** -sivulla, että sähköisen laskutuksen versio, jonka tila on **Luonnos**.
2. Valitse **Määritykset**-välilehdessä **Poista**.
3. Vahvista toimintoasetusten poisto valitsemalla näyttöön tulevassa sanomaruudussa **Kyllä**.
